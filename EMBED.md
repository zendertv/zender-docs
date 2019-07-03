# Integrate Zender Live Player in own website

Embedding the Zender Player is done by adding an [`iframe`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) to your website.

## Choosing the right Zender player url

The easiest way of integrating it to use the following url:
`https://player2.zender.tv/<targetId>/channels/<channelId>/streams`

- targetId: maps to a specific customer
- channelId: maps to a specific channel for a specific customer

This will show the player inside the iframe and will automatically resize.

Both targetId and channelId will be provided to you on the creation of your Zender account. They can also be found through the Zender admin console.

### Zender Lobby mechanism
By default no streams are public and there will be nothing to see.
You can change this behaviour by creating a *lobby* stream : this stream will be active when no other streams are public.
The Player will switch from lobby and back when another stream becomes public.

## Example Code
Create a `div` element, which will act as a wrapper and add the zender `iframe` into it.
Depending if your stream is 16:9 (landscape) or 9:16 (portrait) you want to use a different sizing.
Configure either the `zender-frame-wrapper-16-9` or `zender-frame-wrapper-9-16` as a class on the wrapper.

```html
<div class="zender-frame-wrapper zender-frame-wrapper-9-16">
	<iframe src="about:blank" id="zender-frame" width="640" height="360" frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
</div>
```

```css
/* Wrapper around the zender-frame, with a 16:9 aspect-ratio */
.zender-frame-wrapper-16-9 {
	width: 100%;
	height: 0;
	padding-top: 56.25%;
	position: relative;
}
/* Wrapper around the zender-frame, with a 9:16 aspect-ratio */
.zender-frame-wrapper-9-16 {
	width: 100%;
	height: 0;
	padding-top: 177.78%;
	position: relative;
}

/* Stretch the zender-frame to the size of its wrapper */
.zender-frame-wrapper iframe {
	display: block;
	position: absolute;
	width: 100%;
	height: 100%;
	left: 0;
	right: 0;
	top: 0;
	bottom: 0;
}
```

Configure the `src` of the `iframe` with some javascript after the [load event](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event). This prevents the player from slowing down other content on the page.

```javascript
// Set zender-frame source depending on URL.
window.addEventListener('load', function(e) {
	document.getElementById('zender-frame').src = getPlayerUrl();
});
```

## Communicating with the Zender Player *(exprimental)*

### Zender player → website

**Example**
If you are using the cookie provider for your login you can listen for a `trigger-login` message to execute some code in your surrounding webpage.

```javascript
// Listen for incoming messages from zender-frame
window.addEventListener('message', function(e) {

	// Only allow messages from these URLs (note: no trailing slashes!)
	var allowedOrigins = [
		'https://yoursite.com',
	];

	// Origin checks out
	if (allowedOrigins.includes(e.origin)) {

		switch(e.data.type) {

			case 'trigger-login':
				window.showLoginform(window.location);;
				break;

		}

	}
}, false);
```

### Website → Zender Player

```javascript
var iframe = document.getElementById('zender-frame');
iframe.contentWindow.postMessage('logged-in', '*');
```

## Integrating login

*The Zender Player supports social login providers such as Google, Facebook. This section is only applicable if you want to integrate the Player with your own authentication provider*

[Signed provider](SignedProvider.md) is an authentication mechanism that allows you to easily integrate your own existing authentication mechanism. For more details see the [Signed Provider Documentation](SignedProvider.md)

**Example**

In this example, the parent page receives the login data via its own query string; see the `getLoginData` function. 
The function assumes that the authentication is passed like this : `https://live.yoursite.com?loginData=<signed token>`.
The login data is then transmitted to the Zender `iframe` in the form of a query string attached to the Player url, see the `getPlayerUrl` function.

```javascript
function getLoginData() {
  var queryString = window.location.search.slice(1).split('&');
  var loginData;
  var i;
  for (i = 0; i !== queryString.length; i++) {
    var lhs = queryString[i].split('=')[0];
    var rhs = queryString[i].slice(lhs.length + 1);
    if (lhs === 'loginData') {
      loginData = rhs;
    }
  }
  return loginData;
}
function getPlayerUrl() {
  var playerUrl = <zenderPlayerUrl>; // without the /streams/<uid>part
  if (getLoginData()) {
    return playerUrl + "?loginData=" + getLoginData();
  }
  return playerUrl;
}
```
