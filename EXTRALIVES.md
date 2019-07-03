# Zender Extra lives
By default a user can earn *extra lives* when other people refer that persons nickname.
Sometimes you want to assign extra lives on other events: for example on signup, on completion of a form, after watching an advertisement.

# To assign an extra live to a user
To increment the user with shareCode `the-share-code` use:

```
curl --location --request POST "https://api.zender.tv/v1/extraLives" -H 'authorization: Bearer <bearerToken>' -H 'content-type: application/json' -H 'accept: application/json' \
--header "Content-Type: application/json" \
--header ": " \
--data "{
\"shareCode\": \"<the-share-code>\"
}"
```

