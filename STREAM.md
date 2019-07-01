# Zender Retrieve Stream information

Information about your stream is entered in the Zender Admin.
Sometimes you want to access this information and use it in your app (for example to list upcoming, past streams)

When you retrieve the streams there are two types:
- the lobby stream (will be there at all times, when there is no show)
- non-lobby stream or regular stream/episode

To make these request one needs an admin/API token (used as bearer-token).

As this has admin privileges these requests should be done from backend code;
And ideally cached, so not every user request results in a new API request.


# To retrieve all streams:
```
curl -XGET 'https://api.zender.tv/v1/channels/<channelId>' -H 'authorization: Bearer <bearerToken>' -H 'content-type: application/json' -H 'accept: application/json' | jq '.streams[]'

{
  "published": true,   <= is the stream public
  "state": "live",     <= state of the stream before , live , after 
  "lobby": false,      <= is the stream a lobby stream (in between streams) this field is optional)
  "airdate": "2018-04-09T19:41:00.000Z",
  "channelId": "3789b16d-8e9d-4071-9209-2dae67be3760",
  "userCount": 2,      <= number of users currently on the stream
  "description": "Quizzia ",
  "id": "f5cc622a-4239-40f9-9ee5-0d29374a4a72", <= unique streamId (not available for public if no yet published"
  "title": "Quizzia"
}
```

- To get the next stream information you need to sort by airdate and filter out the lobby stream
- To get the previous stream information you need to take the last airdate in the past

# To retrieve all upcoming/listed streams:
The previous API call retrieves all streams. Sometimes you only want to see the upcoming/listed streams.
A stream is explicitely marked as listed so it is visible to the audience. This can be used to make an overview of upcoming shows.


```
curl -XGET 'https://api.zender.tv/v1/channels/<channelId>/streams/listed?from=2010-06-25T08:21:55.505Z' -H 'authorization: Bearer <bearerToken>' -H 'content-type: application/json' -H 'accept: application/json' | jq '.streams[]'

{
  "published": true,   <= is the stream public
  "state": "live",     <= state of the stream before , live , after 
  "lobby": false,      <= is the stream a lobby stream (in between streams) this field is optional)
  "airdate": "2018-04-09T19:41:00.000Z",
  "channelId": "3789b16d-8e9d-4071-9209-2dae67be3760",
  "userCount": 2,      <= number of users currently on the stream
  "description": "Quizzia ",
  "id": "f5cc622a-4239-40f9-9ee5-0d29374a4a72", <= unique streamId (not available for public if no yet published"
  "title": "Quizzia"
}
```
