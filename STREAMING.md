# Zender Streaming with Phenix RTS
This document describes how to configure your streaming solution to ingest the video signal.

# Architecture:
 This diagram shows how the zender infrastructure integrates the video signal

![Zender Streaming Architecture](docs/images/zender-streaming-architecture.png?raw=true "Zender Streaming Architecture")

The streaming source (camera) needs to be converted to a digital streaming signal.

This is done by a video encoder that typically exists in 3 types of solutions:
1) directly from the browser (not for production)
2) Using a software encoder
OBS https://obsproject.com/ , Wirecast: https://www.telestream.net/wirecast/
3) Hardware encoder (Elemental)

The ingest point is where the encoder sends its signal to so it can be delivered to the endusers (CDN). In order to player the stream there needs to be a compatible player.

Note: 
- Ingest streams are best restarted daily. When a stream is too long running the drift between audio/video packets can be too large to make the synching working well.
- Ingesting bandwidth has a cost associated, be sure to stop the stream when it's not needed

# Encoder settings

- bitrate: 1.5 Mbit/sec
- aspect ratio: 9:16 (portrait) or 16:9 (landscape)
- dimensions: 608x1080 (portrait) or 1080x608 (landscape)
- audio bitrate: 128kbit/sec
- audio sampling rate:  44.1kHz
- frames per second: 25
- H264 profile: baseline
	- there is no need for main: it is re-encoded to baseline anyway
	- also baseline has less latency
- Keyframe interval : 1 second

Note that higher bitrates & dimensions are supported but typically unnecessary for mobile devices playback. This will increase the cost due to additional bandwidth costs.

# Encoder tunings
## AWS Elemental
- Avoid using B-Frames
- Decrease the buffer size to half of the bitrate
- Uncheck the box for Temporal AQ.

## Wirecast
Use ```x264 --tune zerolatency```

## OBS

It is important to remember that the machine that is running the ingest source needs to have a CPU that is fast enough and that has enough network bandwidth to sustain the outgoing bitrate.

When the machine does not have the required CPU power to run the stream in real time, OBS will need to queue up the frames to be encoded, which will result in increased latency. If the outgoing bit rate is higher than the network bandwidth, it will also result in increased latency as the outgoing frames need to be queued up.

Our internal tests have shown that under some of these circumstances OBS has rendered increased latency of 1 to over 10 seconds.

### Configure the RTMP ingest point in the Stream Config:
![OBS Stream Config](docs/images/obs/obs-stream-config.png?raw=true "OBS Stream Config")

### Configure the Video Settings:
Note: you need to check advanced mode , otherwise the options are not visible in the interface

To configure OBS – Go to Setting > Output > Select “Advanced”:
-  Check “Use Custom Buffer Size”. Set the buffer size to 0.
-  Set Tune to “zero latency”.	If you are on Windows - Go to Settings > Advanced -   Check New Network Code
-  Check Low Latency Mode

- Configure Bitrate
- Set keyframe interval to : 1 second (otherwise the latency will have a long delay)

![OBS Video Config](docs/images/obs/obs-video-config.png?raw=true "OBS Video Config")

### Configure Audio
![OBS Audio Config](docs/images/obs/obs-audio-config.png?raw=true "OBS Audio Config")

### Configure Output
![OBS Output Config](docs/images/obs/obs-output-config.png?raw=true "OBS Output Config")

To minimize CPU usage - try the follow alternatives
- Lower the output resolution by going into Settings > Output and check Rescale Output.
- Try half of 720p (640x360).
- Try a faster CPU Usage Profile. Also found in Settings > Output


# Latency & Drift:
For ultra low Latency the latency varies around 2-3 seconds.

Drift is minimal across devices thanks to the Synchronisation Protocol built in to the phenix player.

NOTE: the expected latency needs to be configured in the Zender Quiz module to make sure the questions are synchronized with the video signal.

Additional optimizations for lower latency: It's tempting to optimize for latency only but this will have an impact on the stream stability too, so ideally there is a balance between these two.

# Phenix Streaming
## RTMP Ingest point(s):

For ingest done over RTMP, this needs to be configured. You can use both at the same time for redundancy purposes if required for your use case. Note that additional ingest bandwidth also adds costs.

```
rtmp://ingest-1.phenixrts.com:80/ingest
rtmp://ingest-2.phenixrts.com:80/ingest
```

## Stream Information:
The stream secret (SSSS)  and name (NNNN) will be provided to you separately.
They should be kept secret as this allows someone to stream to the app.

StreamKey: (be sure to add the highlighted part too)

```SSSSSSSS;capabilities=sd,multi-bitrate,origin-shield```

In the zender admin, you need to add the the stream via the Media/Creator section.
The Zender Media Video Url format is as follows: ```phenix:NNNN```

- sd = standard definition quality
- multi-bitrate = the player can switch quality depending on the bandwidth

## Debug/Test page:
You can use the following page to check if all necessary ports are open

<https://phenixrts.com/debugging/#/>


# Generating a stream using ffmpeg
For testing purposes it`s sometimes convenient to just stream file. Adapt the following script (example is for phenix streaming)

```shell
#!/bin/bash

# Specify a video file stream
# The following youtube video is a great test video for testing video & audio sync
# use youtube-dl to download
# See https://www.youtube.com/watch?v=ucZl6vQ_8Uo
VIDEO_FILE=sync.mkv

# font used to display the timestamp, required for it to work
# font can be downloaded at https://www.fontsquirrel.com/fonts/liberation-mono
FONT_FILE=LiberationMono-Bold.ttf
FONT_SIZE=70
FONT_COLOR=white

# Specify the phenix ingest key , matching the stream
STREAM_KEY=...yourkey..

# Options to pass to the streaming
# on-demand = also regular streaming
# uld,ld,sd,hd,uhd = limits the player to a certain output size
STREAM_OPTIONS=\;capabilities=sd,multi-bitrate,origin-shield,streaming,on-demand

# Ingest bit rate
INGEST_BITRATE=1M

# rotation of video
# Rotate
# https://stackoverflow.com/questions/3937387/rotating-videos-with-ffmpeg
#ROTATE_OPTION=-vf "transpose=1"

# IngestPoint
INGEST_POINT=ingest.phenixrts.com:80
#INGEST_POINT=ingest-1.phenixrts.com:80
#INGEST_POINT=ingest-2.phenixrts.com:80

STREAM_URL=rtmp://${INGEST_POINT}/ingest/${STREAM_KEY}


# -tune zerolatency removes all possible delay
# -vf drawtext .. adds a timestamp to the video
# -vf transpose=1 rotates the video 90 degrees

set -x
ffmpeg -stream_loop -1 -re -i ${VIDEO_FILE} \
    -tune zerolatency \
    -vcodec libx264 -vprofile baseline -g 30 -acodec aac -strict -2 -b:v ${INGEST_BITRATE} -maxrate ${INGEST_BITRATE} -bufsize ${INGEST_BITRATE} ${ROTATE_OPTION} \
    -vf drawtext="fontfile=${FONT_FILE}:text='%{localtime\:%T }':r=23.976:x=(w-tw)/2:y=h-(1*lh):fontcolor=${FONT_COLOR}:fontsize=${FONT_SIZE}:box=1:boxcolor=0x00000999" \
    -f flv "${STREAM_URL}${STREAM_OPTIONS}"

exit

```
