# Zender Payout
After a quiz has finished , payout information is available in the admin and can be exported as both generic csv and Paypal csv format.

To automate this one can retrieve the information to automatically do payments:


# To retrieve the payout information
A payout is related to a quiz where the results have been triggered.

To retrieve the payout you need to:
- find the streamId -  See [Retrieve Stream Information](STREAM.md)
- find the quizId - See [Retrieve Quiz Information](QUIZ.md)

```
curl --location --request GET "https://api.zender.tv/v1/channels/<channelId>/streams/<streamId>/quiz/<quizId>/leaderboard/win/export" \
  --header "Content-Type: application/json"
```

# To retrieve the quiz winners
See [Retrieve Quiz Information](QUIZ.md)
