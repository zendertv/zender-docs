# To retrieve Quiz Information:

## To retrieve the basic quiz information for all quizes a particular stream
Using an qdmin/api bearer token you can retrieve all quiz information

```
curl -XGET 'https://api.zender.tv/v1/channels/<channelId>/streams/<streamId>/quiz' -H 'content-type: application/json' -H 'authorization: Bearer <bearerToken>' -H 'accept: application/json' | jq
[
  
    "id": "df209242-4097-479c-ac83-76a4cb8e288c",  <= unique quizId
    "streamId": "abe2c3fb-a60a-41ee-b6e3-a649755bdea2",
    "createdAt": "2018-04-03T14:28:23.237Z",
    "endedAt": "2018-08-28T15:20:03.647Z",
    "status": "ended",
    "startedAt": "2018-08-28T15:19:43.003Z",
    "updatedAt": "2018-08-28T15:20:03.647Z",
    "answerTime": 10000,
    "hideTime": 15000,
    "description": "Test",
    "price": 500, <= the amout of prize money
    "resultsAt": "2018-08-28T15:19:46.402Z", <= indicates if the results have been triggered
    "title": "Test Quiz"
  
]
```

## Retrieve quizzes that have finished
To filter out the quizzes that have finished , filter on streams that have a `resultsAt`

```
curl -XGET 'https://api.zender.tv/v1/channels/<channelId>/streams/<streamId>/quiz' -H 'content-type: application/json' -H 'authorization: Bearer <bearerToken>' -H 'accept: application/json' | jq '.[] | select(.resultsAt) | .id'
```

## To retrieve detailed results for a specific Quiz:
Now that you can find all the quizzes, you can retreive details such as the results of one quiz:

```
curl -XGET 'https://api.zender.tv/v1/channels/<channelId>/streams/<streamId>/quiz/<quizId>/results' -H 'authorization: Bearer <bearerToken>' -H 'content-type: application/json' -H 'accept: application/json'

{
    "winners": [
        
            "id": "309ae678-b9ec-42b0-86fc-d4de304c7dcd",
            "name": "Jan Willem",
            "avatar": "https://graph.facebook.com/1854345981301940/picture?width=250&type=square"
        
    ],
    "count": 1 <= number of winners

}
```
