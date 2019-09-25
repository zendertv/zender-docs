
# Zender Public API

API documentation for all the Zender Microservices

## Indices

* [Admin/Core/Accounts](#admincoreaccounts)

  * [Admin Token Login](#1-admin-token-login)
  * [Create VIP Users](#2-create-vip-users)
  * [Create API token](#3-create-api-token)
  * [Get list of API token users](#4-get-list-of-api-token-users)
  * [Disable an api token](#5-disable-an-api-token)
  * [Update Admin User](#6-update-admin-user)
  * [Get Admin Avatar Image Upload Url](#7-get-admin-avatar-image-upload-url)
  * [Update Admin User Avatar](#8-update-admin-user-avatar)
  * [Get VIP Users for Stream](#9-get-vip-users-for-stream)

* [Admin/Core/Assets](#admincoreassets)

  * [Get Signed Upload Url](#1-get-signed-upload-url)
  * [Upload Asset](#2-upload-asset)

* [Admin/Core/Channels](#admincorechannels)

  * [Get Channels](#1-get-channels)
  * [Get Channel Preview Image Upload Url](#2-get-channel-preview-image-upload-url)
  * [Upload Channel Preview Image](#3-upload-channel-preview-image)
  * [Get Channel Icon Upload Url](#4-get-channel-icon-upload-url)
  * [Upload Channel Icon Image](#5-upload-channel-icon-image)
  * [Get Channel Header Image Upload Url](#6-get-channel-header-image-upload-url)
  * [Upload Channel Header Image](#7-upload-channel-header-image)
  * [Create Channel](#8-create-channel)
  * [Get Channel](#9-get-channel)
  * [Update Channel](#10-update-channel)
  * [Delete Channel](#11-delete-channel)

* [Admin/Core/Streams](#admincorestreams)

  * [Get Streams](#1-get-streams)
  * [Get Listed Streams](#2-get-listed-streams)
  * [Get Channel Preview Image Upload Url copy](#3-get-channel-preview-image-upload-url-copy)
  * [Upload Channel Preview Image copy](#4-upload-channel-preview-image-copy)
  * [Create Stream](#5-create-stream)
  * [Update Stream](#6-update-stream)
  * [Unpublish Stream](#7-unpublish-stream)
  * [Publish Stream](#8-publish-stream)
  * [Delete Stream](#9-delete-stream)
  * [SetState Stream](#10-setstate-stream)
  * [Get Stream Demo URL](#11-get-stream-demo-url)

* [Admin/Core/Users](#admincoreusers)

  * [Get Blocked Users](#1-get-blocked-users)
  * [Create External Users](#2-create-external-users)
  * [Update User](#3-update-user)
  * [Block User](#4-block-user)
  * [Unblock User](#5-unblock-user)
  * [TempBlock User](#6-tempblock-user)
  * [Update Username](#7-update-username)

* [Admin/Emojis](#adminemojis)

  * [Update Emojis Config](#1-update-emojis-config)
  * [Get Emojis Reactions](#2-get-emojis-reactions)
  * [Enable Emojis](#3-enable-emojis)
  * [Disable Emojis](#4-disable-emojis)
  * [Reset Emoji Count](#5-reset-emoji-count)
  * [Reset Avatar Count](#6-reset-avatar-count)

* [Admin/Media](#adminmedia)

  * [Get Media Content](#1-get-media-content)
  * [Create Media Content](#2-create-media-content)
  * [Update Media Content](#3-update-media-content)
  * [Trigger Media Content](#4-trigger-media-content)
  * [Delete Media Content](#5-delete-media-content)
  * [Get Media Config](#6-get-media-config)
  * [Update Media Config](#7-update-media-config)

* [Admin/Polls](#adminpolls)

  * [Get Polls](#1-get-polls)
  * [Update Polls Config](#2-update-polls-config)
  * [Create Poll](#3-create-poll)
  * [Get Poll](#4-get-poll)
  * [Get Poll results](#5-get-poll-results)
  * [Update Poll](#6-update-poll)
  * [Delete Poll](#7-delete-poll)
  * [Start Poll](#8-start-poll)
  * [Stop Poll](#9-stop-poll)

* [Admin/Quiz](#adminquiz)

  * [Get Quiz Config](#1-get-quiz-config)
  * [Create Quiz Config](#2-create-quiz-config)
  * [Update Quiz Config](#3-update-quiz-config)
  * [Create Quiz](#4-create-quiz)
  * [Update Quiz](#5-update-quiz)
  * [Get Quizzes](#6-get-quizzes)
  * [Get Quizzes for channel](#7-get-quizzes-for-channel)
  * [Get Quiz](#8-get-quiz)
  * [Create Question](#9-create-question)
  * [Update Question](#10-update-question)
  * [Delete Question](#11-delete-question)
  * [Start Quiz](#12-start-quiz)
  * [Launch Question](#13-launch-question)
  * [Broadcast Quiz Results](#14-broadcast-quiz-results)
  * [Retrieve Quiz Results](#15-retrieve-quiz-results)
  * [Stop Quiz](#16-stop-quiz)
  * [Reset Quiz](#17-reset-quiz)
  * [Delete Quiz](#18-delete-quiz)
  * [Clear Quiz Referrer code](#19-clear-quiz-referrer-code)
  * [Download quiz winners](#20-download-quiz-winners)
  * [Download quiz players](#21-download-quiz-players)
  * [Download quiz player stats](#22-download-quiz-player-stats)
  * [Increment extra lives (deprecated)](#23-increment-extra-lives-(deprecated))
  * [Increment extra lives](#24-increment-extra-lives)
  * [Set extra lives](#25-set-extra-lives)
  * [Get quiz statistics](#26-get-quiz-statistics)

* [Admin/Shoutbox](#adminshoutbox)

  * [Get Shoutbox Config](#1-get-shoutbox-config)
  * [Set Placeholder Shoutbox Config](#2-set-placeholder-shoutbox-config)
  * [Set Topic Shoutbox Config](#3-set-topic-shoutbox-config)
  * [Set Welcome Shoutbox Config copy](#4-set-welcome-shoutbox-config-copy)
  * [Enable Shoutbox](#5-enable-shoutbox)
  * [Disable Shoutbox](#6-disable-shoutbox)
  * [Update Shoutbox Config](#7-update-shoutbox-config)
  * [Get Shoutbox Messages](#8-get-shoutbox-messages)
  * [Send Shoutbox User Message](#9-send-shoutbox-user-message)
  * [Send Shoutbox System Message](#10-send-shoutbox-system-message)
  * [Update Shoutbox Message](#11-update-shoutbox-message)
  * [Trigger Shoutbox Message](#12-trigger-shoutbox-message)
  * [Delete Shoutbox Message](#13-delete-shoutbox-message)
  * [Export Shoutbox Messages](#14-export-shoutbox-messages)
  * [Update Shoutbox Profanity Filter](#15-update-shoutbox-profanity-filter)
  * [Delete All Shoutbox Messages](#16-delete-all-shoutbox-messages)

* [Player/Core](#playercore)

  * [Get Target](#1-get-target)
  * [Anonymous Token Login](#2-anonymous-token-login)
  * [Provider Token Login](#3-provider-token-login)
  * [Get Target Channels](#4-get-target-channels)
  * [Get Channel](#5-get-channel)
  * [Get Channel Streams](#6-get-channel-streams)
  * [Get Stream](#7-get-stream)
  * [Get Registered Devices](#8-get-registered-devices)
  * [Register Device](#9-register-device)
  * [Unregister Device](#10-unregister-device)
  * [Subscribe to Topic](#11-subscribe-to-topic)
  * [Unsubscribe from Topic](#12-unsubscribe-from-topic)
  * [Geo Check](#13-geo-check)
  * [Get Signed Upload Url](#14-get-signed-upload-url)
  * [Remove user data](#15-remove-user-data)

* [Player/Emojis](#playeremojis)

  * [Get Emojis Config](#1-get-emojis-config)
  * [Post Emojis](#2-post-emojis)
  * [Post Avatars](#3-post-avatars)

* [Player/Media](#playermedia)

  * [Get Media Config](#1-get-media-config)

* [Player/Polls](#playerpolls)

  * [Get Polls Config](#1-get-polls-config)
  * [Poll Vote](#2-poll-vote)

* [Player/Quiz](#playerquiz)

  * [Get Quiz Config](#1-get-quiz-config-1)
  * [Answer Question](#2-answer-question)
  * [Get Quiz Leaderboard Win](#3-get-quiz-leaderboard-win)
  * [Get Quiz Leaderboard Answer](#4-get-quiz-leaderboard-answer)
  * [Get Quiz Leaderboard User](#5-get-quiz-leaderboard-user)
  * [Set Quiz Referrer code](#6-set-quiz-referrer-code)
  * [Get Quiz Referrer code](#7-get-quiz-referrer-code)
  * [Redeem extra life on last question](#8-redeem-extra-life-on-last-question)
  * [Get extra lives](#9-get-extra-lives)

* [Player/Shoutbox](#playershoutbox)

  * [Get Shoutbox Config](#1-get-shoutbox-config-1)
  * [Get Shoutbox Messages](#2-get-shoutbox-messages)
  * [Send Shoutbox Message](#3-send-shoutbox-message)
  * [Delete Shoutbox Messages](#4-delete-shoutbox-messages)

* [Player/Teams](#playerteams)

  * [Create Team](#1-create-team)
  * [Get Team](#2-get-team)
  * [Update Team](#3-update-team)
  * [Delete Team](#4-delete-team)
  * [Join Team](#5-join-team)
  * [Leave Team](#6-leave-team)
  * [Delegate Team](#7-delegate-team)
  * [Remove Team Member](#8-remove-team-member)


--------


## Admin/Core/Accounts



### 1. Admin Token Login


Login by retrieving an admin bearer token.

The "userId" and "password" attributes in the request are mandatory.

All subsequent admin calls must send this bearer token in the "Authorization"-header.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/login
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "userId": "{{adminUser}}",
  "password": "{{adminPassword}}"
}
```



***Responses:***


Status: Admin Token Login (success) | Code: 200



```js
{"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T13:53:54.473Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T13:53:54.473Z"}}
```



Status: Admin Token Login (user not found) | Code: 404



```js
{"code":"NOT_FOUND","message":"User not found"}
```



### 2. Create VIP Users


A VIP user is a user that is associated with a stream and can be used by an admin user to impersonate this VIP user while shouting a message. See the "Send Shoutbox Message On Behalf Of" example of the [Send Shoutbox User Message](#fff94289-ecdf-4ee3-97bd-775444f55430) on how to use a VIP user.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/users/vip
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
[
	{
		"name": "Very Important Person",
		"avatar": "https://www.example.com/vip.jpg",
		"streamId": "28d150e5-c720-4cb8-b028-944b960cc756"
	}
]
```



***Responses:***


Status: Create VIP Users (validation error) | Code: 400



```js
{"code":"VALIDATION_ERROR","message":[{"selector":"name","tip":"name is mandatory."},{"selector":"avatar","tip":"avatar is mandatory."},{"selector":"streamId","tip":"streamId is mandatory."}]}
```



Status: Create VIP Users (success) | Code: 200



```js
[{"name":"Very Important Person","avatar":"https://www.example.com/vip.jpg","streamId":"28d150e5-c720-4cb8-b028-944b960cc756","targetId":"413b6c52-90c4-436c-8641-691afd7085d9","role":"admin","authenticated":true,"id":"d82f3ba5-0385-4fc0-ac2d-c04527163889","createdAt":"2018-02-12T10:58:48.159Z"}]
```



### 3. Create API token


An api token has the same rights as an admin user, but is intended for api access. Each programmatic access should use its own api token.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/apitokens
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 4. Get list of API token users


An api token has the same rights as an admin user, but is intended for api access. Each programmatic access should use its own api token.


***Endpoint:***

```bash
Method: GET
Type: RAW
URL: {{authApiHost}}/v1/auth/apitokens
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 5. Disable an api token


An api token has the same rights as an admin user, but is intended for api access. Each programmatic access should use its own api token.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{authApiHost}}/v1/auth/apitokens
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"tokenId": "apiUser_d92780eb-05d1-47cc-8265-a9180bb21a4e"
}
```



### 6. Update Admin User


Updates an admin user with the provided attributes given in the request. There is no limit to which attributes you can provide.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{adminUserId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "email": "someone@somewhereelse.com"
}
```



***Responses:***


Status: Update User (success) | Code: 200



```js
{"createdAt":"2017-12-04T09:20:28.722Z","role":"user","targetId":"57699178-7d3c-4954-9f6c-6df8e7a164f6","provider":{"name":"facebook","uid":"fb-uid-one"},"name":"one","externalId":"57699178-7d3c-4954-9f6c-6df8e7a164f6_fb-uid-one","avatar":"https://graph.fb.com/avatar/one.png","id":"04049544-5b8b-4f1c-aa6b-fe96d999264b","email":"someone@somewhere.com","updatedAt":"2017-12-04T09:20:56.501Z"}
```



### 7. Get Admin Avatar Image Upload Url



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":"{{$guid}}",
  "filename":"{{channelName}}-avatar-image.png"
}
```



### 8. Update Admin User Avatar



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{adminUserId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "avatar": "{{adminAvatarImageUrl}}"
}
```



***Responses:***


Status: Update User | Code: 200



```js
{"createdAt":"2017-12-04T09:20:28.722Z","role":"user","targetId":"57699178-7d3c-4954-9f6c-6df8e7a164f6","provider":{"name":"facebook","uid":"fb-uid-one"},"name":"one","externalId":"57699178-7d3c-4954-9f6c-6df8e7a164f6_fb-uid-one","avatar":"https://graph.fb.com/avatar/one.png","id":"04049544-5b8b-4f1c-aa6b-fe96d999264b","email":"someone@somewhere.com","updatedAt":"2017-12-04T09:20:56.501Z"}
```



### 9. Get VIP Users for Stream



***Endpoint:***

```bash
Method: GET
Type: 
URL: {{authApiHost}}/v1/auth/users
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| streamId | {{streamId}} |  |



***Responses:***


Status: Get VIP Users for Stream (success) | Code: 200



```js
[{"targetId":"413b6c52-90c4-436c-8641-691afd7085d9","authenticated":true,"avatar":"https://www.example.com/vip.jpg","role":"admin","createdAt":"2018-02-12T10:54:46.191Z","id":"ae41120f-5cc7-4045-b11f-9c67819ef111","name":"Very Important Person","streamId":"28d150e5-c720-4cb8-b028-944b960cc756"}]
```



## Admin/Core/Assets



### 1. Get Signed Upload Url


Get a signed upload url to send/upload asset files to. The uploadUrl in the response is only available for a short period after which it won't be possible to upload files to.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":1511863659392.595,
  "filename":"zender-logo.png"
}
```



***Responses:***


Status: Get Signed Upload Image Url (success) | Code: 200



```js
{
    "uploadId": "ac7a1d06-fb0f-410b-bdb0-3491ede17c01",
    "uploadUrl": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.original.png?AWSAccessKeyId=dummy&Content-Type=image%2Fpng&Expires=1511876958&Signature=RxO8nW3wKBZJHKUVLdHoFzUcUQk%3D&x-amz-acl=public-read&x-amz-meta-filename=zender-logo.png&x-amz-meta-id=ac7a1d06-fb0f-410b-bdb0-3491ede17c01&x-amz-meta-targetid=03013c55-9996-4735-bbff-e1405601346e&x-amz-meta-userid=zender-api&x-amz-meta-userrole=admin&x-amz-tagging=targetId%3D03013c55-9996-4735-bbff-e1405601346e%26targetName%3Dzender-api",
    "resizedUrls": {
        "large": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.large.png",
        "medium": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.medium.png",
        "small": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.small.png"
    },
    "contentType": "image/png",
    "getUrl": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.original.png"
}
```



Status: Get Signed Upload Video Url (success) | Code: 200



```js
{
    "uploadId": "ac7a1d06-fb0f-410b-bdb0-3491ede17c01",
    "uploadUrl": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.original.png?AWSAccessKeyId=dummy&Content-Type=image%2Fpng&Expires=1511876958&Signature=RxO8nW3wKBZJHKUVLdHoFzUcUQk%3D&x-amz-acl=public-read&x-amz-meta-filename=zender-logo.png&x-amz-meta-id=ac7a1d06-fb0f-410b-bdb0-3491ede17c01&x-amz-meta-targetid=03013c55-9996-4735-bbff-e1405601346e&x-amz-meta-userid=zender-api&x-amz-meta-userrole=admin&x-amz-tagging=targetId%3D03013c55-9996-4735-bbff-e1405601346e%26targetName%3Dzender-api",
    "resizedUrls": {
        "large": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.large.png",
        "medium": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.medium.png",
        "small": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.small.png"
    },
    "contentType": "image/png",
    "getUrl": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/ac7a1d06-fb0f-410b-bdb0-3491ede17c01.original.png"
}
```



### 2. Upload Asset


Upload an asset file to a uploadUrl obtained from the "Get Signed Upload Url" endpoint.


***Endpoint:***

```bash
Method: PUT
Type: FILE
URL: {{uploadUrl}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | image/png |  |



***Responses:***


Status: Upload Video Asset | Code: 200



Status: Upload Image Asset | Code: 200



## Admin/Core/Channels



### 1. Get Channels


Get a channel.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Channel | Code: 200



```js
{"stories":[],"preview":{"width":579,"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580},"headerColor":"#B93D87","createdAt":"2017-11-28T13:54:56.714Z","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","headerImage":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","name":"Zender Api Channel","icon":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","iconColor":"#B93D87","id":"67b5528a-baf4-41bc-b558-b36613ee14a4","type":"streams","streams":[],"config":{"auth":{"login":{"url":"http://localhost:3002/v1/auth/login"},"providers":{"youtube":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"google":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"facebook":{"enabled":true,"appId":690051904495300,"tokenUrl":"https://graph.facebook.com/me"}}},"pusher":{"config":{"encrypted":true,"cluster":"eu","authEndpoint":"http://localhost:3002/v1/pusher"},"key":"968089f2292502112add"},"streams":{"url":"http://localhost:3001/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams"},"stories":{"url":"http://localhost:3007/v1/stories/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/stories"}}}
```



### 2. Get Channel Preview Image Upload Url



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":"{{$guid}}",
  "filename":"{{channelName}}-preview-image.png"
}
```



### 3. Upload Channel Preview Image



***Endpoint:***

```bash
Method: PUT
Type: FILE
URL: {{channelPreviewImageUploadUrl}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | image/png |  |



### 4. Get Channel Icon Upload Url



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":"{{$guid}}",
  "filename":"{{channelName}}-icon-image.png"
}
```



### 5. Upload Channel Icon Image



***Endpoint:***

```bash
Method: PUT
Type: FILE
URL: {{channelIconImageUploadUrl}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | image/png |  |



### 6. Get Channel Header Image Upload Url



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":"{{$guid}}",
  "filename":"{{channelName}}-header-image.png"
}
```



### 7. Upload Channel Header Image



***Endpoint:***

```bash
Method: PUT
Type: FILE
URL: {{channelHeaderImageUploadUrl}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | image/png |  |



### 8. Create Channel


Create a new channel.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/channels
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "name":"{{channelName}}",
  "type":"streams",
  "preview": {
    "width":579,
    "height":580,
    "type":"image",
    "url":"{{channelPreviewImageUrl}}"
    
  },
  "headerImage":"{{channelHeaderImageUrl}}",
  "headerColor":"#000000",
  "icon":"{{channelIconImageUrl}}",
  "iconColor":"#000000"
}
```



***Responses:***


Status: Create Channel | Code: 200



```js
{"stories":[],"preview":{"width":579,"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580},"headerColor":"#B93D87","createdAt":"2017-11-28T13:54:56.714Z","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","headerImage":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","name":"Zender Api Channel","icon":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","iconColor":"#B93D87","id":"67b5528a-baf4-41bc-b558-b36613ee14a4","type":"streams","streams":[],"config":{"auth":{"login":{"url":"http://localhost:3002/v1/auth/login"},"providers":{"youtube":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"google":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"facebook":{"enabled":true,"appId":690051904495300,"tokenUrl":"https://graph.facebook.com/me"}}},"pusher":{"config":{"encrypted":true,"cluster":"eu","authEndpoint":"http://localhost:3002/v1/pusher"},"key":"968089f2292502112add"},"streams":{"url":"http://localhost:3001/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams"},"stories":{"url":"http://localhost:3007/v1/stories/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/stories"}}}
```



### 9. Get Channel


Get a channel.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Channel | Code: 200



```js
{"stories":[],"preview":{"width":579,"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580},"headerColor":"#B93D87","createdAt":"2017-11-28T13:54:56.714Z","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","headerImage":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","name":"Zender Api Channel","icon":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","iconColor":"#B93D87","id":"67b5528a-baf4-41bc-b558-b36613ee14a4","type":"streams","streams":[],"config":{"auth":{"login":{"url":"http://localhost:3002/v1/auth/login"},"providers":{"youtube":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"google":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"facebook":{"enabled":true,"appId":690051904495300,"tokenUrl":"https://graph.facebook.com/me"}}},"pusher":{"config":{"encrypted":true,"cluster":"eu","authEndpoint":"http://localhost:3002/v1/pusher"},"key":"968089f2292502112add"},"streams":{"url":"http://localhost:3001/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams"},"stories":{"url":"http://localhost:3007/v1/stories/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/stories"}}}
```



### 10. Update Channel


Update a channel.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "name":"{{channelName}}",
  "type":"streams",
  "preview": {
    "width":579,
    "height":580,
    "type":"image",
    "url":"{{channelPreviewImageUrl}}"
    
  },
  "headerImage":"{{channelHeaderImageUrl}}",
  "headerColor":"#000000",
  "icon":"{{channelIconUrl}}",
  "iconColor":"#000000"
}
```



***Responses:***


Status: Update Channel | Code: 200



```js
{"stories":[],"preview":{"width":579,"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580},"createdAt":"2017-11-28T13:54:56.714Z","headerColor":"#000000","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","headerImage":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","icon":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","iconColor":"#000000","name":"Zender Api Channel Update","id":"67b5528a-baf4-41bc-b558-b36613ee14a4","type":"streams","updatedAt":"2017-11-28T13:55:16.192Z","streams":[],"config":{"auth":{"login":{"url":"http://localhost:3002/v1/auth/login"},"providers":{"youtube":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"google":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"facebook":{"enabled":true,"appId":690051904495300,"tokenUrl":"https://graph.facebook.com/me"}}},"pusher":{"config":{"encrypted":true,"cluster":"eu","authEndpoint":"http://localhost:3002/v1/pusher"},"key":"968089f2292502112add"},"streams":{"url":"http://localhost:3001/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams"},"stories":{"url":"http://localhost:3007/v1/stories/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/stories"}}}
```



### 11. Delete Channel


Delete a channel.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



## Admin/Core/Streams



### 1. Get Streams


Update a stream.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 2. Get Listed Streams


Get all the listed streams with an airdate that lies in the future. Lobby streams will not be returned from this endpoint, neither streams that were marked as "listed: false". The id's of the streams will not be returned unless you call this endpoint with admin priviliges. You can also filter the streams by its status ('before', 'live' or 'after'). When the "from" param is not provided in the request only streams with future airdates will be returned.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/listed
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| from | 2010-06-25T08:21:55.505Z |  |



***Responses:***


Status: Get Listed Streams Success | Code: 200



```js
[
    {
        "preview": {
            "type": "image",
            "url": "https://s3-eu-west-1.amazonaws.com/cdn.staging.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-06-25/792ccdff-e4e8-47cd-bb73-ded58a8f582a.original.png"
        },
        "airdate": "2018-06-25T12:41:00.000Z",
        "published": false,
        "state": "live",
        "title": "Test Phenix",
        "description": "Test Phenix"
    }
]
```



Status: Get Listed Streams Channel Not Found | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "Could not find targetId for channel: <channel-id>"
}
```



### 3. Get Channel Preview Image Upload Url copy



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "id":"{{$guid}}",
  "filename":"{{channelName}}-preview-image.png"
}
```



### 4. Upload Channel Preview Image copy



***Endpoint:***

```bash
Method: PUT
Type: FILE
URL: {{streamPreviewImageUploadUrl}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | image/png |  |



### 5. Create Stream


Create a stream for a channel.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "title":"{{channelName}}",
  "custom":{
    "splash_enabled":false,
    "splash_loginrequired":true,
    "splash_url":"http://zender.tv"
  },
  "description":"{{channelName}} Stream",
  "preview": {
    "type":"image",
    "url":"{{streamPreviewImageUrl}}"
  },
  "airdate":"2017-11-27T10:30:00.000Z",
  "state":"before",
  "interactions":["media","shoutbox","emojis","polls"],
  "lobby": false,
  "listed": true
}
```



***Responses:***


Status: Create Stream | Code: 200



```js
{"title":"Zender API Stream","custom":{"splash_enabled":true,"splash_loginrequired":true,"splash_url":"http://zender.tv"},"description":"Zender API Stream","preview":{"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"airdate":"2017-11-27T10:30:00.000Z","state":"before","interactions":{"media":{"pusher":{"channel":"stream-a2993350-cb51-437d-bf39-41e110a71f5a-media"},"endpoint":"http://192.168.0.169:3003/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/media"},"shoutbox":{"pusher":{"channel":"stream-a2993350-cb51-437d-bf39-41e110a71f5a-shoutbox"},"endpoint":"http://192.168.0.169:3004/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/shoutbox"},"emojis":{"pusher":{"channel":"stream-a2993350-cb51-437d-bf39-41e110a71f5a-emojis"},"endpoint":"http://192.168.0.169:3005/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/emojis"},"polls":{"pusher":{"channel":"stream-a2993350-cb51-437d-bf39-41e110a71f5a-polls"},"endpoint":"http://192.168.0.169:3006/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/polls"}},"channelId":"67b5528a-baf4-41bc-b558-b36613ee14a4","id":"a2993350-cb51-437d-bf39-41e110a71f5a","createdAt":"2017-11-28T13:55:31.569Z","lobby": false,"listed": true}
```



### 6. Update Stream


Update a stream.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"title":"Zender API Stream Update",
	"custom":{
		"splash_enabled": true,
		"splash_loginrequired": false,
		"splash_url": "http://zender.tv"
	},
	"description":"Zender API Stream Update",
	"preview": {
		"type": "image",
		"url": "{{getUrl}}"
	},
	"airdate": "2017-11-27T10:30:00.000Z",
	"state": "live",
	"published": true,
	"lobby": true
}
```



### 7. Unpublish Stream


Update a stream.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "published": false
}
```



***Responses:***


Status: Update Stream | Code: 200



```js
{"preview":{"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/6543fcdc-b272-4569-bba0-dd609a65fb29.original.png"},"createdAt":"2017-11-28T10:38:44.210Z","airdate":"2017-11-27T10:30:00.000Z","custom":{"splash_enabled":true,"splash_url":"http://zender.tv","splash_loginrequired":false},"description":"Zender API Stream Update","published":false,"id":"f4a89037-58ba-41f1-82fa-3e5e83cfdf6e","state":"live","title":"Zender API Stream Update","channelId":"94a22170-712c-4c6f-b31e-febe86aeafc2","interactions":{"media":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-media"},"endpoint":"http://192.168.0.169:3003/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/media"},"shoutbox":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-shoutbox"},"endpoint":"http://192.168.0.169:3004/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/shoutbox"},"emojis":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-emojis"},"endpoint":"http://192.168.0.169:3005/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/emojis"},"polls":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-polls"},"endpoint":"http://192.168.0.169:3006/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/polls"}},"updatedAt":"2017-11-28T10:41:20.753Z"}
```



Status: Publish Stream | Code: 200



```js
{
    "published": true
}
```



Status: Unpublish Stream | Code: 200



```js
{
    "published": false,
}
```



### 8. Publish Stream


Update a stream.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "published": true
}
```



***Responses:***


Status: Update Stream | Code: 200



```js
{"preview":{"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/6543fcdc-b272-4569-bba0-dd609a65fb29.original.png"},"createdAt":"2017-11-28T10:38:44.210Z","airdate":"2017-11-27T10:30:00.000Z","custom":{"splash_enabled":true,"splash_url":"http://zender.tv","splash_loginrequired":false},"description":"Zender API Stream Update","published":false,"id":"f4a89037-58ba-41f1-82fa-3e5e83cfdf6e","state":"live","title":"Zender API Stream Update","channelId":"94a22170-712c-4c6f-b31e-febe86aeafc2","interactions":{"media":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-media"},"endpoint":"http://192.168.0.169:3003/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/media"},"shoutbox":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-shoutbox"},"endpoint":"http://192.168.0.169:3004/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/shoutbox"},"emojis":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-emojis"},"endpoint":"http://192.168.0.169:3005/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/emojis"},"polls":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-polls"},"endpoint":"http://192.168.0.169:3006/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/polls"}},"updatedAt":"2017-11-28T10:41:20.753Z"}
```



Status: Publish Stream | Code: 200



```js
{
    "published": true
}
```



Status: Unpublish Stream | Code: 200



```js
{
    "published": false,
}
```



### 9. Delete Stream


Delete a stream.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 10. SetState Stream


Update a stream.

- `before`:
- `live`:
- `after`:


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
    "state": "live"
}
```



***Responses:***


Status: Unpublish Stream | Code: 200



```js
{
    "published": false,
}
```



Status: Update Stream | Code: 200



```js
{"preview":{"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/6543fcdc-b272-4569-bba0-dd609a65fb29.original.png"},"createdAt":"2017-11-28T10:38:44.210Z","airdate":"2017-11-27T10:30:00.000Z","custom":{"splash_enabled":true,"splash_url":"http://zender.tv","splash_loginrequired":false},"description":"Zender API Stream Update","published":false,"id":"f4a89037-58ba-41f1-82fa-3e5e83cfdf6e","state":"live","title":"Zender API Stream Update","channelId":"94a22170-712c-4c6f-b31e-febe86aeafc2","interactions":{"media":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-media"},"endpoint":"http://192.168.0.169:3003/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/media"},"shoutbox":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-shoutbox"},"endpoint":"http://192.168.0.169:3004/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/shoutbox"},"emojis":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-emojis"},"endpoint":"http://192.168.0.169:3005/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/emojis"},"polls":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-polls"},"endpoint":"http://192.168.0.169:3006/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/polls"}},"updatedAt":"2017-11-28T10:41:20.753Z"}
```



Status: Publish Stream | Code: 200



```js
{
    "published": true
}
```



### 11. Get Stream Demo URL


Update a stream.

- `before`:
- `live`:
- `after`:


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/demo
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Publish Stream | Code: 200



```js
{
    "published": true
}
```



Status: Unpublish Stream | Code: 200



```js
{
    "published": false,
}
```



Status: Update Stream | Code: 200



```js
{"preview":{"type":"image","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/6543fcdc-b272-4569-bba0-dd609a65fb29.original.png"},"createdAt":"2017-11-28T10:38:44.210Z","airdate":"2017-11-27T10:30:00.000Z","custom":{"splash_enabled":true,"splash_url":"http://zender.tv","splash_loginrequired":false},"description":"Zender API Stream Update","published":false,"id":"f4a89037-58ba-41f1-82fa-3e5e83cfdf6e","state":"live","title":"Zender API Stream Update","channelId":"94a22170-712c-4c6f-b31e-febe86aeafc2","interactions":{"media":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-media"},"endpoint":"http://192.168.0.169:3003/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/media"},"shoutbox":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-shoutbox"},"endpoint":"http://192.168.0.169:3004/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/shoutbox"},"emojis":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-emojis"},"endpoint":"http://192.168.0.169:3005/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/emojis"},"polls":{"pusher":{"channel":"stream-f4a89037-58ba-41f1-82fa-3e5e83cfdf6e-polls"},"endpoint":"http://192.168.0.169:3006/v1/channels/94a22170-712c-4c6f-b31e-febe86aeafc2/streams/f4a89037-58ba-41f1-82fa-3e5e83cfdf6e/polls"}},"updatedAt":"2017-11-28T10:41:20.753Z"}
```



## Admin/Core/Users



### 1. Get Blocked Users


Get all users.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{authApiHost}}/v1/auth/users
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| flag | blocked |  |



***Responses:***


Status: Get Blocked Users | Code: 200



```js
[{"authenticated":true,"createdAt":"2017-11-28T14:48:42.879Z","flag":"blocked_2017-11-28T15:27:06.362Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook"},"externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_undefined","avatar":"https://graph.facebook.com/undefined/picture?width=250&type=square","id":"f468fca3-1287-4858-880f-7c099e0ba1d3","updatedAt":"2017-11-28T15:27:06.362Z"}]
```



### 2. Create External Users


Create multiple external users that can be used to shout on behalf of: see "Send Shoutbox Message On Behalf Of" example.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/users
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
[
	{
		"provider": {
			"uid": "fb-uid-one",
			"name": "facebook"
		},
		"name": "one",
		"avatar": "https://graph.fb.com/avatar/one.png"
	},
	{
		"provider": {
			"uid": "fb-uid-two",
			"name": "facebook"
		},
		"name": "two",
		"avatar": "https://graph.fb.com/avatar/two.png"
	},
	{
		"provider": {
			"uid": "fb-uid-three",
			"name": "facebook"
		},
		"name": "three",
		"avatar": "https://graph.fb.com/avatar/three.png"
	}
]
```



***Responses:***


Status: Create External Users | Code: 200



```js
[{"provider":{"uid":"fb-uid-one","name":"facebook"},"name":"one","avatar":"https://graph.fb.com/avatar/one.png","targetId":"04573ba9-3efb-402f-b956-9a0f1cfeb285","externalId":"04573ba9-3efb-402f-b956-9a0f1cfeb285_fb-uid-one","id":"9f7ae72e-0781-404c-baaa-160f91045504","createdAt":"2017-12-01T09:14:45.129Z","role":"user"},{"provider":{"uid":"fb-uid-two","name":"facebook"},"name":"two","avatar":"https://graph.fb.com/avatar/two.png","targetId":"04573ba9-3efb-402f-b956-9a0f1cfeb285","externalId":"04573ba9-3efb-402f-b956-9a0f1cfeb285_fb-uid-two","id":"eba4ae9c-354d-4220-9986-ffeda100d319","createdAt":"2017-12-01T09:14:45.137Z","role":"user"}]
```



### 3. Update User


Create multiple external users that can be used to shout on behalf of: see "Send Shoutbox Message On Behalf Of" example.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{externalUserId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"email": "someone@somewhere.com"
}
```



***Responses:***


Status: Update User | Code: 200



```js
{"createdAt":"2017-12-04T09:20:28.722Z","role":"user","targetId":"57699178-7d3c-4954-9f6c-6df8e7a164f6","provider":{"name":"facebook","uid":"fb-uid-one"},"name":"one","externalId":"57699178-7d3c-4954-9f6c-6df8e7a164f6_fb-uid-one","avatar":"https://graph.fb.com/avatar/one.png","id":"04049544-5b8b-4f1c-aa6b-fe96d999264b","email":"someone@somewhere.com","updatedAt":"2017-12-04T09:20:56.501Z"}
```



### 4. Block User


Blocks a user.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{userId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "flag": "blocked"
}
```



***Responses:***


Status: Unblock User | Code: 200



```js
{
    "authenticated": true,
    "createdAt": "2017-11-29T08:33:42.090Z",
    "flag": "unblocked_2017-11-29T08:38:57.865Z",
    "role": "user",
    "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
    "provider": {
        "name": "facebook",
        "uid": "1459394774070695"
    },
    "name": "Benoit Shapiro",
    "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695",
    "avatar": "https://graph.facebook.com/1459394774070695/picture?width=250&type=square",
    "id": "8184fbdc-6861-4fc5-9944-e7860b95f4df",
    "updatedAt": "2017-11-29T08:38:26.907Z"
}
```



Status: Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"blocked_2017-11-29T08:38:06.761Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T08:38:06.761Z"}
```



Status: Temporary Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"tmpblocked_2017-11-29T10:12:05.879Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T10:12:05.879Z"}
```



### 5. Unblock User


Blocks a user.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{userId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "flag": "unblocked"
}
```



***Responses:***


Status: Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"blocked_2017-11-29T08:38:06.761Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T08:38:06.761Z"}
```



Status: Temporary Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"tmpblocked_2017-11-29T10:12:05.879Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T10:12:05.879Z"}
```



Status: Unblock User | Code: 200



```js
{
    "authenticated": true,
    "createdAt": "2017-11-29T08:33:42.090Z",
    "flag": "unblocked_2017-11-29T08:38:57.865Z",
    "role": "user",
    "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
    "provider": {
        "name": "facebook",
        "uid": "1459394774070695"
    },
    "name": "Benoit Shapiro",
    "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695",
    "avatar": "https://graph.facebook.com/1459394774070695/picture?width=250&type=square",
    "id": "8184fbdc-6861-4fc5-9944-e7860b95f4df",
    "updatedAt": "2017-11-29T08:38:26.907Z"
}
```



### 6. TempBlock User


Blocks a user.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{userId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "flag": "tmpblocked"
}
```



***Responses:***


Status: Temporary Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"tmpblocked_2017-11-29T10:12:05.879Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T10:12:05.879Z"}
```



Status: Unblock User | Code: 200



```js
{
    "authenticated": true,
    "createdAt": "2017-11-29T08:33:42.090Z",
    "flag": "unblocked_2017-11-29T08:38:57.865Z",
    "role": "user",
    "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
    "provider": {
        "name": "facebook",
        "uid": "1459394774070695"
    },
    "name": "Benoit Shapiro",
    "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695",
    "avatar": "https://graph.facebook.com/1459394774070695/picture?width=250&type=square",
    "id": "8184fbdc-6861-4fc5-9944-e7860b95f4df",
    "updatedAt": "2017-11-29T08:38:26.907Z"
}
```



Status: Block User | Code: 200



```js
{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"blocked_2017-11-29T08:38:06.761Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T08:38:06.761Z"}
```

### 7. Update username


Blocks a user.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{authApiHost}}/v1/auth/users/{{externalUserId}}/username
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "username": "abcde"
}
```



***Responses:***


Status: Update User | Code: 200



```js
{"createdAt":"2017-12-04T09:20:28.722Z","role":"user","targetId":"57699178-7d3c-4954-9f6c-6df8e7a164f6","provider":{"name":"facebook","uid":"fb-uid-one"},"name":"one","externalId":"57699178-7d3c-4954-9f6c-6df8e7a164f6_fb-uid-one","avatar":"https://graph.fb.com/avatar/one.png","id":"04049544-5b8b-4f1c-aa6b-fe96d999264b","email":"someone@somewhere.com","updatedAt":"2017-12-04T09:20:56.501Z", "username": "abcde"}
```

## Admin/Emojis



### 1. Update Emojis Config


Update the emojis config of a stream. When creating a stream it will automatically create an emojis config.

- `sortedSets`:
- `enabled`: enables sending emojis


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": true,
  "sortedSets": [
    {
      "title": "Zender API Emoji Set",
      "emojis": [
        {
          "id": "73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
          "title": "73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
        },
        {
          "id": "560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
          "title": "560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/560527f8-4319-4021-a522-9b4ad0aecad5.original.png"
        },
        {
          "id": "26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
          "title": "26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
      },
      "type": "custom",
      "enabled": true
    },
    {
      "emojis": [
        {
          "title": "000-gezichten__smile01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png"
        },
        {
          "title": "000-gezichten__smile02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/b1554f8c-a099-4146-bb72-74e65524ac71.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/b1554f8c-a099-4146-bb72-74e65524ac71.original.png"
        },
        {
          "title": "000-gezichten__smile03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a3920971-0169-41d8-b5c7-b1a5e4ebd853.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a3920971-0169-41d8-b5c7-b1a5e4ebd853.original.png"
        },
        {
          "title": "000-gezichten__smile04",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5734048c-d83b-4941-8bd6-797658274424.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5734048c-d83b-4941-8bd6-797658274424.original.png"
        },
        {
          "title": "000-gezichten__smile05",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5badba92-e650-4223-ba18-87585e1e07a6.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5badba92-e650-4223-ba18-87585e1e07a6.original.png"
        },
        {
          "title": "000-gezichten__smile06",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/3e93bc03-5c51-452a-a4ca-bd6e2121bcce.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/3e93bc03-5c51-452a-a4ca-bd6e2121bcce.original.png"
        },
        {
          "title": "000-gezichten__smile07",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73eb9ba8-a9f2-465d-882d-cf29d6349029.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73eb9ba8-a9f2-465d-882d-cf29d6349029.original.png"
        },
        {
          "title": "000-gezichten__smile08",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/cab89d89-67a6-4ec8-ab06-3fecee8c9d8d.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/cab89d89-67a6-4ec8-ab06-3fecee8c9d8d.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png"
      },
      "id": "7b3f2436-dae0-45cf-aad2-4320cd342640",
      "title": "000-faces"
    },
    {
      "emojis": [
        {
          "title": "001-handen__hand01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png"
        },
        {
          "title": "001-handen__hand02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/655e92a4-5d18-47ab-9cf6-e39c2cb4babf.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/655e92a4-5d18-47ab-9cf6-e39c2cb4babf.original.png"
        },
        {
          "title": "001-handen__hand03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/1b7fe938-d774-474c-a194-d3dd1fb865a8.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/1b7fe938-d774-474c-a194-d3dd1fb865a8.original.png"
        },
        {
          "title": "001-handen__hand04",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/e31906f3-e6be-4fb8-a902-5c07de7707bf.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/e31906f3-e6be-4fb8-a902-5c07de7707bf.original.png"
        },
        {
          "title": "001-handen__hand05",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9308dd80-b525-4313-9bff-7f602fbb9435.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9308dd80-b525-4313-9bff-7f602fbb9435.original.png"
        },
        {
          "title": "001-handen__hand06",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/957a5877-94a9-45c5-94b4-26c6e71c7b5d.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/957a5877-94a9-45c5-94b4-26c6e71c7b5d.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png"
      },
      "id": "4775a542-bc43-4ce6-bf43-27a0fa7acc78",
      "title": "001-hands"
    },
    {
      "emojis": [
        {
          "title": "002-liefde__love01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png"
        },
        {
          "title": "002-liefde__love02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f2730bd7-aa84-4027-baae-0bfbc5a2e065.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f2730bd7-aa84-4027-baae-0bfbc5a2e065.original.png"
        },
        {
          "title": "002-liefde__love03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/18801fe1-bc93-4673-ac7a-e5de23677fd8.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/18801fe1-bc93-4673-ac7a-e5de23677fd8.original.png"
        },
        {
          "title": "002-liefde__love04",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f1ad0ac7-6e89-47cd-8af4-880dbf344dd5.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f1ad0ac7-6e89-47cd-8af4-880dbf344dd5.original.png"
        },
        {
          "title": "002-liefde__love05",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/4bcf20b5-237c-48e1-864c-acd5e0a736fe.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/4bcf20b5-237c-48e1-864c-acd5e0a736fe.original.png"
        },
        {
          "title": "002-liefde__love06",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/bc9b218a-2170-4aba-aeea-efb777ff15d3.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/bc9b218a-2170-4aba-aeea-efb777ff15d3.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png"
      },
      "id": "5b9dab91-f96d-4b60-a612-39a2ef567077",
      "title": "002-love"
    },
    {
      "emojis": [
        {
          "title": "003-dieren__a-bunny",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png"
        },
        {
          "title": "003-dieren__a-cat01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2cd7d92f-ebff-4bb3-b4cd-eca611443244.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2cd7d92f-ebff-4bb3-b4cd-eca611443244.original.png"
        },
        {
          "title": "003-dieren__a-cat02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/c6e365e5-5cde-410f-b036-9a5970ec3aa6.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/c6e365e5-5cde-410f-b036-9a5970ec3aa6.original.png"
        },
        {
          "title": "003-dieren__a-cat03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/97d6ef27-1be6-4071-9f19-b613b24d553e.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/97d6ef27-1be6-4071-9f19-b613b24d553e.original.png"
        },
        {
          "title": "003-dieren__a-cat04",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f64293a2-a7c1-42d8-a62c-5b303617b2df.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f64293a2-a7c1-42d8-a62c-5b303617b2df.original.png"
        },
        {
          "title": "003-dieren__a-chicken",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/caf5e45c-fe08-4740-b5ff-7e160d88cc4e.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/caf5e45c-fe08-4740-b5ff-7e160d88cc4e.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png"
      },
      "id": "ed93d548-63a7-4729-bec8-8fe9cbda2dd5",
      "title": "003-animals"
    },
    {
      "emojis": [
        {
          "title": "004-sport__s-ball",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png"
        },
        {
          "title": "004-sport__s-bike",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/0a13262d-501f-42d8-82d5-5e9026d32998.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/0a13262d-501f-42d8-82d5-5e9026d32998.original.png"
        },
        {
          "title": "004-sport__basebal",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9350eeba-6228-44ea-ae85-ac13e261e6b3.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9350eeba-6228-44ea-ae85-ac13e261e6b3.original.png"
        },
        {
          "title": "004-sport__basketbal",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f5b3882c-af2d-4b3c-a4fe-b2cdae5f6d86.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f5b3882c-af2d-4b3c-a4fe-b2cdae5f6d86.original.png"
        },
        {
          "title": "004-sport__fiets",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/882e4699-f171-4b1b-aaad-c410d210d6a3.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/882e4699-f171-4b1b-aaad-c410d210d6a3.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png"
      },
      "id": "30ae1d2f-dbec-4069-93cc-0bc4352d25eb",
      "title": "004-sport"
    },
    {
      "emojis": [
        {
          "title": "005-objecten__a-food01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png"
        },
        {
          "title": "005-objecten__a-food02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7452ce3e-0112-4f85-b2e2-f17de5d52190.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7452ce3e-0112-4f85-b2e2-f17de5d52190.original.png"
        },
        {
          "title": "005-objecten__a-food03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2994ab4a-f49e-4e03-9c23-64067e629e51.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2994ab4a-f49e-4e03-9c23-64067e629e51.original.png"
        },
        {
          "title": "005-objecten__a-food04",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/43d445f0-02b1-4cde-9eb6-91b1d2267711.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/43d445f0-02b1-4cde-9eb6-91b1d2267711.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png"
      },
      "id": "800e75aa-16e3-4d32-aaa8-b20bc9682c98",
      "title": "005-objects"
    },
    {
      "emojis": [
        {
          "title": "005-weer__a-weer01",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png"
        },
        {
          "title": "005-weer__a-weer02",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a47dbf95-6268-4a19-ad47-2e0f86229f32.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a47dbf95-6268-4a19-ad47-2e0f86229f32.original.png"
        },
        {
          "title": "005-weer__a-weer03",
          "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/61689c10-f4be-4a14-a1cb-b9c2f041ee1a.original.png",
          "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/61689c10-f4be-4a14-a1cb-b9c2f041ee1a.original.png"
        }
      ],
      "icon": {
        "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png"
      },
      "id": "737178d3-a13b-4b44-af2c-04f9a4b69475",
      "title": "005-weather"
    }
  ]
}
```



***Responses:***


Status: Enable Emojis | Code: 200



Status: Disable Emojis | Code: 200



### 2. Get Emojis Reactions


Gets the total of the allowed emojis.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/reactions
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 3. Enable Emojis


Update the emojis config of a stream. When creating a stream it will automatically create an emojis config.

- `sortedSets`:
- `enabled`: enables sending emojis


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": true
}
```



***Responses:***


Status: Disable Emojis | Code: 200



Status: Create and Sort Emoji Sets | Code: 200



Status: Enable Emojis | Code: 200



### 4. Disable Emojis


Update the emojis config of a stream. When creating a stream it will automatically create an emojis config.

- `sortedSets`:
- `enabled`: enables sending emojis


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": false
}
```



***Responses:***


Status: Disable Emojis | Code: 200



Status: Enable Emojis | Code: 200



Status: Create and Sort Emoji Sets | Code: 200



### 5. Reset Emoji Count


Delete a poll.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/reactions
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 6. Reset Avatar Count


Delete a poll.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/avatars
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



## Admin/Media



### 1. Get Media Content


Update the media config of a stream. When creating a stream it will automatically create a media config.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Update Media Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.739Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-28T13:57:21.427Z"}
```



### 2. Create Media Content


Create a new media content item.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "routing": "player",
  "title": "Zender API Media Pancarte",
  "description": "Zender API Media Pancarte",
  "view": {
    "image": {
      "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
    },
    "video": {
      "loop": true,
      "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.original.mp4",
      "alternativeUrls": [
      	"http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.alternative.mp4"
      ],
      "allowedRegions": "BE"
    }
  }
}
```



***Responses:***


Status: Create Image Media for Studio | Code: 200



```js
{
    "routing": "studio",
    "title": "Zender API Media Pancarte",
    "description": "Zender API Media Pancarte",
    "view": {
        "image": {
            "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
        }
    },
    "id": "80f0fe65-ae45-43d9-a1f5-5ad7fbd7fbf7",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "createdAt": "2017-11-28T13:58:08.400Z"
}
```



Status: Create Geoblocked Video Media for Player | Code: 200



```js
{
    "routing": "player",
    "title": "Zender API Media Pancarte",
    "description": "Zender API Media Pancarte",
    "view": {
        "image": {
            "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
        },
        "video": {
            "autoplay": true,
            "aspectRatio": "16:9",
            "loop": true,
            "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.original.mp4",
            "allowedRegions": "BE"
        }
    },
    "id": "49a2328f-3759-44bf-8499-f0e2601efee7",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "createdAt": "2017-11-28T13:57:42.399Z"
}
```



### 3. Update Media Content


Update a media content item.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/{{mediaContentId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "routing": "studio",
  "view": {
    "image": {
      "url": "{{getUrl}}"
    },
    "video": {
      "autoplay": true,
      "aspectRatio": "16:9",
      "loop": false,
      "url": "http://localhost:14569/cdn.local.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.original.mp4"
    }
  },
  "description": "Zender API Media Pancarte Update",
  "title": "Zender API Media Pancarte Update"
}
```



### 4. Trigger Media Content


Trigger a media content item to either the public player or the studio visualization (the "routing" attribute on the media content item decides where the item will be triggered).


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/{{mediaContentId}}/trigger
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 5. Delete Media Content


Delete a media content item.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/{{mediaContentId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 6. Get Media Config


Update the media config of a stream. When creating a stream it will automatically create a media config.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Update Media Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.739Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-28T13:57:21.427Z"}
```



### 7. Update Media Config


Update the media config of a stream. When creating a stream it will automatically create a media config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  
}
```



***Responses:***


Status: Update Media Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.739Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-28T13:57:21.427Z"}
```



## Admin/Polls



### 1. Get Polls


Create a poll.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Create Poll | Code: 200



```js
{"realtimeResults":true,"showResults":true,"fountain":true,"multiVote":true,"multiChoice":true,"priority":1,"closingOffset":5000,"voteRoles":["authenticated"],"question":{"text":"Who will win the elections?"},"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"bbf9ab52-1c7a-4b09-9e8a-f18ace82ce1d"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"9b513553-7cb3-4e8e-a1e5-37770ab4b699"}]},"facebook":{"postId":"10151400246079999","integrationType":"text","linkedChoices":["Bernie","Trump"],"enabled":true},"studio":{"backgroundImage":{"width":579,"height":580,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"backgroundVideo":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","aspectRatio":"16:9","loop":true,"autoplay":true}},"resultType":"actual-votes","id":"0ff964c6-fc5c-4342-a771-024bd0e0433a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","createdAt":"2017-11-29T09:13:15.275Z"}
```



### 2. Update Polls Config


Update the polls config of a stream. When creating a stream it will automatically create a polls config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"enabled": true
}
```



***Responses:***


Status: Update Polls Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.723Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-29T09:17:24.489Z","cdnHost":"http://localhost:14569/cdn.local.zender.tv"}
```



### 3. Create Poll


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "realtimeResults": true,
  "showResults": true,
  "fountain": true,
  "multiVote": true,
  "multiChoice": true,
  "priority": 1,
  "closingOffset": 5000,
  "voteRoles": [
    "authenticated"
  ],
  "question": {
    "text": "Who will win the elections?"
  },
  "answer": {
    "choices": [
      {
        "title": "Bernie Sanders",
        "image": {
          "url": "{{getUrl}}"
        }
      },
      {
        "title": "Donald Trump",
        "image": {
          "url": "{{getUrl}}"
        }
      }
    ]
  },
  "facebook": {
    "postId": "10151400246079999",
    "integrationType": "text",
    "linkedChoices": [
      "Bernie",
      "Trump"
    ],
    "enabled": true
  },
  "studio": {
    "backgroundImage": {
      "width": 579,
      "height": 580,
      "url": "{{getUrl}}"
    },
    "backgroundVideo": {
      "url": "{{getUrl}}",
      "aspectRatio": "16:9",
      "loop": true,
      "autoplay": true
    }
  }
}
```



***Responses:***


Status: Create Poll | Code: 200



```js
{"realtimeResults":true,"showResults":true,"fountain":true,"multiVote":true,"multiChoice":true,"priority":1,"closingOffset":5000,"voteRoles":["authenticated"],"question":{"text":"Who will win the elections?"},"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"bbf9ab52-1c7a-4b09-9e8a-f18ace82ce1d"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"9b513553-7cb3-4e8e-a1e5-37770ab4b699"}]},"facebook":{"postId":"10151400246079999","integrationType":"text","linkedChoices":["Bernie","Trump"],"enabled":true},"studio":{"backgroundImage":{"width":579,"height":580,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"backgroundVideo":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","aspectRatio":"16:9","loop":true,"autoplay":true}},"resultType":"actual-votes","id":"0ff964c6-fc5c-4342-a771-024bd0e0433a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","createdAt":"2017-11-29T09:13:15.275Z"}
```



### 4. Get Poll


Get a poll.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 5. Get Poll results


Get results for a poll.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}/results
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 6. Update Poll


Update a poll.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "realtimeResults": true,
  "showResults": false,
  "fountain": true,
  "multiVote": true,
  "multiChoice": true,
  "priority": 1,
  "closingOffset": 10000,
  "voteRoles": [
    "anonymous"
  ],
  "question": {
    "text": "Who will win the American elections?"
  },
  "answer": {
    "choices": [
      {
        "title": "Bernie Sanders",
        "image": {
          "url": "{{getUrl}}"
        }
      },
      {
        "title": "Donald Trump",
        "image": {
          "url": "{{getUrl}}"
        }
      }
    ]
  }
}
```



***Responses:***


Status: Animate Studio Results Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["anonymous"],"question":{"text":"Who will win the American elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"createdAt":"2017-11-29T09:39:07.473Z","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"b6168b48-15de-4e4e-a17e-932ffaf979eb"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"647d74a4-8ba0-4041-84a4-f6a62e6d81d0"}]},"animateStudioResults":1511948521594,"showResults":false,"id":"d962ae65-75ad-45ac-8495-b38f56d0180a","triggeredAt":1511948388460,"closingOffset":10000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:42:28.063Z"}
```



Status: Trigger Studio Result Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["anonymous"],"question":{"text":"Who will win the American elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"createdAt":"2017-11-29T09:39:07.473Z","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"b6168b48-15de-4e4e-a17e-932ffaf979eb"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"647d74a4-8ba0-4041-84a4-f6a62e6d81d0"}]},"showResults":false,"id":"d962ae65-75ad-45ac-8495-b38f56d0180a","triggeredAt":1511948388460,"closingOffset":10000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:41:26.320Z"}
```



Status: Update Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["anonymous"],"question":{"text":"Who will win the American elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"createdAt":"2017-11-29T09:39:07.473Z","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"b6168b48-15de-4e4e-a17e-932ffaf979eb"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"647d74a4-8ba0-4041-84a4-f6a62e6d81d0"}]},"showResults":false,"id":"d962ae65-75ad-45ac-8495-b38f56d0180a","closingOffset":10000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:40:42.415Z"}
```



Status: Animate Player Results Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["anonymous"],"question":{"text":"Who will win the American elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"createdAt":"2017-11-29T09:39:07.473Z","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"b6168b48-15de-4e4e-a17e-932ffaf979eb"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"647d74a4-8ba0-4041-84a4-f6a62e6d81d0"}]},"animateStudioResults":1511948521594,"showResults":false,"animatePlayerResults":1511948585258,"id":"d962ae65-75ad-45ac-8495-b38f56d0180a","triggeredAt":1511948388460,"closingOffset":10000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:43:23.518Z"}
```



### 7. Delete Poll


Delete a poll.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "realtimeResults": true,
  "showResults": false,
  "fountain": true,
  "multiVote": true,
  "multiChoice": true,
  "priority": 1,
  "closingOffset": 10000,
  "voteRoles": [
    "anonymous"
  ],
  "question": {
    "text": "Who will win the American elections?"
  },
  "answer": {
    "choices": [
      {
        "title": "Bernie Sanders",
        "image": {
          "url": "{{getUrl}}"
        }
      },
      {
        "title": "Donald Trump",
        "image": {
          "url": "{{getUrl}}"
        }
      }
    ]
  }
}
```



***Responses:***


Status: Delete Poll | Code: 200



```js
{"deleted":true}
```



### 8. Start Poll


Start a poll. This means that it will be open for the public to vote on the choices until the poll has stopped and the "closingOffset" defined in the poll has expired. Note that while the poll is started it cannot be edited nor can it be deleted.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}/start
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



***Responses:***


Status: Start Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["authenticated"],"question":{"text":"Who will win the elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"openedAt":"2017-11-29T09:26:39.440Z","createdAt":"2017-11-29T09:23:41.146Z","status":"open","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"084bacc5-b8ce-4096-bdc5-1b1e00570206"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"85a0a3e1-a705-4844-8466-ea0e07ce9727"}]},"showResults":true,"id":"d97a4943-9373-421a-ae6a-8d4a2908e50a","closedAt":"2017-11-29T09:26:10.926Z","closingOffset":5000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:26:39.440Z","postVotes":"http://localhost:3006/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/polls/d97a4943-9373-421a-ae6a-8d4a2908e50a/vote"}
```



Status: Create Poll | Code: 200



```js
{"realtimeResults":true,"showResults":true,"fountain":true,"multiVote":true,"multiChoice":true,"priority":1,"closingOffset":5000,"voteRoles":["authenticated"],"question":{"text":"Who will win the elections?"},"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"bbf9ab52-1c7a-4b09-9e8a-f18ace82ce1d"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"9b513553-7cb3-4e8e-a1e5-37770ab4b699"}]},"facebook":{"postId":"10151400246079999","integrationType":"text","linkedChoices":["Bernie","Trump"],"enabled":true},"studio":{"backgroundImage":{"width":579,"height":580,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"backgroundVideo":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","aspectRatio":"16:9","loop":true,"autoplay":true}},"resultType":"actual-votes","id":"0ff964c6-fc5c-4342-a771-024bd0e0433a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","createdAt":"2017-11-29T09:13:15.275Z"}
```



### 9. Stop Poll


Stop a poll. This means that it will be closed for the public.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}/stop
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



***Responses:***


Status: Stop Poll | Code: 200



```js
{"realtimeResults":true,"studio":{"backgroundVideo":{"aspectRatio":"16:9","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","loop":true,"autoplay":true},"backgroundImage":{"width":579,"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","height":580}},"fountain":true,"voteRoles":["authenticated"],"question":{"text":"Who will win the elections?"},"streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","facebook":{"postId":"10151400246079999","integrationType":"text","enabled":true,"linkedChoices":["Bernie","Trump"]},"priority":1,"openedAt":"2017-11-29T09:26:09.425Z","createdAt":"2017-11-29T09:23:41.146Z","status":"closed","multiChoice":true,"multiVote":true,"answer":{"choices":[{"title":"Bernie Sanders","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"084bacc5-b8ce-4096-bdc5-1b1e00570206"},{"title":"Donald Trump","image":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"},"id":"85a0a3e1-a705-4844-8466-ea0e07ce9727"}]},"showResults":true,"id":"d97a4943-9373-421a-ae6a-8d4a2908e50a","closedAt":"2017-11-29T09:26:10.926Z","closingOffset":5000,"resultType":"actual-votes","updatedAt":"2017-11-29T09:26:10.926Z"}
```



## Admin/Quiz



### 1. Get Quiz Config


Get polls config. This endpoint will also return the started (public) polls and their results (if results are configured for that poll).

When called with an admin token (see [Admin Token Login](#d15beccd-f01f-4d3a-a8ba-1b1bdc3480a7)), the response includes all questions.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 2. Create Quiz Config


Update the polls config of a stream. When creating a stream it will automatically create a polls config.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/quiz/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"enabled": true
}
```



***Responses:***


Status: Update Polls Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.723Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-29T09:17:24.489Z","cdnHost":"http://localhost:14569/cdn.local.zender.tv"}
```



### 3. Update Quiz Config


Update the polls config of a stream. When creating a stream it will automatically create a polls config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"enabled": true
}
```



***Responses:***


Status: Update Polls Config | Code: 200



```js
{"createdAt":"2017-11-28T13:55:31.723Z","id":"a2993350-cb51-437d-bf39-41e110a71f5a","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","enabled":true,"updatedAt":"2017-11-29T09:17:24.489Z","cdnHost":"http://localhost:14569/cdn.local.zender.tv"}
```



### 4. Create Quiz


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"answerTime": 10000,
	"maxLatency": 3000,
	"title": "Test Quiz",
	"description": "Test Trivia"
}
```



***Responses:***


Status: Create Quiz | Code: 200



```js
{"answerTime":10000,"maxLatency":3000,"title":"Test Quiz","description":"Test Trivia","status":"preparation","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","createdAt":"2018-03-05T14:35:58.816Z"}
```



### 5. Update Quiz


Create a poll.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"answerTime": 11000
}
```



***Responses:***


Status: Update Quiz | Code: 200



```js
{"status":"preparation","updatedAt":"2018-03-05T14:41:42.413Z","answerTime":11000,"createdAt":"2018-03-05T14:35:58.816Z","description":"Test Trivia","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","maxLatency":3000,"streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","title":"Test Quiz"}
```



### 6. Get Quizzes


Create a poll.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Quizzes | Code: 200



```js
[{"status":"preparation","answerTime":10000,"createdAt":"2018-03-05T14:35:58.816Z","description":"Test Trivia","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","maxLatency":3000,"streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","title":"Test Quiz"}]
```



### 7. Get Quizzes for channel


Get the quizzes for all streams of a channel.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/quiz
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Quizzes | Code: 200



```js
[{"status":"preparation","answerTime":10000,"createdAt":"2018-03-05T14:35:58.816Z","description":"Test Trivia","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","maxLatency":3000,"streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","title":"Test Quiz"}]
```



### 8. Get Quiz


Get info about a single quiz.

When called with an admin token (see [Admin Token Login](#d15beccd-f01f-4d3a-a8ba-1b1bdc3480a7)), the response includes all questions.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Quiz | Code: 200



```js
{"status":"preparation","answerTime":10000,"createdAt":"2018-03-05T14:35:58.816Z","description":"Test Trivia","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","maxLatency":3000,"streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","title":"Test Quiz","questions":[]}
```



### 9. Create Question


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"text": "Which best movie won the Palme d'Or in 2017",
	"answers": [
		{
			"id": 0,
			"text": "The Square"
		},
		{
			"id": 1,
			"text": "The Circle"
		},
		{
			"id": 2,
			"text": "The Triangle"
		}
	],
	"correct": [0]
}
```



***Responses:***


Status: Create Quiz | Code: 200



```js
{"answerTime":10000,"maxLatency":3000,"title":"Test Quiz","description":"Test Trivia","status":"preparation","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","createdAt":"2018-03-05T14:35:58.816Z"}
```



### 10. Update Question


Create a poll.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question/{{questionId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"text": "Which movie won the Palme d'Or in 2017",
	"answers": [
		{
			"id": 0,
			"text": "The Square"
		},
		{
			"id": 1,
			"text": "The Circle"
		},
		{
			"id": 2,
			"text": "The Triangle"
		}
	],
	"correct": [0]
}
```



***Responses:***


Status: Create Quiz | Code: 200



```js
{"answerTime":10000,"maxLatency":3000,"title":"Test Quiz","description":"Test Trivia","status":"preparation","id":"9b247a8d-09e2-4449-bf0c-81df588ddd11","streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","createdAt":"2018-03-05T14:35:58.816Z"}
```



Status: Update Question | Code: 200



```js
{"correct":[0],"updatedAt":"2018-03-05T14:47:43.808Z","createdAt":"2018-03-05T14:47:36.370Z","answers":[{"id":0,"text":"The Square"},{"id":1,"text":"The Circle"},{"id":2,"text":"The Triangle"}],"text":"Which movie won the Palme d'Or in 2017","id":"4cef81a6-d25e-4927-8714-48b8f8316d0d","quizId":"9b247a8d-09e2-4449-bf0c-81df588ddd11"}
```



### 11. Delete Question


Create a poll.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question/{{questionId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 12. Start Quiz


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/start
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 13. Launch Question


Launches the specified question for this quiz. See [Get Quiz Config](#77a182c3-bd26-4ef9-8070-1f2a92bc7bc1) or [Get Quiz](#25dcb7fd-e7b9-4dc2-87c6-cb76af6d4870) to get the questions.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question/{{questionId}}/launch
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 14. Broadcast Quiz Results


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/results
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 15. Retrieve Quiz Results


Get the quiz results.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/results
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Retrieve Quiz Results | Code: 200



```js
{"winners":[{"id":"309ae678-b9ec-42b0-86fc-d4de304c7dcd","name":"Jan Willem","avatar":"https://graph.facebook.com/1854345981301940/picture?width=250&type=square"}],"count":1}
```



### 16. Stop Quiz


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/stop
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 17. Reset Quiz


Create a poll.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/reset
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 18. Delete Quiz


Create a poll.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



### 19. Clear Quiz Referrer code


Clears referrer code for user with specified share code.

| Permissions         | no token | anonymous token | provider token | admin token |
| ------------------- | :------: | :-------------: | :------------: | :---------: |
| Clear referrer code | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/clearReferrer
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
  "shareCode": "ddddd"
}
```



***Responses:***


Status: Not found | Code: 404



```js
{"code":"NOT_FOUND","message":"Share code does not exist."}
```



Status: Success | Code: 200



```js
{}
```



### 20. Download quiz winners


To download winners as csv, use 'Accept: text/csv', to download as json: 'Accept: application/json'.

| Permissions      | no token | anonymous token | provider token | admin token |
| ---------------- | :------: | :-------------: | :------------: | :---------: |
| Download winners | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/leaderboard/win/export
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Accept | application/json |  |



***Responses:***


Status: Download quiz winners as csv | Code: 200



```js
"id","Name","Username","Login Provider","Login Provider id","Win amount"
"e093ef70-f231-4699-9798-4f77a7886fae","Jan Willem","Jan","facebook","1753346941202930","50.00"
```



Status: Download quiz winners as json | Code: 200



```js
{
    "winners": [
        {
            "id": "e093ef70-f231-4699-9798-4f77a7886fae",
            "Name": "Jan Willem",
            "Username": "Jan",
            "Login Provider": "facebook",
            "Login Provider id": "1753346941202930",
            "Win amount": "50.00"
        }
    ]
}
```



Status: Empty result | Code: 200



```js
"id","Name","Login Provider","Login Provider id"
```



### 21. Download quiz players


To download a list of quiz players as csv, use 'Accept: text/csv', to download as json: 'Accept: application/json'.

| Permissions      | no token | anonymous token | provider token | admin token |
| ---------------- | :------: | :-------------: | :------------: | :---------: |
| Download winners | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/players
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Accept | application/json |  |



***Responses:***


Status: Download quiz players as json | Code: 200



```js
{
    "players": [
        {
            "id": "e093ef70-f231-4699-9798-4f77a7886fae",
            "Name": "Jan Willem",
            "Username": "Jan",
            "Login Provider": "facebook",
            "Login Provider id": "1753346941202930",
            "Win amount": "50.00"
        }
    ]
}
```



Status: Download quiz players as csv | Code: 200



```js
"id","Name","Username","Login Provider","Login Provider id"
"e093ef70-f231-4699-9798-4f77a7886fae","Jan Willem","Jan","facebook","1753346941202930"
```



Status: Empty result | Code: 200



```js
"id","Name","Login Provider","Login Provider id"
```



### 22. Download quiz player stats


To download a list of quiz player stats as csv, use 'Accept: text/csv', to download as json: 'Accept: application/json'.

| Permissions      | no token | anonymous token | provider token | admin token |
| ---------------- | :------: | :-------------: | :------------: | :---------: |
| Download winners | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/playerStats
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Accept | text/csv |  |



***Responses:***


Status: Download quiz player stats as csv | Code: 200



```js
"id","Name","Username","Login Provider","Login Provider id","Correct Answers","Used Extra Lives"
"356fe6a4-83bc-47bf-b2c0-5e2af1e505d8","Anonymous","anonymous2692","device","c49cbeef-8fb4-4caa-88e9-3ca53a762618",1,0
```



Status: Empty result | Code: 200



```js
"id","Name","Username","Login Provider","Login Provider id","Correct Answers","Used Extra Lives"

```



Status: Download quiz player stats as json | Code: 200



```js
{
    "stats": [
        {
            "id": "356fe6a4-83bc-47bf-b2c0-5e2af1e505d8",
            "Name": "Anonymous",
            "Username": "anonymous2692",
            "Login Provider": "device",
            "Login Provider id": "c49cbeef-8fb4-4caa-88e9-3ca53a762618",
            "Correct Answers": 1,
            "Used Extra Lives": 0
        }
    ]
}
```



### 23. Increment extra lives (deprecated)


Increment number of extra lives.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Increment extra lives | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/extraLives
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
	"shareCode": "abcd"
}
```



***Responses:***


Status: Increment extra lives | Code: 200



```js
{"extraLives":3}
```



### 24. Increment extra lives


Increment number of extra lives.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Increment extra lives | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/extraLives
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
	"shareCode": "abcd"
}
```



***Responses:***


Status: Increment extra lives | Code: 200



```js
{"extraLives":3}
```



### 25. Set extra lives


Set number of extra lives.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Set extra lives       | -        | -               | -              | x           |


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{quizApiHost}}/v1/extraLives
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
	"shareCode": "abcd",
	"extraLives": 10
}
```



***Responses:***


Status: Set extra lives | Code: 200



```js
{"extraLives":3}
```



### 26. Get quiz statistics


Get the quiz statistics


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/stats
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Responses:***


Status: Empty stats (no questions triggered) | Code: 200



```js
{}
```



Status: Stats with several questions | Code: 200



```js
[
    {
        "correct": [
            1
        ],
        "updatedAt": "2019-04-24T14:58:02.650Z",
        "launchedAt": "2019-04-24T14:57:44.416Z",
        "createdAt": "2018-09-24T10:55:07.150Z",
        "answers": [
            {
                "id": 0,
                "text": "De grootste openlucht filmstudio"
            },
            {
                "id": 1,
                "text": "De grootste onderwater filmstudio"
            },
            {
                "id": 2,
                "text": "De grootste ondergrondse filmstudio"
            }
        ],
        "text": "Welke filmstudio komt er in 2019 naar Vlaanderen?",
        "id": "b1aa3e58-33a7-41ba-8553-cb4d7400a326",
        "launchIndex": 1,
        "quizId": "c6bb121c-3e9b-41ac-9b4a-486b12df4432",
        "redeemable": true,
        "closeAt": "2019-04-24T14:57:55.916Z",
        "answerAt": "2019-04-24T14:58:02.639Z",
        "stats": {
            "answers": {
                "1": 3
            },
            "stoppedPlaying": 0,
            "extraLives": 0
        }
    },
    {
        "correct": [
            1
        ],
        "updatedAt": "2019-04-24T14:58:32.520Z",
        "launchedAt": "2019-04-24T14:58:13.151Z",
        "createdAt": "2018-09-24T10:56:16.055Z",
        "answers": [
            {
                "id": 0,
                "text": "de Brit Kevin Coin"
            },
            {
                "id": 1,
                "text": "de Hongaar Laszlo Hanyecz"
            },
            {
                "id": 2,
                "text": "de Japanner Satoshi Nakamoto"
            }
        ],
        "text": "Wie gebruikte als eerste de Bitcoin voor een echte commerciële transactie?",
        "id": "1e9b0c9a-0986-4ecb-b5bc-6f086e05f4e4",
        "launchIndex": 2,
        "quizId": "c6bb121c-3e9b-41ac-9b4a-486b12df4432",
        "redeemable": false,
        "closeAt": "2019-04-24T14:58:24.651Z",
        "answerAt": "2019-04-24T14:58:32.510Z",
        "stats": {
            "answers": {
                "0": 1,
                "1": 2
            },
            "stoppedPlaying": 0,
            "extraLives": 0
        }
    },
    {
        "correct": [
            0
        ],
        "updatedAt": "2019-04-24T14:59:03.408Z",
        "launchedAt": "2019-04-24T14:58:44.748Z",
        "createdAt": "2018-09-24T10:55:49.255Z",
        "answers": [
            {
                "id": 0,
                "text": "René Redzepi"
            },
            {
                "id": 1,
                "text": "Peter Goossens"
            },
            {
                "id": 2,
                "text": "Heston Blumenthal"
            }
        ],
        "text": "Welke van deze sterrenchefs had ooit het beste restaurant ter wereld?",
        "id": "9be4c0df-9680-405d-89ea-06dd047cb6f4",
        "launchIndex": 3,
        "quizId": "c6bb121c-3e9b-41ac-9b4a-486b12df4432",
        "redeemable": true,
        "closeAt": "2019-04-24T14:58:56.248Z",
        "answerAt": "2019-04-24T14:59:03.397Z",
        "stats": {
            "answers": {
                "0": 1
            },
            "stoppedPlaying": 1,
            "extraLives": 0
        }
    }
]
```



## Admin/Shoutbox



### 1. Get Shoutbox Config


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 2. Set Placeholder Shoutbox Config


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "placeholder": "Leave a message plz..."
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 3. Set Topic Shoutbox Config


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "topic": "A brand new topic"
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 4. Set Welcome Shoutbox Config copy


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "welcome": "Welcome to the new live stream"
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 5. Enable Shoutbox


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": true
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 6. Disable Shoutbox


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": false
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 7. Update Shoutbox Config


Update the shoutbox config of a stream. When creating a stream it will automatically create a shoutbox config.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"enabled": true,
	"topic": "Topic",
	"placeholder": "Leave a message plz...",
	"welcome": "Welcome to the new live stream",
	"shoutRoles":["user", "anonymous"]
}
```



***Responses:***


Status: Update Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "shoutRoles": [
        "anonymous",
        "user"
    ],
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "starredSort": [
        {
            "id": "110d3e00-925b-441e-bb92-a418dd80a004"
        }
    ],
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-29T08:23:28.714Z"
}
```



### 8. Get Shoutbox Messages


Send a shoutbox message.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Send Shoutbox Message On Behalf Of | Code: 200



```js
{"type":"user","id":"46d8c279-cfbd-4f86-baeb-b798b38d45aa","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"On behalf of."},"createdAt":"2017-11-29T13:04:32.525Z","user":{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"unblocked_2017-11-29T13:04:22.866Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T13:04:22.866Z"}}
```



Status: Send Shoutbox User Message | Code: 200



```js
{"type":"user","id":"49608a40-46f3-498c-a525-2de3927517c6","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"Admin user message."},"createdAt":"2017-11-29T08:44:09.813Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



Status: Send Shoutbox System Message | Code: 200



```js
{"type":"system","id":"e81c1243-c32e-4c57-a755-3d055e8ed20a","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"System says go."},"createdAt":"2017-11-29T08:43:28.504Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



### 9. Send Shoutbox User Message


Send a shoutbox message.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "type": "user",
  "clientId": "ketnet-live-admin-1511880426214",
  "content": {
    "text": "User message.",
    "image": "https://s3-eu-west-1.amazonaws.com/cdn.staging.zender.tv/live/uploads/04573ba9-3efb-402f-b956-9a0f1cfeb285/2017-12-01/cea804ac-4e19-4c03-a601-fe463a422845.original.gif"
  }
}
```



***Responses:***


Status: Send Shoutbox Message On Behalf Of | Code: 200



```js
{"type":"user","id":"46d8c279-cfbd-4f86-baeb-b798b38d45aa","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"On behalf of."},"createdAt":"2017-11-29T13:04:32.525Z","user":{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"unblocked_2017-11-29T13:04:22.866Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T13:04:22.866Z"}}
```



Status: Send Shoutbox User Message | Code: 200



```js
{"type":"user","id":"49608a40-46f3-498c-a525-2de3927517c6","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"Admin user message."},"createdAt":"2017-11-29T08:44:09.813Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



Status: Send Shoutbox System Message | Code: 200



```js
{"type":"system","id":"e81c1243-c32e-4c57-a755-3d055e8ed20a","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"System says go."},"createdAt":"2017-11-29T08:43:28.504Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



### 10. Send Shoutbox System Message


Send a shoutbox message.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "type": "system",
  "clientId": "ketnet-live-admin-1511880426214",
  "content": {
    "text": "System message.",
    "image": "https://s3-eu-west-1.amazonaws.com/cdn.staging.zender.tv/live/uploads/04573ba9-3efb-402f-b956-9a0f1cfeb285/2017-12-01/cea804ac-4e19-4c03-a601-fe463a422845.original.gif"
  }
}
```



***Responses:***


Status: Send Shoutbox System Message | Code: 200



```js
{"type":"system","id":"e81c1243-c32e-4c57-a755-3d055e8ed20a","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"System says go."},"createdAt":"2017-11-29T08:43:28.504Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



Status: Send Shoutbox User Message | Code: 200



```js
{"type":"user","id":"49608a40-46f3-498c-a525-2de3927517c6","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"Admin user message."},"createdAt":"2017-11-29T08:44:09.813Z","user":{"authenticated":true,"createdAt":"2017-11-28T13:53:25.245Z","lastLogin":"2017-11-28T14:41:27.162Z","role":"admin","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","id":"zender-api","updatedAt":"2017-11-28T14:41:27.162Z"}}
```



Status: Send Shoutbox Message On Behalf Of | Code: 200



```js
{"type":"user","id":"46d8c279-cfbd-4f86-baeb-b798b38d45aa","clientId":"ketnet-live-admin-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"On behalf of."},"createdAt":"2017-11-29T13:04:32.525Z","user":{"authenticated":true,"createdAt":"2017-11-29T08:33:42.090Z","flag":"unblocked_2017-11-29T13:04:22.866Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook","uid":"1459394774070695"},"name":"Benoit Shapiro","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695","avatar":"https://graph.facebook.com/1459394774070695/picture?width=250&type=square","id":"8184fbdc-6861-4fc5-9944-e7860b95f4df","updatedAt":"2017-11-29T13:04:22.866Z"}}
```



### 11. Update Shoutbox Message


Get all shoutbox messages.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages/{{messageId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"stars": 5,
    "content": {
        "text": "Something less explicit."
    }
}
```



***Responses:***


Status: Update Shoutbox Message | Code: 200



```js
{"createdAt":"2017-11-28T15:19:10.443Z","clientId":"bdaac6e5-fb79-462c-b669-80641bfef413-1511880426214","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","id":"110d3e00-925b-441e-bb92-a418dd80a004","stars":5,"type":"user","content":{"text":"Something less explicit."},"updatedAt":"2017-11-28T15:26:35.005Z","user":{"id":"f468fca3-1287-4858-880f-7c099e0ba1d3","avatar":"https://graph.facebook.com/undefined/picture?width=250&type=square","externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_undefined"}}
```



### 12. Trigger Shoutbox Message


Trigger a shoutbox message to the studio visualisation?


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages/{{messageId}}/trigger
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



***Responses:***


Status: Trigger Shoutbox Message Success | Code: 200



```js
{
        "createdAt": "2017-11-28T15:19:10.443Z",
        "clientId": "bdaac6e5-fb79-462c-b669-80641bfef413-1511880426214",
        "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
        "id": "110d3e00-925b-441e-bb92-a418dd80a004",
        "stars": 5,
        "type": "user",
        "userId": "f468fca3-1287-4858-880f-7c099e0ba1d3",
        "content": {
            "text": "Something less explicit."
        },
        "updatedAt": "2017-11-28T15:26:35.005Z",
        "user": {
            "id": "f468fca3-1287-4858-880f-7c099e0ba1d3",
            "avatar": "https://graph.facebook.com/undefined/picture?width=250&type=square",
            "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_undefined",
            "flag": "blocked_2017-11-28T15:27:06.362Z"
        }
    }
```



Status: Trigger Unknown Shoutbox Message | Code: 404



```js
{"code":"NOT_FOUND","message":"No message found with id `110d3e00-925b-441e-bb92-a418dd80a004`"}
```



### 13. Delete Shoutbox Message


Delete a shoutbox messages.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages/{{messageId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 14. Export Shoutbox Messages


Download CSV with all the shoutbox messages.


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages/export
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| type | csv |  |



***Responses:***


Status: Export Shoutbox Messages | Code: 200



```js
"Text","Image","Video","First Name","Name","Created At","Id","External Id"
"Kaka.",,,,,"2017-11-29T08:44:50.344Z","zender-api",
"System message.",,,,,"2017-11-29T08:44:28.480Z","zender-api",
"Admin user message.",,,,,"2017-11-29T08:44:09.813Z","zender-api",
"System says go.",,,,,"2017-11-29T08:43:28.504Z","zender-api",
"System says yes.",,,,,"2017-11-29T08:42:47.209Z","zender-api",
"user",,,,,"2017-11-29T08:42:06.270Z","zender-api",
"Who u say?",,,,,"2017-11-29T08:41:43.733Z","zender-api",
"System says yes.",,,,"Benoit Shapiro","2017-11-29T08:41:26.700Z","8184fbdc-6861-4fc5-9944-e7860b95f4df","b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695"
"Who is doing that?",,,,,"2017-11-29T08:41:13.669Z","zender-api",
"System says no.",,,,"Benoit Shapiro","2017-11-29T08:40:17.608Z","8184fbdc-6861-4fc5-9944-e7860b95f4df","b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695"
"System message.",,,,"Benoit Shapiro","2017-11-29T08:39:57.701Z","8184fbdc-6861-4fc5-9944-e7860b95f4df","b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695"
"Something less explicit.",,,,,"2017-11-28T15:19:10.443Z","f468fca3-1287-4858-880f-7c099e0ba1d3","b8f99a0c-1383-4891-af7a-563b5903d390_undefined"
```



### 15. Update Shoutbox Profanity Filter


Update the shoutbox profanity filter list.


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{coreApiHost}}/v1/targets/{{targetId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "shoutbox": {
    "profanity": [
      {
        "matches": "exact",
        "text": "something exact explicit"
      },
      {
        "matches": "contains",
        "text": "something that contains explicit language"
      }
    ]
  }
}
```



***Responses:***


Status: Update Shoutbox Profanity Filter | Code: 200



```js
{"emojis":{"defaultSets":[{"emojis":[{"title":"000-gezichten__smile01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/062c82a8-1de5-4615-808f-02eaefd95845.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/062c82a8-1de5-4615-808f-02eaefd95845.original.png"},{"title":"000-gezichten__smile02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b21bc786-8a07-48d5-ab8d-e0acfa94e5a9.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b21bc786-8a07-48d5-ab8d-e0acfa94e5a9.original.png"},{"title":"000-gezichten__smile03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8be81c15-0ef0-4e83-b414-7ab0620ee774.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8be81c15-0ef0-4e83-b414-7ab0620ee774.original.png"},{"title":"000-gezichten__smile04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e2b27bab-f05d-4a01-95e1-79f778794274.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e2b27bab-f05d-4a01-95e1-79f778794274.original.png"},{"title":"000-gezichten__smile05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/69a7e7c5-ba0e-4095-af53-8d3de9e7a375.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/69a7e7c5-ba0e-4095-af53-8d3de9e7a375.original.png"},{"title":"000-gezichten__smile06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/57350af7-b67d-42b7-a59b-106ea3deae49.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/57350af7-b67d-42b7-a59b-106ea3deae49.original.png"},{"title":"000-gezichten__smile07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/29978b65-818e-4416-bc38-f2d5b03e240e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/29978b65-818e-4416-bc38-f2d5b03e240e.original.png"},{"title":"000-gezichten__smile08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/56cb619a-5f12-4ece-8942-fd4b9de0a8ac.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/56cb619a-5f12-4ece-8942-fd4b9de0a8ac.original.png"},{"title":"000-gezichten__smile09","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ab0d4c4b-7076-4356-86ca-e6c8e183e1c2.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ab0d4c4b-7076-4356-86ca-e6c8e183e1c2.original.png"},{"title":"000-gezichten__smile10","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/02b2c058-bde0-47ac-b21a-3f9d0c1397b7.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/02b2c058-bde0-47ac-b21a-3f9d0c1397b7.original.png"},{"title":"000-gezichten__smile11","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/de0d1e3a-52fa-4f03-af9c-1b427d75acc5.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/de0d1e3a-52fa-4f03-af9c-1b427d75acc5.original.png"},{"title":"000-gezichten__smile12","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/509dcab2-6176-45c8-bc28-cec7aba6a797.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/509dcab2-6176-45c8-bc28-cec7aba6a797.original.png"},{"title":"000-gezichten__smile13","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/70cbe111-3ae1-4579-b5e5-2dc29d08920e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/70cbe111-3ae1-4579-b5e5-2dc29d08920e.original.png"},{"title":"000-gezichten__smile14","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f656854b-da1c-4204-850d-69ef63dd4e29.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f656854b-da1c-4204-850d-69ef63dd4e29.original.png"},{"title":"000-gezichten__smile15","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fecfbfcb-2014-4a64-a571-3d62d79e9cfb.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fecfbfcb-2014-4a64-a571-3d62d79e9cfb.original.png"},{"title":"000-gezichten__smile16","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/61ad7b8e-f27d-499a-8efe-82ca1684dffe.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/61ad7b8e-f27d-499a-8efe-82ca1684dffe.original.png"},{"title":"000-gezichten__t-random01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7d21813-e166-441b-ab52-ac041ed2474c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7d21813-e166-441b-ab52-ac041ed2474c.original.png"},{"title":"000-gezichten__t-random02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/805abf31-8bcb-4376-ba8c-e34eb40f6d56.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/805abf31-8bcb-4376-ba8c-e34eb40f6d56.original.png"},{"title":"000-gezichten__t-random03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/57f6f453-049a-43f0-93c6-8dfd50962040.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/57f6f453-049a-43f0-93c6-8dfd50962040.original.png"},{"title":"000-gezichten__t-random04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/af45e9c6-ef86-4b51-924c-87788a8b7264.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/af45e9c6-ef86-4b51-924c-87788a8b7264.original.png"},{"title":"000-gezichten__t-sad01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d7d7bf03-e77a-452e-9e13-a523a8efa742.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d7d7bf03-e77a-452e-9e13-a523a8efa742.original.png"},{"title":"000-gezichten__t-sad02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4cd31400-8baf-4b23-a5cc-9522265f9208.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4cd31400-8baf-4b23-a5cc-9522265f9208.original.png"},{"title":"000-gezichten__t-sad03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/02b6d320-bc54-4e1b-8a5e-014dd4f87242.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/02b6d320-bc54-4e1b-8a5e-014dd4f87242.original.png"},{"title":"000-gezichten__t-sad05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7a0f6948-d0d6-4c54-8823-6e33ff500171.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7a0f6948-d0d6-4c54-8823-6e33ff500171.original.png"},{"title":"000-gezichten__t-sad06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8163800d-9c98-48a1-827f-2a94b700d24b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8163800d-9c98-48a1-827f-2a94b700d24b.original.png"},{"title":"000-gezichten__t-sad07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/294aa82e-8fbf-4ff3-89aa-61c50a24f410.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/294aa82e-8fbf-4ff3-89aa-61c50a24f410.original.png"},{"title":"000-gezichten__t-sad08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f88579f-309b-41d8-ba87-ce3abffaf924.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f88579f-309b-41d8-ba87-ce3abffaf924.original.png"},{"title":"000-gezichten__u-divers01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7b53c09a-5e93-454c-92ce-3a9171a0ecbf.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7b53c09a-5e93-454c-92ce-3a9171a0ecbf.original.png"},{"title":"000-gezichten__u-divers011","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/366a38df-daa9-45ad-a198-91420f9984c3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/366a38df-daa9-45ad-a198-91420f9984c3.original.png"},{"title":"000-gezichten__u-divers02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/44706833-39b0-44ab-8b82-479e3821d1a0.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/44706833-39b0-44ab-8b82-479e3821d1a0.original.png"},{"title":"000-gezichten__u-divers03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/570da07f-bc33-4562-abeb-2d13d45fe941.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/570da07f-bc33-4562-abeb-2d13d45fe941.original.png"},{"title":"000-gezichten__u-divers04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/22591763-65a5-4317-a4ee-7abf3df67319.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/22591763-65a5-4317-a4ee-7abf3df67319.original.png"},{"title":"000-gezichten__u-divers05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bde12432-7acb-47a4-99d3-5d6316b1720f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bde12432-7acb-47a4-99d3-5d6316b1720f.original.png"},{"title":"000-gezichten__u-divers06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/21001452-8a80-43cc-ad26-a672d13d0b53.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/21001452-8a80-43cc-ad26-a672d13d0b53.original.png"},{"title":"000-gezichten__u-divers07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6a2b3726-d7d0-48d4-abde-f6b74583236a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6a2b3726-d7d0-48d4-abde-f6b74583236a.original.png"},{"title":"000-gezichten__u-divers08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c0fdafc9-f6c4-4626-9b86-cdd8248ca9c5.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c0fdafc9-f6c4-4626-9b86-cdd8248ca9c5.original.png"},{"title":"000-gezichten__u-divers09","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c4ddc01c-a0b8-4396-bfd3-75999dce1a2f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c4ddc01c-a0b8-4396-bfd3-75999dce1a2f.original.png"},{"title":"000-gezichten__u-divers12","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4e1fc193-2238-4458-b994-acfa263ddd7a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4e1fc193-2238-4458-b994-acfa263ddd7a.original.png"},{"title":"000-gezichten__u-divers13","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/137f2d30-252b-4760-b9b2-d83f036b9d6d.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/137f2d30-252b-4760-b9b2-d83f036b9d6d.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/062c82a8-1de5-4615-808f-02eaefd95845.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/062c82a8-1de5-4615-808f-02eaefd95845.original.png"},"id":"7b3f2436-dae0-45cf-aad2-4320cd342640","title":"000-faces"},{"emojis":[{"title":"001-handen__hand01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/982cdc90-f7ea-403b-a7a3-9d01c318c082.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/982cdc90-f7ea-403b-a7a3-9d01c318c082.original.png"},{"title":"001-handen__hand02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/04295cf9-fa41-4145-92b7-43ae13247347.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/04295cf9-fa41-4145-92b7-43ae13247347.original.png"},{"title":"001-handen__hand03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c0714a47-b2bc-4975-a6f2-57e15901b241.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c0714a47-b2bc-4975-a6f2-57e15901b241.original.png"},{"title":"001-handen__hand04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/476dc007-533f-49fa-bcf1-f19e24193341.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/476dc007-533f-49fa-bcf1-f19e24193341.original.png"},{"title":"001-handen__hand05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8d230974-526c-4145-9f5f-0ce3746565f3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8d230974-526c-4145-9f5f-0ce3746565f3.original.png"},{"title":"001-handen__hand06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/570d557a-7104-46d9-b2cb-9bfa510e9f9f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/570d557a-7104-46d9-b2cb-9bfa510e9f9f.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/982cdc90-f7ea-403b-a7a3-9d01c318c082.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/982cdc90-f7ea-403b-a7a3-9d01c318c082.original.png"},"id":"4775a542-bc43-4ce6-bf43-27a0fa7acc78","title":"001-hands"},{"emojis":[{"title":"002-liefde__love01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3e696aef-4e3b-458d-a9a4-1dd29e85577a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3e696aef-4e3b-458d-a9a4-1dd29e85577a.original.png"},{"title":"002-liefde__love02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f919a03a-2435-4fbf-9984-8a71c6b7e307.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f919a03a-2435-4fbf-9984-8a71c6b7e307.original.png"},{"title":"002-liefde__love03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a37b4d26-db46-4adb-8db2-4bd65d7f02f8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a37b4d26-db46-4adb-8db2-4bd65d7f02f8.original.png"},{"title":"002-liefde__love04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/26f85cc0-8e58-4913-9a05-815522767978.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/26f85cc0-8e58-4913-9a05-815522767978.original.png"},{"title":"002-liefde__love05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5f4210ac-277d-4acb-a802-602759429e77.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5f4210ac-277d-4acb-a802-602759429e77.original.png"},{"title":"002-liefde__love06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/56d0b698-8cc3-48d3-8646-c67f0810382b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/56d0b698-8cc3-48d3-8646-c67f0810382b.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3e696aef-4e3b-458d-a9a4-1dd29e85577a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3e696aef-4e3b-458d-a9a4-1dd29e85577a.original.png"},"id":"5b9dab91-f96d-4b60-a612-39a2ef567077","title":"002-love"},{"emojis":[{"title":"003-dieren__a-bunny","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/88531ca8-72b0-47c6-a75c-23c3ff80a2ab.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/88531ca8-72b0-47c6-a75c-23c3ff80a2ab.original.png"},{"title":"003-dieren__a-cat01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/41a743c4-088a-411e-8bee-04a4d20015d3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/41a743c4-088a-411e-8bee-04a4d20015d3.original.png"},{"title":"003-dieren__a-cat02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/50c1d174-c7bb-463c-a125-e92f0403bb75.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/50c1d174-c7bb-463c-a125-e92f0403bb75.original.png"},{"title":"003-dieren__a-cat03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/563693b5-9622-4814-96d6-18e60d3456fb.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/563693b5-9622-4814-96d6-18e60d3456fb.original.png"},{"title":"003-dieren__a-cat04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4cb185e-b067-41f9-9e21-ed6014509e0d.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4cb185e-b067-41f9-9e21-ed6014509e0d.original.png"},{"title":"003-dieren__a-chicken","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a4b73db4-e4be-4b45-b4fa-baf861833962.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a4b73db4-e4be-4b45-b4fa-baf861833962.original.png"},{"title":"003-dieren__a-chicken01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ee6fac0b-80d3-45c3-89af-004624362bb9.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ee6fac0b-80d3-45c3-89af-004624362bb9.original.png"},{"title":"003-dieren__a-chicken02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4905fdf7-f63c-4a94-9c30-0605516a74c0.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4905fdf7-f63c-4a94-9c30-0605516a74c0.original.png"},{"title":"003-dieren__a-cow","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/772a1df7-13a2-48c2-a102-052f801417a0.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/772a1df7-13a2-48c2-a102-052f801417a0.original.png"},{"title":"003-dieren__a-dog01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/61ae7dc8-0050-45b5-b2e4-7215b5f65a76.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/61ae7dc8-0050-45b5-b2e4-7215b5f65a76.original.png"},{"title":"003-dieren__a-dog02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/301b1cf2-8b15-458f-8184-4db0ac6356a2.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/301b1cf2-8b15-458f-8184-4db0ac6356a2.original.png"},{"title":"003-dieren__a-elephant","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/79aa026f-b2d0-4c6c-b81e-cf02b93ef4f4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/79aa026f-b2d0-4c6c-b81e-cf02b93ef4f4.original.png"},{"title":"003-dieren__a-fish01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/24dfc278-43de-4cfa-af68-36e779d7427e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/24dfc278-43de-4cfa-af68-36e779d7427e.original.png"},{"title":"003-dieren__a-fish02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a10e62a5-52c0-45b3-83f9-c84bf6ef2d7e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a10e62a5-52c0-45b3-83f9-c84bf6ef2d7e.original.png"},{"title":"003-dieren__a-fish03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/06979857-0680-4382-8e04-bf315ba58dc0.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/06979857-0680-4382-8e04-bf315ba58dc0.original.png"},{"title":"003-dieren__a-goat","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5b1b8b6c-963e-4ec4-b71a-bc28aee6f0f5.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5b1b8b6c-963e-4ec4-b71a-bc28aee6f0f5.original.png"},{"title":"003-dieren__a-haan","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/28d1d695-a4d9-424e-9384-e994e64fe0d8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/28d1d695-a4d9-424e-9384-e994e64fe0d8.original.png"},{"title":"003-dieren__a-horse","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c459a11e-03f5-42c9-ba22-179637b5124d.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c459a11e-03f5-42c9-ba22-179637b5124d.original.png"},{"title":"003-dieren__a-koala","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/763d2cff-9fa4-4804-ab92-b99731da5039.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/763d2cff-9fa4-4804-ab92-b99731da5039.original.png"},{"title":"003-dieren__a-monkey01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f1331be-ed8e-43c0-a7dd-ff42f94a6a0e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f1331be-ed8e-43c0-a7dd-ff42f94a6a0e.original.png"},{"title":"003-dieren__a-monkey02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ee6ccf85-0eed-4441-b3fd-6178941a9365.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ee6ccf85-0eed-4441-b3fd-6178941a9365.original.png"},{"title":"003-dieren__a-mouse","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4f827364-6363-416d-9575-594282fb9338.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4f827364-6363-416d-9575-594282fb9338.original.png"},{"title":"003-dieren__a-octopus","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/54e24149-2b3d-4fdd-a1fb-8517cf8e04fd.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/54e24149-2b3d-4fdd-a1fb-8517cf8e04fd.original.png"},{"title":"003-dieren__a-pig","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/290ed713-27fa-4d4a-99c4-e44ff0ff56e6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/290ed713-27fa-4d4a-99c4-e44ff0ff56e6.original.png"},{"title":"003-dieren__a-pinguin","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/943ebb59-02ea-4891-9cca-4e3709ac5d3a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/943ebb59-02ea-4891-9cca-4e3709ac5d3a.original.png"},{"title":"003-dieren__a-sheep","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1e524c0e-2d46-481c-a2d6-2bc0feb1aeb4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1e524c0e-2d46-481c-a2d6-2bc0feb1aeb4.original.png"},{"title":"003-dieren__a-snake","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ed820265-88d8-4a2f-805a-9df637c5223c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ed820265-88d8-4a2f-805a-9df637c5223c.original.png"},{"title":"003-dieren__a-spider","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2b8f570b-76b1-431e-ae87-553619fc5825.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2b8f570b-76b1-431e-ae87-553619fc5825.original.png"},{"title":"003-dieren__a-tiger01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/87ed9442-1d30-4f9f-ba8b-462bfc2cfba4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/87ed9442-1d30-4f9f-ba8b-462bfc2cfba4.original.png"},{"title":"003-dieren__a-tiger02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/46753813-1955-4a30-bd8e-e2a505566984.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/46753813-1955-4a30-bd8e-e2a505566984.original.png"},{"title":"003-dieren__a-tiger03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6a8f7904-9453-4ada-86c2-66f8863f6bf6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6a8f7904-9453-4ada-86c2-66f8863f6bf6.original.png"},{"title":"003-dieren__a-turtle","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7b3938d-2b55-493a-a1ba-6bd4839fea80.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7b3938d-2b55-493a-a1ba-6bd4839fea80.original.png"},{"title":"003-dieren__a-whale","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4699eef-794c-4c03-b512-fc57e4e4de24.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4699eef-794c-4c03-b512-fc57e4e4de24.original.png"},{"title":"003-dieren__b-bear","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8bf07105-7934-432c-8668-938a274f3b41.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8bf07105-7934-432c-8668-938a274f3b41.original.png"},{"title":"003-dieren__b-bunny","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f3808edf-27a8-41eb-8848-342205e2b1ee.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f3808edf-27a8-41eb-8848-342205e2b1ee.original.png"},{"title":"003-dieren__b-camel","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fdb62c6a-980e-40a9-8cd1-342d998a56f2.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fdb62c6a-980e-40a9-8cd1-342d998a56f2.original.png"},{"title":"003-dieren__b-cat01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/328b4aab-7a65-430d-8115-5a6d4519e856.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/328b4aab-7a65-430d-8115-5a6d4519e856.original.png"},{"title":"003-dieren__b-cat02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6d75fb32-5bf0-4fa0-8330-92ea56bcb02e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6d75fb32-5bf0-4fa0-8330-92ea56bcb02e.original.png"},{"title":"003-dieren__b-cat03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f8758276-a914-45e7-a00b-25ffe3e00ebb.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f8758276-a914-45e7-a00b-25ffe3e00ebb.original.png"},{"title":"003-dieren__b-cat04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d08d88c6-a571-4044-aa99-7210a363731c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d08d88c6-a571-4044-aa99-7210a363731c.original.png"},{"title":"003-dieren__b-cat05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6fc3bfa0-4a00-4dfb-a04c-d025b77ed82f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6fc3bfa0-4a00-4dfb-a04c-d025b77ed82f.original.png"},{"title":"003-dieren__b-dog","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/71d0172d-acca-4aae-9bb3-729941807156.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/71d0172d-acca-4aae-9bb3-729941807156.original.png"},{"title":"003-dieren__b-dragon","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/97a9e9fc-82ee-483b-8d32-328617f26070.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/97a9e9fc-82ee-483b-8d32-328617f26070.original.png"},{"title":"003-dieren__b-frog","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0ecbacbf-7a0c-404c-9f7b-e6deef335145.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0ecbacbf-7a0c-404c-9f7b-e6deef335145.original.png"},{"title":"003-dieren__b-horse","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6b2393a6-9758-4a8f-8b86-6a1ae7b6638f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6b2393a6-9758-4a8f-8b86-6a1ae7b6638f.original.png"},{"title":"003-dieren__b-lion01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f670f9c-259d-4be3-a2ae-3a2f74ba23e3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f670f9c-259d-4be3-a2ae-3a2f74ba23e3.original.png"},{"title":"003-dieren__b-lion02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7ab109bb-fddf-4072-92df-951dd63c3b8e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7ab109bb-fddf-4072-92df-951dd63c3b8e.original.png"},{"title":"003-dieren__b-monkey00","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e397833e-18fa-46fe-9287-88a7297e3553.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e397833e-18fa-46fe-9287-88a7297e3553.original.png"},{"title":"003-dieren__b-monkey01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3638a162-64ad-44ce-b825-7a4625035e6f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3638a162-64ad-44ce-b825-7a4625035e6f.original.png"},{"title":"003-dieren__b-monkey02a","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/14977fd1-7ef3-4da8-adf7-fe26c861b739.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/14977fd1-7ef3-4da8-adf7-fe26c861b739.original.png"},{"title":"003-dieren__b-monkey02b","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aad04fe4-7767-430e-8233-bf1a9c46b718.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aad04fe4-7767-430e-8233-bf1a9c46b718.original.png"},{"title":"003-dieren__b-monkey03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e03b0c3f-b1d2-4a56-a781-61f51b014aed.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e03b0c3f-b1d2-4a56-a781-61f51b014aed.original.png"},{"title":"003-dieren__b-monkey04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1859c504-0d13-4d3a-88f8-80c0b38e077c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1859c504-0d13-4d3a-88f8-80c0b38e077c.original.png"},{"title":"003-dieren__b-monkey05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7721d2fd-b76a-4e85-8ed2-523eb1370640.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7721d2fd-b76a-4e85-8ed2-523eb1370640.original.png"},{"title":"003-dieren__b-panda","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7aa7dc9c-d9af-4fc5-a707-e78e4afa8639.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7aa7dc9c-d9af-4fc5-a707-e78e4afa8639.original.png"},{"title":"003-dieren__b-pig00","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d58d6572-6314-4052-9eeb-185478c81c90.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d58d6572-6314-4052-9eeb-185478c81c90.original.png"},{"title":"003-dieren__b-pig01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b012a02e-c8fd-45b4-b97f-3a36b0484691.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b012a02e-c8fd-45b4-b97f-3a36b0484691.original.png"},{"title":"003-dieren__b-pig02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/cad29c0f-5756-421a-bbf1-81470109d06f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/cad29c0f-5756-421a-bbf1-81470109d06f.original.png"},{"title":"003-dieren__b-tiger","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e2fd5c3a-e8b3-419a-b1d2-d5b322b5fe42.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e2fd5c3a-e8b3-419a-b1d2-d5b322b5fe42.original.png"},{"title":"003-dieren__b-unicorn01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7392b54-b9de-47b3-8099-72bd3d0b89c7.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c7392b54-b9de-47b3-8099-72bd3d0b89c7.original.png"},{"title":"003-dieren__b-unicorn02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ce8c715d-f034-46ad-85d1-7483fb287f7a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ce8c715d-f034-46ad-85d1-7483fb287f7a.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/88531ca8-72b0-47c6-a75c-23c3ff80a2ab.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/88531ca8-72b0-47c6-a75c-23c3ff80a2ab.original.png"},"id":"ed93d548-63a7-4729-bec8-8fe9cbda2dd5","title":"003-animals"},{"emojis":[{"title":"004-sport__s-ball","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e0841320-7014-4b0f-96dc-0dac8d678329.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e0841320-7014-4b0f-96dc-0dac8d678329.original.png"},{"title":"004-sport__s-bike","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8edbddf7-ac6e-40be-afcb-8b5285413c8f.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8edbddf7-ac6e-40be-afcb-8b5285413c8f.original.png"},{"title":"004-sport__basebal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8594d919-21fa-40bc-9ee0-e7e3e8f7c8a8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8594d919-21fa-40bc-9ee0-e7e3e8f7c8a8.original.png"},{"title":"004-sport__basketbal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b6fb2fd0-f915-4c60-a890-fdffc1082479.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b6fb2fd0-f915-4c60-a890-fdffc1082479.original.png"},{"title":"004-sport__fiets","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/58bc95a9-81e6-4cab-ada3-0314cd3b73f8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/58bc95a9-81e6-4cab-ada3-0314cd3b73f8.original.png"},{"title":"004-sport__golfbal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/98c6746f-b21d-40b7-8b34-04996126e75e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/98c6746f-b21d-40b7-8b34-04996126e75e.original.png"},{"title":"004-sport__pingpong","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0cb4030e-abbf-462b-b5f9-b872479cf443.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0cb4030e-abbf-462b-b5f9-b872479cf443.original.png"},{"title":"004-sport__rugbybal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f373b4af-a33a-4973-a9b3-c353c460f5c3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f373b4af-a33a-4973-a9b3-c353c460f5c3.original.png"},{"title":"004-sport__ski2","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f9bf13e0-f9c9-4eaa-b5ed-21b0e821d628.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f9bf13e0-f9c9-4eaa-b5ed-21b0e821d628.original.png"},{"title":"004-sport__surf","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/964d2832-26c5-461b-89b5-895a34cabbe6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/964d2832-26c5-461b-89b5-895a34cabbe6.original.png"},{"title":"004-sport__surf2","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f4d56135-af8e-4446-88aa-ae59a0a846c6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f4d56135-af8e-4446-88aa-ae59a0a846c6.original.png"},{"title":"004-sport__tennisbal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/987d677f-d3e9-477f-8339-6ace4c8ab5a7.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/987d677f-d3e9-477f-8339-6ace4c8ab5a7.original.png"},{"title":"004-sport__tennisracket2","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/553e75f2-2ab0-45be-af21-a46c2e832f46.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/553e75f2-2ab0-45be-af21-a46c2e832f46.original.png"},{"title":"004-sport__volleybal","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/03c5fed0-acf9-4f2c-bc62-f3d173ecd6fc.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/03c5fed0-acf9-4f2c-bc62-f3d173ecd6fc.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e0841320-7014-4b0f-96dc-0dac8d678329.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/e0841320-7014-4b0f-96dc-0dac8d678329.original.png"},"id":"30ae1d2f-dbec-4069-93cc-0bc4352d25eb","title":"004-sport"},{"emojis":[{"title":"005-objecten__a-food01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d2312d6f-2ddb-470f-b2f3-383d067439ff.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d2312d6f-2ddb-470f-b2f3-383d067439ff.original.png"},{"title":"005-objecten__a-food02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6f53bf58-dbb1-49a5-b42d-5a7126fe5e25.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/6f53bf58-dbb1-49a5-b42d-5a7126fe5e25.original.png"},{"title":"005-objecten__a-food03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5b44cebb-8f7f-48d2-8cc3-90549f8d0564.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5b44cebb-8f7f-48d2-8cc3-90549f8d0564.original.png"},{"title":"005-objecten__a-food04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8915ffb9-ea83-4f76-a39a-9fd561326d8c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8915ffb9-ea83-4f76-a39a-9fd561326d8c.original.png"},{"title":"005-objecten__a-food05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2d88ca38-8fba-4c0b-9a26-c921e0733292.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2d88ca38-8fba-4c0b-9a26-c921e0733292.original.png"},{"title":"005-objecten__a-food06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/40c05b12-fe63-4d98-af02-2fa048406f09.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/40c05b12-fe63-4d98-af02-2fa048406f09.original.png"},{"title":"005-objecten__a-food07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d531d754-1212-46b1-b2c1-3e0369201b9c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d531d754-1212-46b1-b2c1-3e0369201b9c.original.png"},{"title":"005-objecten__a-food08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/74084913-a3cd-4301-8cc8-7f370aee07e4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/74084913-a3cd-4301-8cc8-7f370aee07e4.original.png"},{"title":"005-objecten__a-food10","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ca0bbc93-b629-4f38-97db-a4725e81967b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ca0bbc93-b629-4f38-97db-a4725e81967b.original.png"},{"title":"005-objecten__a-food11","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/abd73306-5d8c-4ad5-9fe0-1c7b69cf33d1.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/abd73306-5d8c-4ad5-9fe0-1c7b69cf33d1.original.png"},{"title":"005-objecten__a-food12","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d54cb87b-61b4-4d26-8c1c-5088cc56d263.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d54cb87b-61b4-4d26-8c1c-5088cc56d263.original.png"},{"title":"005-objecten__a-food13","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/078c4e40-91f2-4485-8c8b-509a0e4bdc24.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/078c4e40-91f2-4485-8c8b-509a0e4bdc24.original.png"},{"title":"005-objecten__a-food14","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/16bc05bf-58e5-4dab-a8a5-d5fe1670c001.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/16bc05bf-58e5-4dab-a8a5-d5fe1670c001.original.png"},{"title":"005-objecten__a-food15","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9002359a-8a9a-4158-879a-6415b75a4e29.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9002359a-8a9a-4158-879a-6415b75a4e29.original.png"},{"title":"005-objecten__a-food16","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a58c46e6-54dc-4680-85cb-dd312e75a05b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a58c46e6-54dc-4680-85cb-dd312e75a05b.original.png"},{"title":"005-objecten__b-nature01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/11510420-0f57-4163-b90c-3900cfe15971.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/11510420-0f57-4163-b90c-3900cfe15971.original.png"},{"title":"005-objecten__b-nature02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1d40ef20-4a95-4abb-a6da-7de44790c79c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1d40ef20-4a95-4abb-a6da-7de44790c79c.original.png"},{"title":"005-objecten__b-nature03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2866dd9e-bda1-4ee5-bacf-4570d45c7cf4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2866dd9e-bda1-4ee5-bacf-4570d45c7cf4.original.png"},{"title":"005-objecten__b-nature04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5500a785-29aa-4839-b779-719b16eb87f3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/5500a785-29aa-4839-b779-719b16eb87f3.original.png"},{"title":"005-objecten__b-nature05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/73ca314c-58ce-4440-86e3-c589321528df.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/73ca314c-58ce-4440-86e3-c589321528df.original.png"},{"title":"005-objecten__b-nature06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/31e2efbf-bdfc-4d48-bfa4-b6d1aade6d75.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/31e2efbf-bdfc-4d48-bfa4-b6d1aade6d75.original.png"},{"title":"005-objecten__b-nature07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/427be1c9-4c3f-447d-88ee-189503b40d9b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/427be1c9-4c3f-447d-88ee-189503b40d9b.original.png"},{"title":"005-objecten__c-congrats01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fbbcb3be-7d8e-49e9-9512-bd3c4b6ce28a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fbbcb3be-7d8e-49e9-9512-bd3c4b6ce28a.original.png"},{"title":"005-objecten__c-congrats02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0ae91d16-1c7b-4c9f-94c3-fe4b70b0accb.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0ae91d16-1c7b-4c9f-94c3-fe4b70b0accb.original.png"},{"title":"005-objecten__c-congrats03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0e914c23-8118-4305-a557-dbf6164f3a10.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/0e914c23-8118-4305-a557-dbf6164f3a10.original.png"},{"title":"005-objecten__c-congrats04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bf5ea5d1-202f-4545-87d3-cf8e0aef26fa.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bf5ea5d1-202f-4545-87d3-cf8e0aef26fa.original.png"},{"title":"005-objecten__c-congrats05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c2fbc666-5a66-4128-9485-a228e80e1bf3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/c2fbc666-5a66-4128-9485-a228e80e1bf3.original.png"},{"title":"005-objecten__c-congrats06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/09d65b0b-e11a-4f1f-bb48-8354c4079ced.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/09d65b0b-e11a-4f1f-bb48-8354c4079ced.original.png"},{"title":"005-objecten__c-congrats07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa65ee34-f4dd-49e9-bb01-12bf2ac969ce.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa65ee34-f4dd-49e9-bb01-12bf2ac969ce.original.png"},{"title":"005-objecten__d-music01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/dd22bce7-ac8e-44c6-8451-730325771816.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/dd22bce7-ac8e-44c6-8451-730325771816.original.png"},{"title":"005-objecten__d-music02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/20a751c7-4046-4c4e-ac1a-5596183e3f77.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/20a751c7-4046-4c4e-ac1a-5596183e3f77.original.png"},{"title":"005-objecten__d-music03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fb61a704-d936-4988-844d-b7eacf793958.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fb61a704-d936-4988-844d-b7eacf793958.original.png"},{"title":"005-objecten__d-music04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ccfe59a3-03bc-4cec-8ec0-528bf4c9c3a5.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ccfe59a3-03bc-4cec-8ec0-528bf4c9c3a5.original.png"},{"title":"005-objecten__e-text01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1fd3af46-8881-45e7-8abe-4a9c286b35e2.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/1fd3af46-8881-45e7-8abe-4a9c286b35e2.original.png"},{"title":"005-objecten__e-text02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f6907fca-870c-46b7-af48-6778c0e3662b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/f6907fca-870c-46b7-af48-6778c0e3662b.original.png"},{"title":"005-objecten__e-text03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/84e0168e-9904-470b-8aee-e5e45754af09.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/84e0168e-9904-470b-8aee-e5e45754af09.original.png"},{"title":"005-objecten__e-text04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7e44089b-55f9-4efb-94b7-dea20025960a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7e44089b-55f9-4efb-94b7-dea20025960a.original.png"},{"title":"005-objecten__e-text05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8965159e-d1ec-4d80-8dad-a05439e04deb.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/8965159e-d1ec-4d80-8dad-a05439e04deb.original.png"},{"title":"005-objecten__e-text06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b97941d4-095d-432a-83f5-68de1a49f8b4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b97941d4-095d-432a-83f5-68de1a49f8b4.original.png"},{"title":"005-objecten__f-transport01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d96a1b9c-605d-422a-a6e2-cd51df9d392e.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d96a1b9c-605d-422a-a6e2-cd51df9d392e.original.png"},{"title":"005-objecten__f-transport02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b3366ac4-51e6-44c2-a51a-29f1d0979e0a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/b3366ac4-51e6-44c2-a51a-29f1d0979e0a.original.png"},{"title":"005-objecten__f-transport03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fd089265-5a5c-4428-8381-4e877de135f8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fd089265-5a5c-4428-8381-4e877de135f8.original.png"},{"title":"005-objecten__f-transport04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4f8bb73a-5a47-42a0-b11e-79a44278db7a.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4f8bb73a-5a47-42a0-b11e-79a44278db7a.original.png"},{"title":"005-objecten__g-clothing01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2daace3e-dee0-4d1f-9acb-7e558c1cc751.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/2daace3e-dee0-4d1f-9acb-7e558c1cc751.original.png"},{"title":"005-objecten__g-clothing02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f05379b-476f-482f-a459-931b2f426f50.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f05379b-476f-482f-a459-931b2f426f50.original.png"},{"title":"005-objecten__g-clothing03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f888d90-3d99-4157-9b7c-26c222a70e80.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/3f888d90-3d99-4157-9b7c-26c222a70e80.original.png"},{"title":"005-objecten__g-clothing04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9a868692-2eec-406d-ab0d-7fc4ddeeb3d8.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9a868692-2eec-406d-ab0d-7fc4ddeeb3d8.original.png"},{"title":"005-objecten__g-clothing05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/df77ea4b-7fbd-4ad9-befd-11e08fa91a72.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/df77ea4b-7fbd-4ad9-befd-11e08fa91a72.original.png"},{"title":"005-objecten__g-clothing06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a4cc85bb-6c26-4197-bf92-8fddfcb6d657.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a4cc85bb-6c26-4197-bf92-8fddfcb6d657.original.png"},{"title":"005-objecten__h-clothing07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4e0e955-1c92-449d-812a-04425800d759.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d4e0e955-1c92-449d-812a-04425800d759.original.png"},{"title":"005-objecten__h-divers01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a9bc5a11-0980-44d2-b7bd-333309f4285c.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a9bc5a11-0980-44d2-b7bd-333309f4285c.original.png"},{"title":"005-objecten__h-divers02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/26a571b9-618a-42b9-a0d8-cb02d5989540.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/26a571b9-618a-42b9-a0d8-cb02d5989540.original.png"},{"title":"005-objecten__h-divers03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/079961dc-28f7-420c-82e1-feee378f7b9d.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/079961dc-28f7-420c-82e1-feee378f7b9d.original.png"},{"title":"005-objecten__h-divers04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4d3372a9-2f42-4508-aa5f-cedadd93ad4b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/4d3372a9-2f42-4508-aa5f-cedadd93ad4b.original.png"},{"title":"005-objecten__h-divers05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fa3d6fd2-e404-4666-b16d-5c472e817e77.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/fa3d6fd2-e404-4666-b16d-5c472e817e77.original.png"},{"title":"005-objecten__h-divers06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d1f2a730-ae3f-4956-927a-f2217a12c52b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d1f2a730-ae3f-4956-927a-f2217a12c52b.original.png"},{"title":"005-objecten__h-divers07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/393ec2eb-ddc1-4427-bea3-4134112a8b63.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/393ec2eb-ddc1-4427-bea3-4134112a8b63.original.png"},{"title":"005-objecten__h-divers08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9359fc83-c661-4a5e-ac1b-85a1308cde8b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/9359fc83-c661-4a5e-ac1b-85a1308cde8b.original.png"},{"title":"005-objecten__h-divers09","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/12ce7ac0-807a-4b97-95ed-eeedaf04a141.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/12ce7ac0-807a-4b97-95ed-eeedaf04a141.original.png"},{"title":"005-objecten__h-divers10","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/63b15ae3-7e26-4a9d-965c-60e9c4209f35.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/63b15ae3-7e26-4a9d-965c-60e9c4209f35.original.png"},{"title":"005-objecten__h-divers11","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f0c48fe-6b02-408d-9cbc-5c95160ef683.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7f0c48fe-6b02-408d-9cbc-5c95160ef683.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d2312d6f-2ddb-470f-b2f3-383d067439ff.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d2312d6f-2ddb-470f-b2f3-383d067439ff.original.png"},"id":"800e75aa-16e3-4d32-aaa8-b20bc9682c98","title":"005-objects"},{"emojis":[{"title":"005-weer__a-weer01","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/10f24dae-5ed3-490d-adfe-2ebc7b0ccaa6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/10f24dae-5ed3-490d-adfe-2ebc7b0ccaa6.original.png"},{"title":"005-weer__a-weer02","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bdd4b3f3-4741-4c00-ba4c-7d10c9af752b.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/bdd4b3f3-4741-4c00-ba4c-7d10c9af752b.original.png"},{"title":"005-weer__a-weer03","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/055a1f83-bd42-4e5f-a510-4062944e56ff.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/055a1f83-bd42-4e5f-a510-4062944e56ff.original.png"},{"title":"005-weer__a-weer04","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7ba3d7fa-032a-4074-b604-e5463ef8d687.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/7ba3d7fa-032a-4074-b604-e5463ef8d687.original.png"},{"title":"005-weer__a-weer05","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d5a46386-4a8c-436b-bc4e-d6bed0046339.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d5a46386-4a8c-436b-bc4e-d6bed0046339.original.png"},{"title":"005-weer__a-weer06","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d83a87ab-52a6-441d-a4c7-9078293ee8da.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/d83a87ab-52a6-441d-a4c7-9078293ee8da.original.png"},{"title":"005-weer__a-weer07","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/34b23010-b039-4f5f-a27f-5a5e7ec0b9a4.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/34b23010-b039-4f5f-a27f-5a5e7ec0b9a4.original.png"},{"title":"005-weer__a-weer08","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/70ba2151-4ab6-4ecf-b56c-54aedb172e4d.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/70ba2151-4ab6-4ecf-b56c-54aedb172e4d.original.png"},{"title":"005-weer__a-weer09","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/669f3fac-217c-4e98-94cd-350f0e1e4513.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/669f3fac-217c-4e98-94cd-350f0e1e4513.original.png"},{"title":"005-weer__a-weer10","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a54c26f7-94f5-4abf-ab7a-1d7e9b05efd3.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a54c26f7-94f5-4abf-ab7a-1d7e9b05efd3.original.png"},{"title":"005-weer__a-weer11","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ad135439-3d07-4cd7-b6c9-78a41dfe3250.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/ad135439-3d07-4cd7-b6c9-78a41dfe3250.original.png"},{"title":"005-weer__a-weer12","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a0c970a1-1603-4955-b737-6c0eb827c816.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/a0c970a1-1603-4955-b737-6c0eb827c816.original.png"},{"title":"005-weer__a-weer13","url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/59a95ad9-a592-48cc-8b4b-803ab80aa5f9.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/59a95ad9-a592-48cc-8b4b-803ab80aa5f9.original.png"}],"icon":{"url":"http://localhost:14569/cdn.local.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/10f24dae-5ed3-490d-adfe-2ebc7b0ccaa6.original.png","id":"/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/10f24dae-5ed3-490d-adfe-2ebc7b0ccaa6.original.png"},"id":"737178d3-a13b-4b44-af2c-04f9a4b69475","title":"005-weather"}]},"settings":{"JWPLAYER_KEY":"0y/TpFS258Rn2+Nm1uKH161b8MDefnMrMRgenVs5y/4="},"createdAt":"2017-11-28T13:53:25.129Z","allowedInteractions":["media","shoutbox","emojis","polls"],"locales":{"selection":"browser","en":{"emojis":{},"polls":{"question":{"message":"Question:"},"nopoll":{"message":"There is no data available"},"closed":{"message":"Voting is no longer possible"}},"shoutbox":{"notloggedin":{"login":"Login","loginwith":"Login with"},"errors":{"blocked":"Your message has not been sent. Your profile is blocked.","resend":"Your message has not been sent. Please try again.","profanity":"Your message has not been sent. Watch your language."},"placeholder":{"blocked":"You can't leave a comment anymore. Your profile is blocked."}},"media":{"geoblocked":{"modal":{"title":"Livestream unavailable","body":"You can't see the requested livestream in this country.","button":"OK"},"pancarte":{"text":"This video is not available in your country."}},"noflash":{"modal":{"title":"Error while playing","body":"This livestream is only viewable with Flash. We are working on a solution to play livestreams without Flash in the future.","button":"OK"},"pancarte":{"text":"Your device/browser is not compatible to play this video."}},"playbackerror":{"modal":{"title":"Error while playing","body":"This livestream can't be loaded. Please try again later.","button":"OK"},"pancarte":{"text":"There was an error encountered while loading this video."}}},"auth":{"blocked":{"modal":{"title":"Blocked","body":"Your comment seems inappropriate. You were blocked.","button":"OK"}},"failed":{"modal":{"body":"Please try again","button":"OK","title":"Error while logging in"}}},"stream":{"nostreams":{"pancarte":{"text":"There are currently no broadcasts available."}},"limitedexperience":{"modal":{"title":"You can't leave a comment.","body":"Download our app or visit our website with a computer to leave a comment.","button":"OK"}},"state":{"live":"Live in"}}},"default":{"emojis":{},"polls":{"question":{"message":"Vraag:"},"closed":{"message":"Stemmen is niet meer mogelijk"},"nopoll":{"message":"Momenteel is er geen data beschikbaar"}},"shoutbox":{"notloggedin":{"login":"Meld je aan.","loginwith":"Aanmelden met"},"errors":{"blocked":"Je bericht is niet verstuurd. Je werd geblokkeerd.","resend":"Je bericht werd niet verstuurd. Probeer opnieuw aub.","profanity":"Je bericht is niet verstuurd. Let op je taalgebruik."},"placeholder":{"blocked":"Je kan niet meer reageren. Jouw profiel werd geblokkeerd."}},"media":{"geoblocked":{"modal":{"body":"De opgevraagde livestream kan je niet bekijken in het land waar je je nu bevindt.","button":"OK","title":"Livestream niet beschikbaar"},"pancarte":{"text":"Deze video is helaas niet beschikbaar in jouw land."}},"noflash":{"modal":{"body":"Deze livestream is alleen te bekijken met Flash. We werken aan een oplossing om livestreams in de toekomst ook zonder Flash af te spelen.","button":"OK","title":"Fout tijdens afspelen"},"pancarte":{"text":"Jouw toestel/browser voldoet niet om de video af te spelen."}},"playbackerror":{"modal":{"body":"De livestream kan niet worden ingeladen. Probeer het later nog eens opnieuw.","button":"OK","title":"Fout tijdens afspelen"},"pancarte":{"text":"Er is een probleem bij het inladen van de video."}}},"auth":{"blocked":{"modal":{"body":"Je hebt ongepaste berichten geplaatst. Je werd geblokkeerd.","button":"OK","title":"Geblokkeerd"}},"failed":{"modal":{"body":"Gelieve het opnieuw te proberen","button":"OK","title":"Fout bij aanmelden"}}},"stream":{"nostreams":{"pancarte":{"text":"Er zijn momenteel geen uitzendingen beschikbaar."}},"limitedexperience":{"modal":{"body":"Download onze app of surf naar onze website met een computer om mee te reageren","button":"OK","title":"Je kan niet reageren"}},"state":{"live":"live binnen"}}}},"shoutbox":{"profanity":[{"matches":"exact","text":"something exact explicit"},{"matches":"contains","text":"something that contains explicit language"}]},"name":"zender-api","alias":"zender-api","id":"b8f99a0c-1383-4891-af7a-563b5903d390","updatedAt":"2017-11-29T08:55:53.903Z","config":{"auth":{"login":{"url":"http://localhost:3002/v1/auth/login"},"providers":{"youtube":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"google":{"clientId":"721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"},"facebook":{"enabled":true,"appId":690051904495300,"tokenUrl":"https://graph.facebook.com/me"}}},"pusher":{"config":{"encrypted":true,"cluster":"eu","authEndpoint":"http://localhost:3002/v1/pusher"},"key":"968089f2292502112add"},"search":{"url":"http://localhost:3008/v1/search","method":"POST"},"stories":{"url":"http://localhost:3007/v1/stories/all","method":"GET"},"notifications":{"url":"http://localhost:3001/v1/notifications","method":"GET"},"topics":[]}}
```



### 16. Delete All Shoutbox Messages


Delete a shoutbox messages.


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



## Player/Core



### 1. Get Target


Get a target by id or alias.

This is generally the first call the client will make since it contains all the necessary information to proceed.

A target contains configuration for accessing the different functionalities like authentication, pusher eventing, content upload, ... It also has information about theming, locales and ui related settings.

When fetching the target you also retrieve a list of associated channels.

It is possible to fetch the target by the human readable alias attribute instead of by the id (see "Get Target (by alias)" example).

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Get Target  | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/targets/{{targetId}}
```



***Responses:***


Status: Get Target (by alias) | Code: 200



```js
{
    "id": "2808b5c6-76a1-4d18-93f5-23ea9f6246da",
    "name": "zender-api",
    "alias": "zender-api",
    "config": {
        "auth": {
            "login": {
                "url": "https://api.zender.tv/v1/auth/login"
            },
            "providers": {
                "youtube": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "google": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "device": {},
                "facebook": {
                    "enabled": true,
                    "tokenUrl": "https://graph.facebook.com/me",
                    "appId": 690051904495300
                }
            }
        },
        "pusher": {
            "config": {
                "encrypted": true,
                "cluster": "eu",
                "authEndpoint": "https://api.zender.tv/v1/auth/pusher"
            },
            "key": "e03e32164a92e6ee8ed2"
        },
        "search": {
            "method": "POST",
            "url": "https://api.zender.tv/v1/search"
        },
        "upload": {
            "url": "https://api.zender.tv/v1/upload",
            "method": "POST"
        },
        "stories": {
            "url": "https://api.zender.tv/v1/stories/all",
            "method": "GET"
        },
        "notifications": {
            "method": "GET",
            "url": "https://api.zender.tv/v1/notifications"
        },
        "topics": [
            {
                "name": "standard stream notifications",
                "id": "5763a6d2-b3ab-4e6a-aee0-1ea63a06d354"
            },
            {
                "name": "hot stream notifications",
                "id": "be88e951-bbaf-4c16-a96a-f26da2eba763"
            }
        ]
    },
    "settings": {},
    "theming": {
        "misc": {
            "logo": {
                "square": "https://cdn.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-04-09/5db24024-5b64-4359-a43a-7e52dfc6baaf.original.png",
                "default": "https://cdn.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-04-09/5db24024-5b64-4359-a43a-7e52dfc6baaf.original.png"
            },
            "background": "https://cdn.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-03-29/4f768b4f-5c80-4b28-8c35-c48e767b234f.original.png"
        }
    },
    "locales": {
        "selection": "browser",
        "en": {
            "emojis": {},
            "polls": {
                "question": {
                    "message": "Question:"
                },
                "nopoll": {
                    "message": "There is no data available"
                },
                "closed": {
                    "message": "Voting is no longer possible"
                }
            },
            "shoutbox": {
                "notloggedin": {
                    "login": "Login",
                    "loginwith": "Login with"
                },
                "errors": {
                    "blocked": "Your message has not been sent. Your profile is blocked.",
                    "resend": "Your message has not been sent. Please try again.",
                    "profanity": "Your message has not been sent. Watch your language."
                },
                "placeholder": {
                    "blocked": "You can't leave a comment anymore. Your profile is blocked."
                }
            },
            "media": {
                "geoblocked": {
                    "modal": {
                        "title": "Livestream unavailable",
                        "body": "You can't see the requested livestream in this country.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "This video is not available in your country."
                    }
                },
                "noflash": {
                    "modal": {
                        "title": "Error while playing",
                        "body": "This livestream is only viewable with Flash. We are working on a solution to play livestreams without Flash in the future.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "Your device/browser is not compatible to play this video."
                    }
                },
                "playbackerror": {
                    "modal": {
                        "title": "Error while playing",
                        "body": "This livestream can't be loaded. Please try again later.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "There was an error encountered while loading this video."
                    }
                }
            },
            "auth": {
                "blocked": {
                    "modal": {
                        "title": "Blocked",
                        "body": "Your comment seems inappropriate. You were blocked.",
                        "button": "OK"
                    }
                },
                "failed": {
                    "modal": {
                        "body": "Please try again",
                        "button": "OK",
                        "title": "Error while logging in"
                    }
                }
            },
            "stream": {
                "nostreams": {
                    "pancarte": {
                        "text": "There are currently no broadcasts available."
                    }
                },
                "limitedexperience": {
                    "modal": {
                        "title": "You can't leave a comment.",
                        "body": "Download our app or visit our website with a computer to leave a comment.",
                        "button": "OK"
                    }
                },
                "state": {
                    "live": "Live in"
                }
            }
        },
        "default": {
            "emojis": {},
            "polls": {
                "question": {
                    "message": "Vraag:"
                },
                "closed": {
                    "message": "Stemmen is niet meer mogelijk"
                },
                "nopoll": {
                    "message": "Momenteel is er geen data beschikbaar"
                }
            },
            "shoutbox": {
                "notloggedin": {
                    "login": "Meld je aan.",
                    "loginwith": "Aanmelden met"
                },
                "errors": {
                    "blocked": "Je bericht is niet verstuurd. Je werd geblokkeerd.",
                    "resend": "Je bericht werd niet verstuurd. Probeer opnieuw aub.",
                    "profanity": "Je bericht is niet verstuurd. Let op je taalgebruik."
                },
                "placeholder": {
                    "blocked": "Je kan niet meer reageren. Jouw profiel werd geblokkeerd."
                }
            },
            "media": {
                "geoblocked": {
                    "modal": {
                        "body": "De opgevraagde livestream kan je niet bekijken in het land waar je je nu bevindt.",
                        "button": "OK",
                        "title": "Livestream niet beschikbaar"
                    },
                    "pancarte": {
                        "text": "Deze video is helaas niet beschikbaar in jouw land."
                    }
                },
                "noflash": {
                    "modal": {
                        "body": "Deze livestream is alleen te bekijken met Flash. We werken aan een oplossing om livestreams in de toekomst ook zonder Flash af te spelen.",
                        "button": "OK",
                        "title": "Fout tijdens afspelen"
                    },
                    "pancarte": {
                        "text": "Jouw toestel/browser voldoet niet om de video af te spelen."
                    }
                },
                "playbackerror": {
                    "modal": {
                        "body": "De livestream kan niet worden ingeladen. Probeer het later nog eens opnieuw.",
                        "button": "OK",
                        "title": "Fout tijdens afspelen"
                    },
                    "pancarte": {
                        "text": "Er is een probleem bij het inladen van de video."
                    }
                }
            },
            "auth": {
                "blocked": {
                    "modal": {
                        "body": "Je hebt ongepaste berichten geplaatst. Je werd geblokkeerd.",
                        "button": "OK",
                        "title": "Geblokkeerd"
                    }
                },
                "failed": {
                    "modal": {
                        "body": "Gelieve het opnieuw te proberen",
                        "button": "OK",
                        "title": "Fout bij aanmelden"
                    }
                }
            },
            "stream": {
                "nostreams": {
                    "pancarte": {
                        "text": "Er zijn momenteel geen uitzendingen beschikbaar."
                    }
                },
                "limitedexperience": {
                    "modal": {
                        "body": "Download onze app of surf naar onze website met een computer om mee te reageren",
                        "button": "OK",
                        "title": "Je kan niet reageren"
                    }
                },
                "state": {
                    "live": "live binnen"
                }
            }
        }
    },
    "status": {
        "code": "ok"
    },
    "channels": [
        {
            "id": "3789b16d-8e9d-4071-9209-2dae67be3760",
            "name": "Zender Trivia channel",
            "createdAt": "2018-03-05T13:18:06.247Z"
        }
    ]
}
```



Status: Get Target (by id) | Code: 200



```js
{
    "id": "b8f99a0c-1383-4891-af7a-563b5903d390",
    "name": "zender-api",
    "alias": "zender-api",
    "config": {
        "auth": {
            "login": {
                "url": "{{authApiEndpoint}}/v1/auth/login"
            },
            "providers": {
                "youtube": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "google": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "facebook": {
                    "enabled": true,
                    "appId": 690051904495300,
                    "tokenUrl": "https://graph.facebook.com/me"
                }
            }
        },
        "pusher": {
            "config": {
                "encrypted": true,
                "cluster": "eu",
                "authEndpoint": "{{coreApiEndpoint}}/v1/pusher"
            },
            "key": "968089f2292502112add"
        },
        "search": {
            "url": "{{coreApiEndpoint}}/v1/search",
            "method": "POST"
        },
        "stories": {
            "url": "{{coreApiEndpoint}}/v1/stories/all",
            "method": "GET"
        },
        "notifications": {
            "url": "{{coreApiEndpoint}}/v1/notifications",
            "method": "GET"
        },
        "topics": [
            {
                "name": "standard stream notifications",
                "id": "5763a6d2-b3ab-4e6a-aee0-1ea63a06d354"
            },
            {
                "name": "hot stream notifications",
                "id": "be88e951-bbaf-4c16-a96a-f26da2eba763"
            }
        ]
    },
    "settings": {},
    "theming": {},
    "locales": {
        "selection": "browser",
        "en": {
            "emojis": {},
            "polls": {
                "question": {
                    "message": "Question:"
                },
                "nopoll": {
                    "message": "There is no data available"
                },
                "closed": {
                    "message": "Voting is no longer possible"
                }
            },
            "shoutbox": {
                "notloggedin": {
                    "login": "Login",
                    "loginwith": "Login with"
                },
                "errors": {
                    "blocked": "Your message has not been sent. Your profile is blocked.",
                    "resend": "Your message has not been sent. Please try again.",
                    "profanity": "Your message has not been sent. Watch your language."
                },
                "placeholder": {
                    "blocked": "You can't leave a comment anymore. Your profile is blocked."
                }
            },
            "media": {
                "geoblocked": {
                    "modal": {
                        "title": "Livestream unavailable",
                        "body": "You can't see the requested livestream in this country.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "This video is not available in your country."
                    }
                },
                "noflash": {
                    "modal": {
                        "title": "Error while playing",
                        "body": "This livestream is only viewable with Flash. We are working on a solution to play livestreams without Flash in the future.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "Your device/browser is not compatible to play this video."
                    }
                },
                "playbackerror": {
                    "modal": {
                        "title": "Error while playing",
                        "body": "This livestream can't be loaded. Please try again later.",
                        "button": "OK"
                    },
                    "pancarte": {
                        "text": "There was an error encountered while loading this video."
                    }
                }
            },
            "auth": {
                "blocked": {
                    "modal": {
                        "title": "Blocked",
                        "body": "Your comment seems inappropriate. You were blocked.",
                        "button": "OK"
                    }
                },
                "failed": {
                    "modal": {
                        "body": "Please try again",
                        "button": "OK",
                        "title": "Error while logging in"
                    }
                }
            },
            "stream": {
                "nostreams": {
                    "pancarte": {
                        "text": "There are currently no broadcasts available."
                    }
                },
                "limitedexperience": {
                    "modal": {
                        "title": "You can't leave a comment.",
                        "body": "Download our app or visit our website with a computer to leave a comment.",
                        "button": "OK"
                    }
                },
                "state": {
                    "live": "Live in"
                }
            }
        },
        "default": {
            "emojis": {},
            "polls": {
                "question": {
                    "message": "Vraag:"
                },
                "closed": {
                    "message": "Stemmen is niet meer mogelijk"
                },
                "nopoll": {
                    "message": "Momenteel is er geen data beschikbaar"
                }
            },
            "shoutbox": {
                "notloggedin": {
                    "login": "Meld je aan.",
                    "loginwith": "Aanmelden met"
                },
                "errors": {
                    "blocked": "Je bericht is niet verstuurd. Je werd geblokkeerd.",
                    "resend": "Je bericht werd niet verstuurd. Probeer opnieuw aub.",
                    "profanity": "Je bericht is niet verstuurd. Let op je taalgebruik."
                },
                "placeholder": {
                    "blocked": "Je kan niet meer reageren. Jouw profiel werd geblokkeerd."
                }
            },
            "media": {
                "geoblocked": {
                    "modal": {
                        "body": "De opgevraagde livestream kan je niet bekijken in het land waar je je nu bevindt.",
                        "button": "OK",
                        "title": "Livestream niet beschikbaar"
                    },
                    "pancarte": {
                        "text": "Deze video is helaas niet beschikbaar in jouw land."
                    }
                },
                "noflash": {
                    "modal": {
                        "body": "Deze livestream is alleen te bekijken met Flash. We werken aan een oplossing om livestreams in de toekomst ook zonder Flash af te spelen.",
                        "button": "OK",
                        "title": "Fout tijdens afspelen"
                    },
                    "pancarte": {
                        "text": "Jouw toestel/browser voldoet niet om de video af te spelen."
                    }
                },
                "playbackerror": {
                    "modal": {
                        "body": "De livestream kan niet worden ingeladen. Probeer het later nog eens opnieuw.",
                        "button": "OK",
                        "title": "Fout tijdens afspelen"
                    },
                    "pancarte": {
                        "text": "Er is een probleem bij het inladen van de video."
                    }
                }
            },
            "auth": {
                "blocked": {
                    "modal": {
                        "body": "Je hebt ongepaste berichten geplaatst. Je werd geblokkeerd.",
                        "button": "OK",
                        "title": "Geblokkeerd"
                    }
                },
                "failed": {
                    "modal": {
                        "body": "Gelieve het opnieuw te proberen",
                        "button": "OK",
                        "title": "Fout bij aanmelden"
                    }
                }
            },
            "stream": {
                "nostreams": {
                    "pancarte": {
                        "text": "Er zijn momenteel geen uitzendingen beschikbaar."
                    }
                },
                "limitedexperience": {
                    "modal": {
                        "body": "Download onze app of surf naar onze website met een computer om mee te reageren",
                        "button": "OK",
                        "title": "Je kan niet reageren"
                    }
                },
                "state": {
                    "live": "live binnen"
                }
            }
        }
    },
    "status": {
        "code": "ok"
    },
    "channels": [
        {
            "id": "67b5528a-baf4-41bc-b558-b36613ee14a4",
            "name": "Zender Api Channel",
            "createdAt": "2017-11-28T13:54:56.714Z"
        }
    ]
}
```



### 2. Anonymous Token Login


Login by fetching an anonymous bearer token.

Only the targetId must be provided. Be aware that not all public functionality will be accessible with this obtained token. For instance the sending of a shoutbox message, the casting of a poll vote and the answering of quiz question can be configured to only accept calls of a user that was logged in through a provider (See [Provider Token Login](#bdcaea10-f58a-6019-aa49-25a5c78f9b14)).

For further reference a user that is logged in through this call will have the role 'anonymous' assigned. A user that is logged in with a provider has the role 'user' assigned. The bearer token in the response must be send as Authorization header for subsequent requests.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Anonymous Token Login | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/login
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "targetId": "{{targetId}}"
}
```



***Responses:***


Status: Anonymous Token Login | Code: 200



```js
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "user": {
        "id": "7b0f4d85-90c0-40f6-aeff-8f1c7c877337",
        "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
        "role": "anonymous"
    }
}
```



### 3. Provider Token Login


Login by fetching an provider user bearer token.

This endpoint can be used to login with the different providers (facebook, instagram, google, ...) See the examples for the different requests.

A user that is logged in with a provider has the role 'user' assigned. The bearer token in the response must be send as Authorization header for subsequent requests.

| Permissions          | no token | anonymous token | provider token | admin token |
| -------------------- | :------: | :-------------: | :------------: | :---------: |
| Provider Token Login | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{authApiHost}}/v1/auth/login
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "targetId": "{{targetId}}",
  "provider": "googleweb",
  "token": "{{google-token}}",
  "clientId": "{{google-client-id}}"
}
```



***Responses:***


Status: Google Provider Token Login | Code: 200



```js
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "user": {
        "provider": {
            "uid": "114183937812290902494",
            "name": "googleweb"
        },
        "targetId": "e878ecf0-31b9-11e8-883b-150a4ff79cb7",
        "authenticated": true,
        "avatar": "https://lh3.googleusercontent.com/-XdUIqdMkCZA/AAAAAAAAAAI/AAAAAAAAAAA/4252rscbv5M/photo.jpg?sz=50",
        "name": "John Doe",
        "externalId": "e878ecf0-31b9-11e8-883b-150a4ff79cb7_114183937812290902494",
        "id": "76ba109d-0408-42a5-ba6a-5858cb4288eb",
        "createdAt": "2018-04-16T11:22:28.398Z",
        "role": "user"
    }
}
```



Status: Facebook Provider Token Login | Code: 200



```js
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "user": {
        "authenticated": true,
        "createdAt": "2017-11-29T08:33:42.090Z",
        "role": "user",
        "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
        "provider": {
            "name": "facebook",
            "uid": "1459894774070695"
        },
        "name": "John Doe",
        "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_1459394774070695",
        "avatar": "https://graph.facebook.com/1559394774070695/picture?width=250&type=square",
        "id": "8184fbdc-6861-4fc5-9944-e7860b95f4df",
        "updatedAt": "2017-11-29T08:34:36.952Z"
    }
}
```



### 4. Get Target Channels


Gets all the available channels of a target.

| Permissions         | no token | anonymous token | provider token | admin token |
| ------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Channel Streams | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Target Channels (success) | Code: 200



```js
[{"targetId":"2808b5c6-76a1-4d18-93f5-23ea9f6246da","icon":"https://s3-eu-west-1.amazonaws.com/cdn.staging.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-04-03/43f4631e-7be1-4dad-acdf-1afa70225b2f.original.png","iconColor":"#B93D87","updatedAt":"2018-04-03T14:00:56.702Z","createdAt":"2018-03-05T13:18:06.247Z","headerColor":"#B93D87","id":"3789b16d-8e9d-4071-9209-2dae67be3760","name":"Zender Trivia channel","type":"streams"}]
```



### 5. Get Channel


Retrieve the info of a channel by id.

A channel can be viewed as a collection of streams.

It contains the links to its underlying streams (and stories).

When you're not logged in yet, the config contained in the response provides the login endpoint and the possible providers you can use. See [Provider Token Login](#bdcaea10-f58a-6019-aa49-25a5c78f9b14) on how to login.

The [Pusher](https://pusher.com) info is also provided in the response.

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Get Channel | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}
```



***Responses:***


Status: Get Channel | Code: 200



```js
{
    "stories": [],
    "preview": {
        "width": 579,
        "type": "image",
        "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
        "height": 580
    },
    "createdAt": "2017-11-28T13:54:56.714Z",
    "headerColor": "#000000",
    "targetId": "b8f99a0c-1383-4891-af7a-563b5903d390",
    "headerImage": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
    "icon": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
    "iconColor": "#000000",
    "name": "Zender Api Channel",
    "id": "67b5528a-baf4-41bc-b558-b36613ee14a4",
    "type": "streams",
    "updatedAt": "2017-11-28T13:55:16.192Z",
    "streams": [
        {
            "preview": {
                "type": "image",
                "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"
            },
            "createdAt": "2017-11-28T13:55:31.569Z",
            "airdate": "2017-11-27T10:30:00.000Z",
            "custom": {
                "splash_enabled": true,
                "splash_url": "https://zender.tv",
                "splash_loginrequired": false
            },
            "description": "Zender API Stream Update",
            "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "published": true,
            "state": "live",
            "userCount": 10,
            "title": "Zender API Stream",
            "channelId": "67b5528a-baf4-41bc-b558-b36613ee14a4",
            "updatedAt": "2017-11-28T13:55:43.800Z"
        }
    ],
    "config": {
        "auth": {
            "login": {
                "url": "{{authApiHost}}/v1/auth/login"
            },
            "providers": {
                "youtube": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "google": {
                    "clientId": "721563578034-8h5gt7grfb857fsisbom90ln2k1n747h.apps.googleusercontent.com"
                },
                "facebook": {
                    "enabled": true,
                    "appId": 690051904495300,
                    "tokenUrl": "https://graph.facebook.com/me"
                }
            }
        },
        "pusher": {
            "config": {
                "encrypted": true,
                "cluster": "eu",
                "authEndpoint": "{{coreApiHost}}/v1/pusher"
            },
            "key": "968089f2292502112add"
        },
        "streams": {
            "url": "{{coreApiHost}}/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams"
        },
        "stories": {
            "url": "{{coreApiHost}}/v1/stories/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/stories"
        }
    }
}
```



### 6. Get Channel Streams


Get all the published streams of a channel.

The response will only contain streams that have the "published" attribute set to true.

| Permissions         | no token | anonymous token | provider token | admin token |
| ------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Channel Streams | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Channel Streams | Code: 200



```js
[{"s3CdnImageRegExp":"https://s3-eu-west-1.amazonaws.com/(.*)(.original[.|/]|.large[.|/]|.medium[.|/]|.small[.|/])(.*)","published":true,"airdate":"2018-06-25T12:41:00.000Z","createdAt":"2018-06-25T12:42:25.624Z","preview":{"type":"image","url":"https://s3-eu-west-1.amazonaws.com/cdn.staging.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-06-25/792ccdff-e4e8-47cd-bb73-ded58a8f582a.original.png"},"custom":{},"state":"live","channelId":"444e7089-7570-407f-b17e-cca0fa1b3b0e","updatedAt":"2018-06-25T12:56:49.641Z","userCount":2,"description":"Test Phenix","id":"1bd940d9-6d2b-4fd2-b104-bfbabc9cbac4","title":"Test Phenix"}]
```



Status: Get Channel Streams | Code: 200



```js
[
    {
        "preview": {
            "type": "image",
            "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"
        },
        "createdAt": "2017-11-28T13:55:31.569Z",
        "airdate": "2017-11-27T10:30:00.000Z",
        "custom": {
            "splash_enabled": true,
            "splash_url": "http://zender.tv",
            "splash_loginrequired": false
        },
        "description": "Zender API Stream",
        "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
        "published": true,
        "userCount": 3,
        "state": "live",
        "title": "Zender API Stream",
        "channelId": "67b5528a-baf4-41bc-b558-b36613ee14a4",
        "updatedAt": "2017-11-28T13:55:43.800Z"
    }
]
```



### 7. Get Stream


Retrieves a stream by id.

A stream contains the interaction endpoints for fetching further interaction data together with the [pusher](https://pusher.com) channels to subscribe to.

See the different interaction get config endpoints calls:

[Get Emojis Config](#bfa45fa0-263f-00e6-fd6a-b7798e323eda)

[Get Media Config](#8cb5cb06-faed-8d36-24d9-1dd78b0607c9)

[Get Shoutbox Config](#9e6b94f6-dea4-97e5-4533-940c22f27bcb)

[Get Polls Config](#bc0abbc2-1fe2-3dd6-3586-efea39c53727)

[Get Quiz Config](#a72e8fb6-0e60-384f-8dd9-031c2a977c65)

The state of a stream can be 'before', 'live' or 'after'.

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Get Stream  | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Stream | Code: 200



```js
{
    "s3CdnImageRegExp": "https://s3-eu-west-1.amazonaws.com/(.*)(.original[.|/])(.*)",
    "published": true,
    "interactions": {
        "media": {
            "pusher": {
                "channel": "stream-abe2c3fb-a60a-41ee-b6e3-a649755bdea2-media"
            },
            "endpoint": "{{mediaApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/media"
        },
        "shoutbox": {
            "pusher": {
                "channel": "stream-abe2c3fb-a60a-41ee-b6e3-a649755bdea2-shoutbox"
            },
            "endpoint": "{{shoutboxApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/shoutbox"
        },
        "emojis": {
            "pusher": {
                "channel": "stream-abe2c3fb-a60a-41ee-b6e3-a649755bdea2-emojis"
            },
            "endpoint": "{{emojisApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/emojis"
        },
        "polls": {
            "pusher": {
                "channel": "stream-abe2c3fb-a60a-41ee-b6e3-a649755bdea2-polls"
            },
            "endpoint": "{{pollsApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/polls"
        },
        "quiz": {
            "pusher": {
                "channel": "stream-abe2c3fb-a60a-41ee-b6e3-a649755bdea2-quiz"
            },
            "endpoint": "{{quizApiHost}}/v1/channels/3789b16d-8e9d-4071-9209-2dae67be3760/streams/abe2c3fb-a60a-41ee-b6e3-a649755bdea2/quiz"
        }
    },
    "channelId": "3789b16d-8e9d-4071-9209-2dae67be3760",
    "updatedAt": "2018-04-16T09:07:55.956Z",
    "airdate": "2018-03-05T13:18:00.000Z",
    "userCount": 23,
    "createdAt": "2018-03-05T13:18:57.622Z",
    "description": "Trivia stream",
    "id": "abe2c3fb-a60a-41ee-b6e3-a649755bdea2",
    "preview": {
        "type": "image",
        "url": "https://cdn.zender.tv/live/uploads/2808b5c6-76a1-4d18-93f5-23ea9f6246da/2018-04-03/b7afb9c2-943a-471a-a8f2-af2853be7dbe.original.png"
    },
    "custom": {},
    "state": "live",
    "title": "Zender API stream"
}
```



### 8. Get Registered Devices


Retrieves all the registered devices of a user logged in with a provider.

| Permissions             | no token | anonymous token | provider token | admin token |
| ----------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Registered Devices  | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/users/devices
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Registered Devices | Code: 200



```js
[{"type":"android","token":"fake-device-token"}]
```



### 9. Register Device


The register device endpoint is used for registering a device in order to receive native push notifications.

This call is only relevant for native implementations (iOS/Android).

You can only register a device with a provider bearer token.

| Permissions     | no token | anonymous token | provider token | admin token |
| --------------- | :------: | :-------------: | :------------: | :---------: |
| Register Device | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/users/devices/register
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"deviceToken": "deviceToken",
	"deviceType": "android"
}
```



***Responses:***


Status: Register Device | Code: 200



```js
{
    "targetId": "6702e9ea-2b46-4487-8830-d713b32c7c5e",
    "authenticated": true,
    "avatar": "https://graph.facebook.com/undefined/picture?width=250&type=square",
    "externalId": "6702e9ea-2b46-4487-8830-d713b32c7c5e_undefined",
    "role": "user",
    "devices": [
        {
            "type": "android",
            "endpoint": "<arn-endpoint>",
            "token": "deviceToken"
        }
    ],
    "updatedAt": "2018-01-09T09:20:22.654Z",
    "createdAt": "2018-01-09T09:19:30.719Z",
    "provider": {
        "name": "facebook"
    },
    "id": "904cae9c-e1e8-4c35-8791-a22845f9a0d2"
}
```



### 10. Unregister Device


The unregister device endpoint is used for unregistering a device in order to stop receiving native push notifications.

This call is only relevant for native implementations (iOS/Android).

You can only register a device with a provider bearer token.

| Permissions       | no token | anonymous token | provider token | admin token |
| ----------------- | :------: | :-------------: | :------------: | :---------: |
| Unregister Device | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/users/devices/unregister
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"deviceToken": "deviceToken",
	"deviceType": "android"
}
```



***Responses:***


Status: Unregister Device (validation error) | Code: 400



```js
{"code":"BAD_REQUEST","message":"Please provide 'deviceType' and 'deviceToken' params in request body!"}
```



Status: Unregister Device (success) | Code: 200



```js
{"targetId":"6702e9ea-2b46-4487-8830-d713b32c7c5e","authenticated":true,"avatar":"https://graph.facebook.com/undefined/picture?width=250&type=square","externalId":"6702e9ea-2b46-4487-8830-d713b32c7c5e_undefined","role":"user","devices":[],"updatedAt":"2018-01-09T09:23:49.486Z","createdAt":"2018-01-09T09:19:30.719Z","provider":{"name":"facebook"},"id":"904cae9c-e1e8-4c35-8791-a22845f9a0d2"}
```



### 11. Subscribe to Topic


Subscribe to a push notifications topic.

The possible topicIds that can be provided in the request body can be found in the "config" attribute of the [Get Target](#5810f0fe-7be7-6839-c4a7-307b2527777e) response.

| Permissions        | no token | anonymous token | provider token | admin token |
| ------------------ | :------: | :-------------: | :------------: | :---------: |
| Subscribe to Topic | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/users/devices/subscribe
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"deviceToken": "deviceToken",
	"topicId": "be88e951-bbaf-4c16-a96a-f26da2eba763"
}
```



***Responses:***


Status: Subscribe to Topic (success) | Code: 200



```js
{"topicId":"be88e951-bbaf-4c16-a96a-f26da2eba763","token":"deviceToken","status":"subscribed"}
```



Status: Subscribe to Topic (validation error) | Code: 400



```js
{"code":"BAD_REQUEST","message":"Please provide 'deviceToken' and 'topicId' params in request body!"}
```



### 12. Unsubscribe from Topic


Unsubcribe from a push notifications topic.

The possible topicIds that can be provided in the request body can be found in the "config" attribute of the [Get Target](#5810f0fe-7be7-6839-c4a7-307b2527777e) response.

| Permissions            | no token | anonymous token | provider token | admin token |
| ---------------------- | :------: | :-------------: | :------------: | :---------: |
| Unsubscribe from Topic | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/users/devices/unsubscribe
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"deviceToken": "deviceToken",
	"topicId": "be88e951-bbaf-4c16-a96a-f26da2eba763"
}
```



***Responses:***


Status: Unsubscribe from Topic (validation error) | Code: 400



```js
{"code":"BAD_REQUEST","message":"Please provide 'deviceToken' and 'topicId' params in request body!"}
```



Status: Unsubscribe from Topic (success) | Code: 200



```js
{"topicId":"be88e951-bbaf-4c16-a96a-f26da2eba763","token":"deviceToken","status":"unsubscribed"}
```



### 13. Geo Check


Get the geo location of an ip address.

| Permissions | no token | anonymous token | device token | admin token |
| ----------- | :------: | :-------------: | :----------: | :---------: |
| Geo Check   | x        | x               | x            | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{coreApiHost}}/v1/geo/8.8.8.8
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Geo Check | Code: 200



```js
{"ip":"8.8.8.8","country_code":"US","country_name":"United States","region_code":"","region_name":"","city":"","zip_code":"","time_zone":"","latitude":37.751,"longitude":-97.822,"metro_code":0}

```



### 14. Get Signed Upload Url


This endpoint returns a url (uploadUrl) where you can upload content (images, video) to.

If the resource to upload is an image, different resized variants urls can be returned.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Signed Upload Url | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{coreApiHost}}/v1/upload
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"filename": "test-file.png"
}
```



***Responses:***


Status: Get Signed Upload Url | Code: 200



```js
{
    "uploadId": "e5855fe4-f371-49aa-9803-be69be580e1b",
    "uploadUrl": "https://s3-eu-west-1.amazonaws.com/cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/user/2018-03-14/e5855fe4-f371-49aa-9803-be69be580e1b.original.png?AWSAccessKeyId=ASIAI4MYZEZT3GXDJGQQ&Content-Type=image%2Fpng&Expires=1521020020&Signature=%2BlusmzZ1GiI3n0jJPgKOnGPUFf4%3D&x-amz-acl=public-read&x-amz-meta-filename=test-file.png&x-amz-meta-id=e5855fe4-f371-49aa-9803-be69be580e1b&x-amz-meta-targetid=6702e9ea-2b46-4487-8830-d713b32c7c5e&x-amz-meta-userid=904cae9c-e1e8-4c35-8791-a22845f9a0d2&x-amz-meta-userrole=user&x-amz-security-token=FQoDYXdzEEIaDP1OrJUcxN4dkPcjZCLAAw0OdxgDaHb5I%2BzpLqyJZ1LH3M9yO1HBh%2BcF%2FDib9HzPGp281XQGQ0M5gS7xOUfPEFXKSMHwyHgF2hSW2i2G5RUkKPrBn6WuagkJOejtxR%2FqHzlLJyVtz9W1dN68bPLAoCiVzxOZcM2l7JytXZUORFHM7FLB0jLcS1PoW2CI%2FsEVEnCbCWT%2F5r7JppbwEIYoz4TU3tgPe9lw5KoW42SV%2BxiP5xUfSScHdhvjv0K8%2B91yV0LPaRpSWbiF3L%2FrfxGZYZXIA5Fxg1joJcuA4Kk5FhXcM5gaU0FlDLvryhZy%2BGg6JiB3TzPKhYCgL4XXTCpOpI4lf99UAzGOXHn6Twd4H7Goq5awSl%2BpSbYmJpTd60WRndbas1xoxqkEVBEUE5d41kvtDNmaz5nLaPj6wVYndBB7pWcoxmIBTm3IlU%2FvW6%2Fpzv764tESHLcu32qgQKffsHX0jBEWSYBt54FFeyigflDZVxVl6dyiIDFCy8%2FxYDkWqSJvN3nQz3HgUjb89b%2B7HkcpstzQ37vwqJsFPdG%2FQlrS8G4Er9ERIJ%2FkrewIeQfYPmkGikia99%2B0Dm34uk9QxtNsGOVYdzywIAGn5TuH5QQoycuj1QU%3D&x-amz-tagging=targetId%3D6702e9ea-2b46-4487-8830-d713b32c7c5e%26targetName%3Dkarrewiet",
    "resizedUrls": {
        "large": "https://s3-eu-west-1.amazonaws.com/cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/user/2018-03-14/e5855fe4-f371-49aa-9803-be69be580e1b.large.png",
        "medium": "https://s3-eu-west-1.amazonaws.com/cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/user/2018-03-14/e5855fe4-f371-49aa-9803-be69be580e1b.medium.png",
        "small": "https://s3-eu-west-1.amazonaws.com/cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/user/2018-03-14/e5855fe4-f371-49aa-9803-be69be580e1b.small.png"
    },
    "contentType": "image/png",
    "getUrl": "https://s3-eu-west-1.amazonaws.com/cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/user/2018-03-14/e5855fe4-f371-49aa-9803-be69be580e1b.original.png"
}
```



### 15. Remove user data


Removes user authentication data.
External id is kept, so that account reactivation is still possible.

Make sure to remove other data (like shouts) first.


***Endpoint:***

```bash
Method: DELETE
Type: FORMDATA
URL: {{authApiHost}}/v1/auth/users
```



***Responses:***


Status: Remove user data, success | Code: 200



```js
{}
```



Status: Remove user data, unauthorized | Code: 401



```js
{"code":"UNAUTHORIZED","message":"This request is not authorized."}
```



## Player/Emojis



### 1. Get Emojis Config


Get emojis config of a particular stream.

| Permissions       | no token | anonymous token | provider token | admin token |
| ----------------- | :------: | :-------------: | :------------: | :---------: |
| Get Emojis Config | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Emojis Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.724Z",
    "sortedSets": [
        {
            "emojis": [
                {
                    "title": "73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
                },
                {
                    "title": "560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/560527f8-4319-4021-a522-9b4ad0aecad5.original.png"
                },
                {
                    "title": "26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
            },
            "id": "7e85a00c-5d94-444c-93a2-b93764d50ca2",
            "title": "Zender API Emoji Set",
            "type": "custom",
            "enabled": true
        },
        {
            "emojis": [
                {
                    "title": "000-gezichten__smile01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png"
                },
                {
                    "title": "000-gezichten__smile02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/b1554f8c-a099-4146-bb72-74e65524ac71.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/b1554f8c-a099-4146-bb72-74e65524ac71.original.png"
                },
                {
                    "title": "000-gezichten__smile03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a3920971-0169-41d8-b5c7-b1a5e4ebd853.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a3920971-0169-41d8-b5c7-b1a5e4ebd853.original.png"
                },
                {
                    "title": "000-gezichten__smile04",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5734048c-d83b-4941-8bd6-797658274424.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5734048c-d83b-4941-8bd6-797658274424.original.png"
                },
                {
                    "title": "000-gezichten__smile05",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5badba92-e650-4223-ba18-87585e1e07a6.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/5badba92-e650-4223-ba18-87585e1e07a6.original.png"
                },
                {
                    "title": "000-gezichten__smile06",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/3e93bc03-5c51-452a-a4ca-bd6e2121bcce.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/3e93bc03-5c51-452a-a4ca-bd6e2121bcce.original.png"
                },
                {
                    "title": "000-gezichten__smile07",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73eb9ba8-a9f2-465d-882d-cf29d6349029.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73eb9ba8-a9f2-465d-882d-cf29d6349029.original.png"
                },
                {
                    "title": "000-gezichten__smile08",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/cab89d89-67a6-4ec8-ab06-3fecee8c9d8d.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/cab89d89-67a6-4ec8-ab06-3fecee8c9d8d.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/fbc5dabe-8fb7-4c1c-8dd0-d70d37ce4559.original.png"
            },
            "id": "7b3f2436-dae0-45cf-aad2-4320cd342640",
            "title": "000-faces"
        },
        {
            "emojis": [
                {
                    "title": "001-handen__hand01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png"
                },
                {
                    "title": "001-handen__hand02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/655e92a4-5d18-47ab-9cf6-e39c2cb4babf.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/655e92a4-5d18-47ab-9cf6-e39c2cb4babf.original.png"
                },
                {
                    "title": "001-handen__hand03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/1b7fe938-d774-474c-a194-d3dd1fb865a8.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/1b7fe938-d774-474c-a194-d3dd1fb865a8.original.png"
                },
                {
                    "title": "001-handen__hand04",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/e31906f3-e6be-4fb8-a902-5c07de7707bf.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/e31906f3-e6be-4fb8-a902-5c07de7707bf.original.png"
                },
                {
                    "title": "001-handen__hand05",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9308dd80-b525-4313-9bff-7f602fbb9435.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9308dd80-b525-4313-9bff-7f602fbb9435.original.png"
                },
                {
                    "title": "001-handen__hand06",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/957a5877-94a9-45c5-94b4-26c6e71c7b5d.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/957a5877-94a9-45c5-94b4-26c6e71c7b5d.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/16d20a2e-47ee-4315-b673-7b91e5230763.original.png"
            },
            "id": "4775a542-bc43-4ce6-bf43-27a0fa7acc78",
            "title": "001-hands"
        },
        {
            "emojis": [
                {
                    "title": "002-liefde__love01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png"
                },
                {
                    "title": "002-liefde__love02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f2730bd7-aa84-4027-baae-0bfbc5a2e065.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f2730bd7-aa84-4027-baae-0bfbc5a2e065.original.png"
                },
                {
                    "title": "002-liefde__love03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/18801fe1-bc93-4673-ac7a-e5de23677fd8.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/18801fe1-bc93-4673-ac7a-e5de23677fd8.original.png"
                },
                {
                    "title": "002-liefde__love04",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f1ad0ac7-6e89-47cd-8af4-880dbf344dd5.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f1ad0ac7-6e89-47cd-8af4-880dbf344dd5.original.png"
                },
                {
                    "title": "002-liefde__love05",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/4bcf20b5-237c-48e1-864c-acd5e0a736fe.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/4bcf20b5-237c-48e1-864c-acd5e0a736fe.original.png"
                },
                {
                    "title": "002-liefde__love06",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/bc9b218a-2170-4aba-aeea-efb777ff15d3.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/bc9b218a-2170-4aba-aeea-efb777ff15d3.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9523c952-2e23-4c3a-bf83-61c9a17a4168.original.png"
            },
            "id": "5b9dab91-f96d-4b60-a612-39a2ef567077",
            "title": "002-love"
        },
        {
            "emojis": [
                {
                    "title": "003-dieren__a-bunny",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png"
                },
                {
                    "title": "003-dieren__a-cat01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2cd7d92f-ebff-4bb3-b4cd-eca611443244.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2cd7d92f-ebff-4bb3-b4cd-eca611443244.original.png"
                },
                {
                    "title": "003-dieren__a-cat02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/c6e365e5-5cde-410f-b036-9a5970ec3aa6.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/c6e365e5-5cde-410f-b036-9a5970ec3aa6.original.png"
                },
                {
                    "title": "003-dieren__a-cat03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/97d6ef27-1be6-4071-9f19-b613b24d553e.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/97d6ef27-1be6-4071-9f19-b613b24d553e.original.png"
                },
                {
                    "title": "003-dieren__a-cat04",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f64293a2-a7c1-42d8-a62c-5b303617b2df.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f64293a2-a7c1-42d8-a62c-5b303617b2df.original.png"
                },
                {
                    "title": "003-dieren__a-chicken",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/caf5e45c-fe08-4740-b5ff-7e160d88cc4e.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/caf5e45c-fe08-4740-b5ff-7e160d88cc4e.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/d0e333f7-1905-4acb-9e63-4102c11e9db5.original.png"
            },
            "id": "ed93d548-63a7-4729-bec8-8fe9cbda2dd5",
            "title": "003-animals"
        },
        {
            "emojis": [
                {
                    "title": "004-sport__s-ball",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png"
                },
                {
                    "title": "004-sport__s-bike",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/0a13262d-501f-42d8-82d5-5e9026d32998.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/0a13262d-501f-42d8-82d5-5e9026d32998.original.png"
                },
                {
                    "title": "004-sport__basebal",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9350eeba-6228-44ea-ae85-ac13e261e6b3.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9350eeba-6228-44ea-ae85-ac13e261e6b3.original.png"
                },
                {
                    "title": "004-sport__basketbal",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f5b3882c-af2d-4b3c-a4fe-b2cdae5f6d86.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/f5b3882c-af2d-4b3c-a4fe-b2cdae5f6d86.original.png"
                },
                {
                    "title": "004-sport__fiets",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/882e4699-f171-4b1b-aaad-c410d210d6a3.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/882e4699-f171-4b1b-aaad-c410d210d6a3.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/9f088285-b8af-49b5-bb18-f8c3ea950d64.original.png"
            },
            "id": "30ae1d2f-dbec-4069-93cc-0bc4352d25eb",
            "title": "004-sport"
        },
        {
            "emojis": [
                {
                    "title": "005-objecten__a-food01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png"
                },
                {
                    "title": "005-objecten__a-food02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7452ce3e-0112-4f85-b2e2-f17de5d52190.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7452ce3e-0112-4f85-b2e2-f17de5d52190.original.png"
                },
                {
                    "title": "005-objecten__a-food03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2994ab4a-f49e-4e03-9c23-64067e629e51.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/2994ab4a-f49e-4e03-9c23-64067e629e51.original.png"
                },
                {
                    "title": "005-objecten__a-food04",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/43d445f0-02b1-4cde-9eb6-91b1d2267711.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/43d445f0-02b1-4cde-9eb6-91b1d2267711.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/8ed6b445-a414-48b3-9a0a-5a8b037b9f47.original.png"
            },
            "id": "800e75aa-16e3-4d32-aaa8-b20bc9682c98",
            "title": "005-objects"
        },
        {
            "emojis": [
                {
                    "title": "005-weer__a-weer01",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png"
                },
                {
                    "title": "005-weer__a-weer02",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a47dbf95-6268-4a19-ad47-2e0f86229f32.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/a47dbf95-6268-4a19-ad47-2e0f86229f32.original.png"
                },
                {
                    "title": "005-weer__a-weer03",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/61689c10-f4be-4a14-a1cb-b9c2f041ee1a.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/61689c10-f4be-4a14-a1cb-b9c2f041ee1a.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/7d645b32-1e43-4a32-93a5-6a48d8df842f.original.png"
            },
            "id": "737178d3-a13b-4b44-af2c-04f9a4b69475",
            "title": "005-weather"
        }
    ],
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "enabled": true,
    "updatedAt": "2017-11-28T13:56:54.728Z",
    "cdnHost": "https://cdn.zender.tv",
    "defaultEmoji": {
        "title": "73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
        "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
        "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
    },
    "sets": [
        {
            "emojis": [
                {
                    "title": "73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
                },
                {
                    "title": "560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/560527f8-4319-4021-a522-9b4ad0aecad5.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/560527f8-4319-4021-a522-9b4ad0aecad5.original.png"
                },
                {
                    "title": "26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
                    "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png",
                    "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/26b9db64-ec8d-47fe-92c9-d4e104213ab9.original.png"
                }
            ],
            "icon": {
                "url": "https://cdn.zender.tv/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png",
                "id": "/live/uploads/e1cc9d4b-2969-4d50-a74f-cb39ac5f5f68/2017-11-28/73ebf11e-ad24-4dcb-878f-3e9b06db280e.original.png"
            },
            "id": "7e85a00c-5d94-444c-93a2-b93764d50ca2",
            "title": "Zender API Emoji Set",
            "type": "custom",
            "enabled": true
        }
    ],
    "postEmojis": "{{emojisApiHost}}/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/emojis/reactions",
    "postAvatars": "{{emojisApiHost}}/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/emojis/avatars",
    "emojis": {
        "total": 0,
        "counters": {}
    },
    "avatars": {
        "total": 0
    }
}
```



### 2. Post Emojis


Send a single or multiple emojis.

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Post Emojis | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/reactions
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "emojis": [
    { "id": "{{defaultEmoji}}" }
  ]
}
```



***Responses:***


Status: Post Emojis (validation error) | Code: 400



```js
{"message":[{"selector":"emojis","tip":"emojis is mandatory."},{"selector":"emojis.*.id","tip":"emojis.*.id is mandatory."}]}
```



Status: Post Single Emoji (success) | Code: 200



```js
{}
```



Status: Post Multiple Emojis (success) | Code: 200



```js
{}
```



### 3. Post Avatars


Posting an avatar is only possible if the Bearer token in the authorization header belongs to a non-anonymous user. To login as a authenticated user see: "Provider Token Login".

| Permissions  | no token | anonymous token | provider token | admin token |
| ------------ | :------: | :-------------: | :------------: | :---------: |
| Post Avatars | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{emojisApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/emojis/avatars
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "count": 10
}
```



***Responses:***


Status: Post Avatars (validation error) | Code: 400



```js
{"message":[{"selector":"count","tip":"count is mandatory."}]}
```



Status: Post Multiple Emojis (success) | Code: 200



```js
{}
```



Status: Post Single Emoji (success) | Code: 200



```js
{}
```



## Player/Media



### 1. Get Media Config


Get the media config of a particular stream.

The response of can contain triggered content items that contain an image and/or video. The media content items will always have a "routing" attribute that can be either 'studio' (studio visualisation) or 'player' (the zender player).

When a different url is needed for native video versus web, the url will be separated by '|native:', so in effect: 'https://some.video/stream|native:rtsp://some.other/url' should be split up in those two parts.

| Permissions      | no token | anonymous token | provider token | admin token |
| ---------------- | :------: | :-------------: | :------------: | :---------: |
| Get Media Config | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{mediaApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/media/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
| Authorization | Bearer {{adminToken}} |  |



***Responses:***


Status: Get Media Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.739Z",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "enabled": true,
    "updatedAt": "2017-11-28T13:57:21.427Z",
    "content": [
        {
            "routing": "studio",
            "createdAt": "2017-11-28T13:58:08.400Z",
            "view": {
                "image": {
                    "url": "https://cdn.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
                }
            },
            "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "description": "Zender API Media Pancarte",
            "id": "80f0fe65-ae45-43d9-a1f5-5ad7fbd7fbf7",
            "title": "Zender API Media Pancarte"
        },
        {
            "routing": "player",
            "createdAt": "2017-11-28T13:57:42.399Z",
            "view": {
                "image": {
                    "url": "https://cdn..zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
                },
                "video": {
                    "autoplay": true,
                    "aspectRatio": "16:9",
                    "loop": true,
                    "url": "https://cdn.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.original.mp4",
                    "alternativeUrls": [
                    	"https://cdn.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/567153ca-482c-476f-a289-6317b9360574.alternative.mp4"	
                    ],
                    "allowedRegions": "BE"
                }
            },
            "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "description": "Zender API Media Pancarte",
            "id": "49a2328f-3759-44bf-8499-f0e2601efee7",
            "title": "Zender API Media Pancarte"
        }
    ]
}
```



## Player/Polls



### 1. Get Polls Config


Get polls config. This endpoint will also return the started (public) polls and their results (if results are configured for that poll).

| Permissions      | no token | anonymous token | provider token | admin token |
| ---------------- | :------: | :-------------: | :------------: | :---------: |
| Get Polls Config | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Polls Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.723Z",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "enabled": true,
    "updatedAt": "2017-11-29T09:17:24.489Z",
    "cdnHost": "https://cdn.zender.tv",
    "polls": [
        {
            "realtimeResults": true,
            "studio": {
                "backgroundVideo": {
                    "aspectRatio": "16:9",
                    "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
                    "loop": true,
                    "autoplay": true
                },
                "backgroundImage": {
                    "width": 579,
                    "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
                    "height": 580
                }
            },
            "fountain": true,
            "voteRoles": [
                "authenticated"
            ],
            "question": {
                "text": "Who will win the elections?"
            },
            "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "facebook": {
                "postId": "10151400246079999",
                "integrationType": "text",
                "enabled": true,
                "linkedChoices": [
                    "Bernie",
                    "Trump"
                ]
            },
            "priority": 1,
            "openedAt": "2017-11-29T09:27:45.942Z",
            "createdAt": "2017-11-29T09:23:41.146Z",
            "status": "open",
            "multiChoice": true,
            "multiVote": true,
            "answer": {
                "choices": [
                    {
                        "title": "Bernie Sanders",
                        "image": {
                            "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
                            "id": "/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"
                        },
                        "id": "084bacc5-b8ce-4096-bdc5-1b1e00570206"
                    },
                    {
                        "title": "Donald Trump",
                        "image": {
                            "url": "https://cdn.zender.tv/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png",
                            "id": "/live/uploads/b8f99a0c-1383-4891-af7a-563b5903d390/2017-11-28/aa807b08-311a-45a1-9a43-fd8ac9a19616.original.png"
                        },
                        "id": "85a0a3e1-a705-4844-8466-ea0e07ce9727"
                    }
                ]
            },
            "showResults": true,
            "id": "d97a4943-9373-421a-ae6a-8d4a2908e50a",
            "closedAt": "2017-11-29T09:27:19.894Z",
            "closingOffset": 5000,
            "updatedAt": "2017-11-29T09:27:45.942Z",
            "postVotes": "{{pollsApiHost}}/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/polls/d97a4943-9373-421a-ae6a-8d4a2908e50a/vote"
        }
    ],
    "results": {
        "d97a4943-9373-421a-ae6a-8d4a2908e50a": {
            "total": 1,
            "counters": {
                "85a0a3e1-a705-4844-8466-ea0e07ce9727": 1
            }
        }
    }
}
```



### 2. Poll Vote


Vote for a choice of a poll.

These are the different responses that the endpoint can produce:

**200 OK**: If the cast of the vote was successful. See the "Poll vote (success)" example.

**410 GONE**: If you try to cast a vote for a poll that was stopped (i.e. its status is closed). See the "Poll vote (closed poll)" example.

**403 FORBIDDEN**: If you try to cast a vote for a poll that has the "multiVote" attribute set to false. See the "Poll vote (vote already cast)" example.

**400 BAD REQUEST**: If you try to cast more than one vote for a poll that has the "multiChoice" attribute set to false. See the "Poll vote (no multiple choice)" example.

**403 FORBIDDEN**: If you try to cast a vote for a poll with a token of a user with a role that does not match one of the roles defined in the "voteRoles" array of the poll. See the "Poll vote (auth role mismatch)" example.

**400 BAD REQUEST**: If you provide a request body where the "votes" attribute is not an array of objects with an "id" and positive "count" attributes. See the "Poll vote (role mismatch)" example.

**404 NOT FOUND**: If the poll does not exist. See the "Poll vote (poll not found)" example.

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Poll Vote   | -        | configurable    | configurable   | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{pollsApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/polls/{{pollId}}/vote
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "votes": [
    {
      "count": 1,
      "id": "{{choiceId}}"
    }
  ]
}
```



***Responses:***


Status: Poll Vote (success) | Code: 200



```js
{"votes":[{"count":1,"id":"084bacc5-b8ce-4096-bdc5-1b1e00570206"}]}
```



Status: Poll Vote (validation error) | Code: 400



```js
{"message":[{"path":["votes"],"tip":"Votes must be an array of objects with an id and positive count"}]}
```



Status: Poll Vote (auth role mismatch) | Code: 403



```js
{"code":"FORBIDDEN","message":"You are not allowed to vote for this poll."}
```



## Player/Quiz



### 1. Get Quiz Config


Get polls config. This endpoint will also return the started quizzes.

| Permissions     | no token | anonymous token | provider token | admin token |
| --------------- | :------: | :-------------: | :------------: | :---------: |
| Get Quiz Config | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Quiz Config (no quizzes active) | Code: 200



```js
{"enabled":true,"createdAt":"2018-03-05T14:33:42.658Z","id":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","quizzes":[]}
```



Status: Get Quiz Config (quiz active) | Code: 200



```js
{"streamId":"0f7b9760-38c9-11e8-8624-fd8ce62b547c","createdAt":"2018-04-16T12:49:06.159Z","enabled":true,"quizzes":[{"createdAt":"2018-04-16T12:49:08.189Z","answerTime":10000,"streamId":"0f7b9760-38c9-11e8-8624-fd8ce62b547c","description":"Trivia about Sports","startedAt":"2018-04-16T12:51:04.783Z","id":"0e9da1fd-322e-48bf-aedc-a0adb00b4b3f","title":"Sports Quiz","status":"started","updatedAt":"2018-04-16T12:51:04.783Z"}]}
```



Status: Get Quiz Config | Code: 200



```js
{"enabled":true,"createdAt":"2018-03-05T14:33:42.658Z","id":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","streamId":"abe2c3fb-a60a-41ee-b6e3-a649755bdea2","quizzes":[]}
```



### 2. Answer Question


Send the answer to a quiz question.

These are the different responses that the endpoint can produce:

**410 GONE**: The answer was to early or did not arrive within the configured quiz "answerTime". See the "Answer Question (answerTime expired)" example.

**410 GONE**: If the user answered a previous question wrong or not at all. In other words: the user is terminated from the quiz. See the "Answer Question (previous question not answered or answered incorrect)" example.

**409 CONFLICT**: If you try to answer twice or more. See the "Answer Question (already answered)" example.

**404 NOT FOUND**: If the question does not exist. See the "Answer Question (question not found)" example.

| Permissions     | no token | anonymous token | provider token | admin token |
| --------------- | :------: | :-------------: | :------------: | :---------: |
| Answer Question | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question/{{questionId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "answer": 1
}
```



***Responses:***


Status: Answer Question (already answered) | Code: 409



```js
{"code":"CONFLICT","message":"You can only answer a question once."}
```



Status: Answer Question (question not found) | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "No question found with id: 9c2bf863-a210-41c8-a6bf-08d01a19593 for quiz: 0e9da1fd-322e-48bf-aedc-a0adb00b4b3fd"
}
```



Status: Answer Question (answerTime expired) | Code: 410



```js
{"code":"GONE","message":"You can not answer the question for this quiz at this time."}
```



Status: Answer Question (previous question not answered or answered incorrect) | Code: 410



```js
{"code":"GONE","message":"You can no longer answer questions for this quiz."}
```



Status: Answer Question | Code: 200



```js
{}
```



### 3. Get Quiz Leaderboard Win


Retrieves the top n users by descending quiz wins for a given target (i.e. the target of the bearer token).

| Permissions              | no token | anonymous token | provider token | admin token |
| ------------------------ | :------: | :-------------: | :------------: | :---------: |
| Get Quiz Leaderboard Win | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/leaderboard
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| type | win |  |
| limit | 10 |  |



***Responses:***


Status: Get Quiz Leaderboard Win | Code: 200



```js
[{"user":{"id":"f132c34a-ec33-4779-a837-e27c3e868753","name":"Anonymous","avatar":"https://cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/2017-11-09/eb37b0a3-d660-40cd-a1eb-7fe98cfdb3df.original.jpeg","externalId":"e878ecf0-31b9-11e8-883b-150a4ff79cb7_fbed2d37-02bd-4e0e-8ee7-c1205fa75df0"},"scores":{"wins":1,"answers":1}}]
```



### 4. Get Quiz Leaderboard Answer


Retrieves the top n users by descending correct answers for a given target (i.e. the target of the bearer token).

| Permissions                 | no token | anonymous token | provider token | admin token |
| --------------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Quiz Leaderboard Answer | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/leaderboard
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| type | answer |  |
| limit | 10 |  |



***Responses:***


Status: Get Quiz Leaderboard Answer (no bearer token provided) | Code: 401



```js
{"code":"UNAUTHORIZED","message":"You are not allowed to retrieve this leaderboard."}
```



Status: Get Quiz Leaderboard Answer (success) | Code: 200



```js
[{"user":{"id":"f132c34a-ec33-4779-a837-e27c3e868753","name":"Anonymous","avatar":"https://cdn.zender.tv/live/uploads/6702e9ea-2b46-4487-8830-d713b32c7c5e/2017-11-09/eb37b0a3-d660-40cd-a1eb-7fe98cfdb3df.original.jpeg","externalId":"e878ecf0-31b9-11e8-883b-150a4ff79cb7_fbed2d37-02bd-4e0e-8ee7-c1205fa75df0"},"scores":{"wins":1,"answers":1}}]
```



### 5. Get Quiz Leaderboard User


Retrieves current user's quiz scores for a given target (i.e. the target of the bearer token).

| Permissions               | no token | anonymous token | provider token | admin token |
| ------------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Quiz Leaderboard User | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/leaderboard
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| type | user |  |



***Responses:***


Status: Get Quiz Leaderboard User (no bearer token provided) | Code: 401



```js
{"code":"UNAUTHORIZED","message":"You are not allowed to retrieve this leaderboard."}
```



### 6. Set Quiz Referrer code


Sets current user's referrer code for a given target (i.e. the target of the bearer token).

| Permissions  | no token | anonymous token | provider token | admin token |
| ------------ | :------: | :-------------: | :------------: | :---------: |
| Set referrer | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/referrer
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
  "shareCode": "2808b5c6-76a1-4d18-93f5-23ea9f6246da_10212482779324747"
}
```



***Responses:***


Status: Set Quiz Referrer code | Code: 200



```js
{"status":"ok"}
```



Status: Set own quiz referrer code | Code: 403



```js
{"code":"FORBIDDEN","message":"Cannot set own referrer code."}
```



Status: Share code doesn't exist | Code: 404



```js
{"code":"NOT_FOUND","message":"Share code does not exist."}
```



### 7. Get Quiz Referrer code


Gets current user's referrer code for a given target (i.e. the target of the bearer token).

| Permissions  | no token | anonymous token | provider token | admin token |
| ------------ | :------: | :-------------: | :------------: | :---------: |
| Get referrer | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/referrer
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Responses:***


Status: Get Quiz Referrer code | Code: 200



```js
{"code":"2808b5c6-76a1-4d18-93f5-23ea9f6246da_10212482779324747"}
```



Status: Not found | Code: 404



```js
{"code":"NOT_FOUND","message":"No referrer code set."}
```



### 8. Redeem extra life on last question


Redeem an extra life on the specified question. This is to be used when the user gives a bad answer or no answer to a question, and they want to stay in the quiz.

| Permissions    | no token | anonymous token | provider token | admin token |
| -------------- | :------: | :-------------: | :------------: | :---------: |
| Use extra life | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/{{quizId}}/question/{{questionId}}/redeem
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Body:***

```js        
{
}
```



***Responses:***


Status: You cannot redeem when still in the running. | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "You cannot redeem when still in the running."
}
```



Status: Forbidden, no closed questions | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "No closed questions yet."
}
```



Status: Question is not closed. | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "Question not closed yet."
}
```



Status: Question is not redeemable. | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "You can not redeem an extra life for this question."
}
```



Status: No questions | Code: 403



```js
{"code":"FORBIDDEN","message":"No questions."}
```



Status: Only last question can be redeemed | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "Can only redeem last question."
}
```



Status: Ok | Code: 200



```js
{}
```



Status: You can redeem an extra life once per quiz. | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "You can redeem an extra life once per quiz."
}
```



Status: No extra lives | Code: 403



```js
{
    "code": "FORBIDDEN",
    "message": "No extra lives."
}
```



### 9. Get extra lives


Get number of extra lives.

| Permissions     | no token | anonymous token | provider token | admin token |
| --------------- | :------: | :-------------: | :------------: | :---------: |
| Get extra lives | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{quizApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/quiz/extraLives
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
|  |  |  |



***Responses:***


Status: Get extra lives | Code: 200



```js
{"extraLives":11}
```



## Player/Shoutbox



### 1. Get Shoutbox Config


Get the shoutbox configuration for a given stream.

| Permissions         | no token | anonymous token | provider token | admin token |
| ------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Shoutbox Config | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/config
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
| Authorization | Bearer {{providerToken}} |  |



***Responses:***


Status: Get Shoutbox Config | Code: 200



```js
{
    "createdAt": "2017-11-28T13:55:31.657Z",
    "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "topic": "Topic",
    "id": "a2993350-cb51-437d-bf39-41e110a71f5a",
    "placeholder": "Leave a message plz...",
    "welcome": "Welcome to the new live stream",
    "enabled": true,
    "updatedAt": "2017-11-28T14:43:43.326Z",
    "postShouts": "{{shoutboxApiHost}}/v1/channels/67b5528a-baf4-41bc-b558-b36613ee14a4/streams/a2993350-cb51-437d-bf39-41e110a71f5a/shoutbox/messages",
    "shouts": [
        {
            "createdAt": "2017-11-28T14:50:50.426Z",
            "clientId": "bdaac6e5-fb79-462c-b669-80641bfef413-1511880426214",
            "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "id": "92639bcc-05c8-4c8f-b7f3-4f01710264d8",
            "type": "user",
            "userId": "f468fca3-1287-4858-880f-7c099e0ba1d3",
            "content": {
                "text": "Something interesting."
            },
            "user": {
                "id": "f468fca3-1287-4858-880f-7c099e0ba1d3",
                "avatar": "https://graph.facebook.com/undefined/picture?width=250&type=square",
                "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_undefined"
            }
        },
        {
            "createdAt": "2017-11-28T14:50:17.999Z",
            "clientId": "bdaac6e5-fb79-462c-b669-80641bfef413-1511880426210",
            "streamId": "a2993350-cb51-437d-bf39-41e110a71f5a",
            "id": "58e51b0a-fc89-491d-980d-8b03877d8b49",
            "type": "user",
            "userId": "f468fca3-1287-4858-880f-7c099e0ba1d3",
            "content": {
                "text": "Something interesting."
            },
            "user": {
                "id": "f468fca3-1287-4858-880f-7c099e0ba1d3",
                "avatar": "https://graph.facebook.com/undefined/picture?width=250&type=square",
                "externalId": "b8f99a0c-1383-4891-af7a-563b5903d390_undefined"
            }
        }
    ]
}
```



### 2. Get Shoutbox Messages


Get all shoutbox messages.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Get Shoutbox Messages | x        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



### 3. Send Shoutbox Message


Send a shoutbox message.

**200 OK**: Message send successfully. See "Send Shoutbox Message (success)" example.

**403 FORBIDDEN**: If you try to send a message with a token of a user with role that does not match one of the roles defined in the "voteRoles" array of the poll. See "Send Shoutbox Message (auth role mismatch)" example.

| Permissions           | no token | anonymous token | provider token | admin token |
| --------------------- | :------: | :-------------: | :------------: | :---------: |
| Send Shoutbox Message | -        | configurable    | configurable   | -           |


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/{{channelId}}/streams/{{streamId}}/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "type": "user",
  "clientId": "bdaac6e5-fb79-462c-b669-80641bfef413-1511880426214",
  "content": {
    "text": "Something interesting.",
    "image": "https://cdn.zender.tv/live/uploads/03013c55-9996-4735-bbff-e1405601346e/2017-11-28/4fd6327e-6189-4c68-a5fc-dacca6013ab8.original.png"
  }
}
```



***Responses:***


Status: Send Shoutbox Message (auth role mismatch) | Code: 403



```js
{"code":"FORBIDDEN","message":"You are not allowed to shout."}
```



Status: Send Shoutbox Message (validation error) | Code: 400



```js
{
"message":[{"selector":"type","tip":"type is mandatory."},{"selector":"clientId","tip":"clientId is mandatory."},{"selector":"content.text","tip":"content.text is mandatory."}]}
```



Status: Send Shoutbox Message (success) | Code: 200



```js
{"type":"user","id":"d0d23aea-e9d3-4b2e-8cfd-99c10f31539f","clientId":"bdaac6e5-fb79-462c-b669-80641bfef413-1511880426210","streamId":"a2993350-cb51-437d-bf39-41e110a71f5a","content":{"text":"Something interesting."},"createdAt":"2017-11-28T14:48:46.427Z","user":{"authenticated":true,"createdAt":"2017-11-28T14:48:42.879Z","role":"user","targetId":"b8f99a0c-1383-4891-af7a-563b5903d390","provider":{"name":"facebook"},"externalId":"b8f99a0c-1383-4891-af7a-563b5903d390_undefined","avatar":"https://graph.facebook.com/undefined/picture?width=250&type=square","id":"f468fca3-1287-4858-880f-7c099e0ba1d3"}}
```



### 4. Delete Shoutbox Messages


Delete all shoutbox messages from current user.

| Permissions              | no token | anonymous token | provider token | admin token |
| ------------------------ | :------: | :-------------: | :------------: | :---------: |
| Delete Shoutbox Messages | -        | -               | x              | -           |


***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{shoutboxApiHost}}/v1/channels/all/streams/all/shoutbox/messages
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
  "enabled": "false"
}
```



***Responses:***


Status: Delete Shoutbox Messages, success | Code: 200



```js
{"count":0}
```



## Player/Teams



### 1. Create Team



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{teamsApiHost}}/v1/teams
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"name": "Small Town Heroes",
	"category": "Colleagues",
	"avatar": "https://static1.squarespace.com/static/5955fc221b631b7dd41ede60/t/59563d7b6b4998649f330b42/1559119093821"
}
```



***Responses:***


Status: Create Team Validation Errors | Code: 400



```js
{
    "code": "VALIDATION_ERROR",
    "message": "3 errors occurred",
    "name": "ValidationError",
    "errors": [
        "avatar must be a `string` type, but the final value was: `[]`.",
        "name must be a `string` type, but the final value was: `true`.",
        "category must be a `string` type, but the final value was: `6`."
    ]
}
```



Status: Create Team Success | Code: 200



```js
{
    "name": "Small Town Heroes",
    "category": "Colleagues",
    "avatar": "https://static1.squarespace.com/static/5955fc221b631b7dd41ede60/t/59563d7b6b4998649f330b42/1559119093821",
    "id": "712abb65-b6b2-4d01-b2fd-09ed44a15d3d",
    "admin": {
        "id": "e81356dd-1502-400f-b216-da9d09eacd7d",
        "username": "user-device2",
        "name": "user-device",
        "avatar": "https://cdn.zender.tv/assets/zender/default-avatar2.png"
    },
    "members": [
        {
            "id": "e81356dd-1502-400f-b216-da9d09eacd7d",
            "username": "user-device2",
            "name": "user-device",
            "avatar": "https://cdn.zender.tv/assets/zender/default-avatar2.png"
        }
    ],
    "teamCode": "37WGCG",
    "createdAt": "2019-06-06T15:00:11.546Z"
}

```



Status: Create Team Duplicate Team Name | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "Team name already in use.",
    "name": "DuplicateTeamNameError"
}
```



Status: Create Team No Multiple Teams | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "You can only be part of one team.",
    "name": "MultipleTeamsError"
}
```



### 2. Get Team


Get your team.

| Permissions | no token | anonymous token | provider token | admin token |
| ----------- | :------: | :-------------: | :------------: | :---------: |
| Get team    | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{teamsApiHost}}/v1/teams/{{teamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Get Team Success | Code: 200



```js
{
    "avatar": "https://static1.squarespace.com/static/5955fc221b631b7dd41ede60/t/59563d7b6b4998649f330b42/1559119093821",
    "admin": "d5f8ed38-56fc-45e0-a7ce-f6196430a35c",
    "members": [
        "d5f8ed38-56fc-45e0-a7ce-f6196430a35c"
    ],
    "category": "Colleagues",
    "createdAt": "2019-06-06T15:06:50.609Z",
    "id": "a53b13c5-e595-45ed-921a-92d9b9644ff1",
    "name": "Zender"
}
```



Status: Get Team Unauthorized | Code: 401



```js
{
    "code": "UNAUTHORIZED",
    "message": "This request is not authorized.",
    "name": "UnauthorizedError"
}
```



Status: Get Team Not Found Error | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "No team found for id 'unknown'",
    "name": "NotFoundError"
}
```



### 3. Update Team


Get emojis config of a particular stream.

| Permissions       | no token | anonymous token | provider token | admin token |
| ----------------- | :------: | :-------------: | :------------: | :---------: |
| Get Emojis Config | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{teamsApiHost}}/v1/teams/{{teamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"category": "Friends",
	"avatar": "https://m.media-amazon.com/images/M/MV5BNDVkYjU0MzctMWRmZi00NTkxLTgwZWEtOWVhYjZlYjllYmU4XkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_UY268_CR0,0,182,268_AL_.jpg"
}
```



***Responses:***


Status: Update Team Success | Code: 200



```js
{
    "avatar": "https://m.media-amazon.com/images/M/MV5BNDVkYjU0MzctMWRmZi00NTkxLTgwZWEtOWVhYjZlYjllYmU4XkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_UY268_CR0,0,182,268_AL_.jpg",
    "admin": "4d5e9a5f-de97-469d-bc09-0d2ad184e90a",
    "updatedAt": "2019-06-06T15:14:47.290Z",
    "members": [
        "4d5e9a5f-de97-469d-bc09-0d2ad184e90a"
    ],
    "category": "Friends",
    "createdAt": "2019-06-06T15:14:38.212Z",
    "id": "a939c8ef-5a3d-461e-9abb-3e39f861e305",
    "name": "Small Town Heroes"
}
```



Status: Update Team Only Admin Can Update Team | Code: 401



```js
{
    "code": "UNAUTHORIZED",
    "message": "Only the admin can update a team.",
    "name": "UnauthorizedError"
}
```



Status: Update Team Validation Error | Code: 400



```js
{
    "code": "VALIDATION_ERROR",
    "message": "2 errors occurred",
    "name": "ValidationError",
    "errors": [
        "avatar must be a `string` type, but the final value was: `2`.",
        "category must be a `string` type, but the final value was: `1`."
    ]
}
```



### 4. Delete Team


Get emojis config of a particular stream.

| Permissions       | no token | anonymous token | provider token | admin token |
| ----------------- | :------: | :-------------: | :------------: | :---------: |
| Get Emojis Config | -        | x               | x              | x           |


***Endpoint:***

```bash
Method: DELETE
Type: 
URL: {{teamsApiHost}}/v1/teams/{{teamId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Responses:***


Status: Delete Team Only Admin Can Delete Error | Code: 401



```js
{
    "code": "UNAUTHORIZED",
    "message": "Only the admin can delete a team.",
    "name": "UnauthorizedError"
}
```



Status: Delete Team Success | Code: 200



```js
{}
```



Status: Delete Team Not Found Error | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "No team found for id 'a853efc4-51f9-465b-b229-dd46d4ff1332'",
    "name": "NotFoundError"
}
```



### 5. Join Team



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{teamsApiHost}}/v1/teams/join
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"teamCode": "{{teamCode}}"
}
```



***Responses:***


Status: Join Team Maximum Capacity Error | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "You cannot join a team that is at maximum capacity (5).",
    "name": "MaximumCapacityError"
}
```



Status: Join Team Not Found | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "No team found with code 'unknow'",
    "name": "NotFoundError"
}
```



Status: Join Team Validation Error | Code: 400



```js
{
    "code": "VALIDATION_ERROR",
    "message": "teamCode must be at least 6 characters",
    "name": "ValidationError",
    "errors": [
        {
            "path": "teamCode",
            "type": "min",
            "message": "teamCode must be at least 6 characters"
        }
    ]
}
```



Status: Join Team Already Joined Another Team | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "You can only be part of one team.",
    "name": "MultipleTeamsError"
}
```



Status: Join Team Success | Code: 200



```js
{
    "avatar": "https://m.media-amazon.com/images/M/MV5BNDVkYjU0MzctMWRmZi00NTkxLTgwZWEtOWVhYjZlYjllYmU4XkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_UY268_CR0,0,182,268_AL_.jpg",
    "admin": "4d5e9a5f-de97-469d-bc09-0d2ad184e90a",
    "updatedAt": "2019-06-06T15:21:00.183Z",
    "members": [
        "4d5e9a5f-de97-469d-bc09-0d2ad184e90a",
        "b7add6bc-9f74-4248-938b-96d5e8d7a60b"
    ],
    "category": "Friends",
    "createdAt": "2019-06-06T15:14:38.212Z",
    "id": "a939c8ef-5a3d-461e-9abb-3e39f861e305",
    "name": "Small Town Heroes",
    "teamCode": "TEC0DE"
}
```



### 6. Leave Team



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{teamsApiHost}}/v1/teams/leave
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{}
```



***Responses:***


Status: Leave Team Success | Code: 200



```js
{
    "avatar": "https://m.media-amazon.com/images/M/MV5BNDVkYjU0MzctMWRmZi00NTkxLTgwZWEtOWVhYjZlYjllYmU4XkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_UY268_CR0,0,182,268_AL_.jpg",
    "admin": "4d5e9a5f-de97-469d-bc09-0d2ad184e90a",
    "updatedAt": "2019-06-06T15:21:58.734Z",
    "members": [
        "4d5e9a5f-de97-469d-bc09-0d2ad184e90a"
    ],
    "category": "Friends",
    "createdAt": "2019-06-06T15:14:38.212Z",
    "id": "a939c8ef-5a3d-461e-9abb-3e39f861e305",
    "name": "Small Town Heroes"
}
```



### 7. Delegate Team


Delegate the admin rights to another member of the team. This can only be performed by the current admin of the team and only to a current member of the admin's team.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{teamsApiHost}}/v1/teams/delegate
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
	"adminId": "{{adminId}}"
}
```



***Responses:***


Status: Delegate Team No Team Admin Error | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "You cannot delegate your admin rights if you are not an admin.",
    "name": "NoTeamAdminError"
}
```



Status: Delegate Team Success | Code: 200



```js
{
    "avatar": "https://static1.squarespace.com/static/5955fc221b631b7dd41ede60/t/59563d7b6b4998649f330b42/1559119093821",
    "teamCode": "8LP0K0",
    "admin": {
        "id": "4fb7b6fa-6ae2-47b3-be63-3c6237eb08ac",
        "username": "user-device12",
        "name": "user-device",
        "avatar": "https://cdn.zender.tv/assets/zender/default-avatar2.png"
    },
    "updatedAt": "2019-06-13T09:12:32.338Z",
    "members": [
        {
            "id": "2126711e-8ab1-48cc-9658-f56e3e58348f",
            "username": "user-device19",
            "name": "user-device",
            "avatar": "https://cdn.zender.tv/assets/zender/default-avatar2.png"
        },
        {
            "id": "4fb7b6fa-6ae2-47b3-be63-3c6237eb08ac",
            "username": "user-device12",
            "name": "user-device",
            "avatar": "https://cdn.zender.tv/assets/zender/default-avatar2.png"
        }
    ],
    "category": "Colleagues",
    "createdAt": "2019-06-13T09:11:20.733Z",
    "id": "02192059-568c-4e3d-ae1a-b2b5c82d8f6e",
    "name": "Delegate Team 2"
}
```



Status: Delegate Team Not Part Of A Team Error | Code: 404



```js
{
    "code": "NOT_FOUND",
    "message": "You are currently not part of a team.",
    "name": "NotFoundError"
}
```



Status: Delegate Team Not A Member Error | Code: 409



```js
{
    "code": "CONFLICT",
    "message": "The user to which your admin rights will be delegated is not member of your team.",
    "name": "NotAMemberError"
}
```



### 8. Remove Team Member


Delegate the admin rights to another member of the team. This can only be performed by the current admin of the team and only to a current member of the admin's team.


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{teamsApiHost}}/v1/teams/removeMember/{{memberId}}
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
}
```



---
[Back to top](#zender-public-api)
> Made with &#9829; by [thedevsaddam](https://github.com/thedevsaddam) | Generated at: 2019-09-11 14:51:37 by [docgen](https://github.com/thedevsaddam/docgen)
