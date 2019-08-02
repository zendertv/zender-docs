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
Here is a sample code for nodejs to calculate the tokens

```javascript
const crypto = require('crypto');  
const querystring = require("querystring");

// ArabMillionaire
let secret = "<your-secret>";
let targetId = "<your-target-id>";
let channelId = "<your-channel-id>";

function sign(user,secret) {
    	const secretDecoded = Buffer.from(secret, "base64"); // the provided secret is base64, so it needs to be decoded first
	const signature_date = new Date().getTime() / 1000; // seconds since epoch

	const hmac = crypto.createHmac( "sha1", secretDecoded); // prepare the hmac signing
	hmac.update(`${signature_date}_${user.id}_${user.first_name}_${user.last_name}`); // use the agreed signing template

	const signature = hmac.digest("base64"); // calculate the signature , base64

	userData = {
		"id": user.id,
		"first_name": user.first_name,
		"last_name": user.last_name,
		"avatar": user.avatar,
		"signature_date": signature_date,
		"signature" : signature,
	};

	signedToken = JSON.stringify(userData); // stringify the json structure
	return signedToken;
}

// A sample user information
let userInfo = {
		"id":"testuserId",
		"first_name": "Test",
		"last_name": "User",
		"avatar": "https://ui-avatars.com/api/?background=0D8ABC&color=fff"
};

// Sign the user Info with the secret
const token=sign(userInfo,secret);


// Calculate the url

const encryptedBytes = Buffer.from(token);
encodedToken = encryptedBytes.toString('base64'); // base64 encode the token

const params = querystring.stringify({signedToken: encodedToken });

let url=`https://player2.zender.tv/${targetId}/channels/${channelId}?${params}`
console.log("Direct Loginurl ===>");
console.log();
console.log(url);

console.log();
// Calculate the API call
const body = {
        provider: "signedProvider",
        token: token,
        targetId: targetId
};

console.log("API Call via the cli ===>");
console.log();
// Instructions to validate the generate token
console.log(`curl https://api.zender.tv/v1/auth/login -d '${JSON.stringify(body)}' -H 'Content-Type: application/json' -v`);
console.log();
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
