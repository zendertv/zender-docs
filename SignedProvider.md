# Signed Provider Authentication
In many cases, customers want to keep control/ownership over the user data and the authentication process. Zender provides a signed provider authentication mechanism that makes that possible.

# Authentication flow
This diagram explains how the signed provider flow works:

![Zender Signed Provider Diagram](docs/images/signed-provider-diagram.png?raw=true "Zender Signed Provider Diagram")

- First the user starts the app
- Then the user logs in (or is already logged in)
- The user authenticates against the customer authentication endpoint and an App session is created

- When the app is about to start the Zender Player, it first asks a signed token
- The customer endpoint provides the user with a signed token which contains the user information, a signature (using a shared secret) and a timestamp

- This signed token is then passed to the authentication of the Zender Player
- Then the player starts and the signedToken is sent to the Zender Authentication for verification

- The Zender Authentication verifies the signature using the shared secret
- It checks that the signature is not too old
- On successful verification it will extract the user information from the token and create a Zender User if it doesn't exist already
- From then on the Zender Player has successfully logged in the user and works with its own Zender Session

# Requirements:
The Signed Provider needs additional backend configuration.

- requires a valid zender targetId and channelId
- requires a valid shared secret
- requires "signedProvider" to be configured on the backend
- validity of the signature
- endpoint to redirect users to for login purposes (web)
- requires synchronized clock on signing backend
- requires decision on signing expiration time

# Signed Provider Token format
## Preparing the signedToken
Let's say we have user with the following information:
```
{
	"id":"<some internal customer userId>",
	"first_name":"Patrick",
	"last_name":"Debois",
	"avatar":"https://...",
}
```

The signature is based on a mutually agreed signature Template:
```
signature_date = `${new Date().getTime() / 1000}`; // seconds since epoch
secretDecoded = Buffer.from(secret, "base64"); // secret is base64 first decode it
hmac = crypto.createHmac( "sha1", secretDecoded); // prepare the hmac signing
hmac.update(`${signature_date}_${token.id}_${token.first_name}_${token.last_name}`);
signature = hmac.digest(`${signature_date}_${token.id}_${token.first_name}_${token.last_name}`);
tokenData = {
	"id":"<some internal customer userId>",
	"first_name":"Patrick",
	"last_name":"Debois",
	"avatar":"https://...",
	"signature_date":signature_date
};
signedToken = base64(JSON.stringify(tokenData)) // creates a string
```

- signature_date is seconds since last epoch
- signature_date is needs to be generated on server side, this will minimize the drift when signature validity is checked.
- signature is a hmac.digest("base64") of a templated string

## Authentication Payload Format
- provider: "signedProvider"
- payload:
```json
{
	"token" : signedToken
}
```


## Verifying a token

```javascript
const body = {
        provider: "signedProvider",
        token: "<signedToken>",
        targetId: "<targetId>"
};

// Instructions to validate the generate token
console.log(`curl https://api.zender.tv/v1/auth/login -d '${JSON.stringify(body)}' -H 'Content-Type: application/json' -v`);
```
