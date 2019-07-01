# Zender Authentication 
Zender supports several authentication mechanisms including social logins (Instagram, Youtube, Google, Facebook).

To authenticate a user:
- Zender will delegate the authentication to an external provider
- That login provider generates a token
- That token is send to the Zender Platform
- The Zender Platform verifies that token
- If the token is valid, Zender will either extract the user information from the token or query the login provider for extra user information

This allows you to keep all user information in your own CRM system and re-use existing authentication providers.
Additional you only need to pass a limited subset of user information to the Zender platform to comply with GDPR regulations.

# Terminology
- Login Provider: the mechanism used to login (device,signedProvider, Facebook, Google, Instagram, Youtube)
- Login Payload: the required fields to pass to the login provider

# Required and optional user information

# Authentication Providers Payload
## Device authentication

- provider: "device"
- payload:
```json
{
'token': '',
	'avatar': 'https://example.com/myavatar.png',
    'name': username
}
```

The image the avatar points to is best limited in size ~ 256x256

## Facebook authentication

- provider: "facebook"
- payload:
```json
{
	'token': '<facebook-token>'
}
```

## Google authentication

- provider: "google"
- payload:
```json
{
	'token': '<google-token>'
}
```

## Phone/Email authentication
This uses Facebook AccountKit

- provider: "accountkit"
- payload:
```json
{
	'token': '<accountkit-token>'
}
```

## Signed Provider
This login method allows for integration of external authentication (like existing non-social authentication).
More details can be found at [Signed Provider Documentation](SignedProvider.md)

- provider: "signedProvider"
- payload:
```json
{
	'token': '<accountkit-token>'
}
```

# Native flow:
User has not logged in zender
- In a native app, the customer App first authenticates the user and then generates the correct signature
- The app can then login with that information to the Zender Platform (API POST request)
- The Zender backend validates the signature
- If the signature is valid, a zender User/ Session is created

User has already logged in zender:
- Upon successful authentication, Zender will generate its own session so no second login is required unless the session has expired.

User logout:
- A user can log out via the menu in Zender.
Note: when a user signs out of the customer website, a user is still logged in Zender

# Sample Authentication Code 
## iOS
```objective-c
ZenderAuthentication *authentication = [ZenderAuthentication authenticationWith:@{
  @"<key>": @"<value>",
  @"<key>": @"<value>",
  @"<key>": @"<value>"
} provider:@"<provider>"];

self.player.authentication=authentication;
```

## Android
```java
HashMap authPayload = new HashMap<String, String>();
authPayload.put("<key>","<value>");
authPayload.put("<key>","<value>");
authPayload.put("<key>","<value>");
ZenderAuthentication authentication = new ZenderAuthentication(authPayload,"<provider>");
```

## React Native
```javascript
const zenderAuthentication = {
 provider: "signedProvider" , // Json Authentication
 payload: {
   "<key>": "<value>",
   "<key>": "<value>",
   "<key>": "<value>"
 }
}
```

