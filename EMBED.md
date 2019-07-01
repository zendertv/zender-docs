# Integrate Zender Live Player in own website

Embedding the Zender Player is as easy as adding an iframe to your website.

# Choosing the right Zender player url

The easiest way of integrating it to use the following url:
`https://player2.zender.tv/<targetId>/channels/<channelId>/streams`

- targetId: maps to a specific customer
- channelId: maps to a specific channel for a specific customer

This will show the player inside the iframe and will automatically resize.

Both targetId and channelId will be provided to you on the creation of your Zender account. They can also be found through the Zender admin console.

# Zender Lobby mechanism
By default when no streams are public there will nothing to see.
You can change this behaviour by creating a *lobby* stream : this stream will be active when no other streams are public.
The player will switch from lobby and back when another stream becomes public

# Example Code
It all starts with a div element where you add zender iframe into.

Then depending if your stream is 16:9 (landscape) or 9:16 (portrait) you want to use a different sizing. (use the correct class)

```html
<div class="zender-frame-wrapper-9-16">
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

```javascript
// Set zender-frame source depending on URL.
window.addEventListener('load', function(e) {
	document.getElementById('zender-frame').src = getPlayerUrl();
});
```

# Listening to Zender Player events

## Login via iframe messages
If you are using the cookie provider for your login you can listen for a trigger-login message to execute some code in your surrounding webpage.

### Zender player → website

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

### Website → Zender player

```javascript
var iframe = document.getElementById('zender-frame');
iframe.contentWindow.postMessage('logged-in', '*');
```

## Listen to player events (Experimental)
```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Parent Window</title>
</head>
<body>

    <h1>Parent Window</h1>
    <p>Got Message:</p>
    <div id="results"></div>
    <br/>

    <script>
        // addEventListener support for IE8
        function bindEvent(element, eventName, eventHandler) {
            if (element.addEventListener){
                element.addEventListener(eventName, eventHandler, false);
            } else if (element.attachEvent) {
                element.attachEvent('on' + eventName, eventHandler);
            }
        }
        var iframeSource = 'https://player2.zender.tv/<targetId>/<channelId>/streams
        // Create the iframe
        var iframe = document.createElement('iframe');
        iframe.setAttribute('src', iframeSource);
        iframe.setAttribute('id', 'the_iframe');
        iframe.style.width = 1024 + 'px';
        iframe.style.height = 768 + 'px';
        document.body.appendChild(iframe);

        // Send a message to the child iframe
        var iframeEl = document.getElementById('the_iframe'),
            results = document.getElementById('results');

        // Listen to message from child window
        bindEvent(window, 'message', function (e) {
            results.innerHTML = JSON.stringify(e.data);
        });
    </script>
</body>
</html>


```

# Logging in via Signed Provider
The Zender Web Player understands social login providers such as Google,Facebook.
Signed provider is authentication mechanism that allows you to easily integrate your own existing authentication mechanism.

This authentication is passed like this : `https://live.yoursite.com?loginData=<signed token>`

In this case the login data will be parsed by the zender player by examining its query string. In the example here, the parent page also receives the login data via its own query string; see the getLoginData function. The login data is then transmitted to the Zender iframe in the getPlayerUrl function.

For more details see the [Signed Provider Documentation](SignedProvider.md)

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


