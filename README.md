# \<autobahn-connection\>

## Overview
autobahn-connection creates an autobahn connection. By default, the connection is configured to use the cookie and WAMP-CRA methods, and the router address is set to ```<document.location.origin>/ws```.

## Installation

Use [Bower](bower.io) to get the latest version of autobahn-connection

```
$ bower install autobahn-connection
```

If your browser does not have native support for webcomponents, make sure to include it. It's a good idea to do this conditionally (as per [Polymer for the Performance-obsessed'](https://aerotwist.com/blog/polymer-for-the-performance-obsessed/)); alternatively, a plain old script tag will do:

```html
<script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
```

Then import the element in your page:

```html
<link rel="import" href="bower_components/autobahn-connection/autobahn-connection.html">
```

## Example Usage
Declare the element:

```html
<autobahn-connection on-autobahn-auth-accepted="fooAuthAccepted" on-autobahn-auth-denied="fooAuthDenied"></autobahn-connection>
```

Add a listener to the autobahn-auth-accepted and autobahn-auth-denied events.

```html
<script>
	Polymer({
		fooAuthDenied: function() {
			console.log('auth denied!');
		},
		fooAuthAccepted: function() {
			console.log('auth accepted');
		}
	})
</script>
```

For more information on the library, see [autobahn.ws](autobahn.ws/js).
