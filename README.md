# QRCode.js
QRCode.js is a pure client-side javascript library for rendering QRCodes as SVG, canvas/PNG, or html table.
QRCode.js has no dependencies, not even for the demo anymore.

## Basic Usage
```html
<div id="qrcode"></div>

<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://example.com");
</script>
```

or with some options

```html
<div id="qrcode"></div>

<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://example.com",
	width:  128,
	height: 128,
	border:   4,   // 4 is the default, and is standards-compliant
	output: "svg", // or "table" or the default "canvas" to generate a PNG data-URL.
	colorDark:    "#000000",
	colorLight:   "#ffffff",
	correctLevel: QRCode.CorrectLevel.H,
	imgStyle:     "display:block; max-width:100%; margin-left:auto; margin-right:auto;"
	    // style for img tag produced by canvas/png renderer
});
</script>
```

and you can use some methods

```javascript
    qrcode.setCode("http://example.com");
        // change the qr code using all current settings and output method
    qrcode.destruct();
        // removes all created elements, canvas png, svg, table, follow by new QRCode(originalDiv, ...)
    
    // DEPRECATED:
    qrcode.clear();
        // DEPRECATED: svg and table same as destruct, but canvas/png works differently by only emptying canvas
        // this is for backwards compatibility
    qrcode.makeCode("http://example.com");
        // DEPRECATED calls setCode(str)
```

## Demonstration
[https://github.com/locandy/qrcodejs/blob/improve-documentation/index.html](https://htmlpreview.github.io/?https://github.com/locandy/qrcodejs/blob/master/index.html)

## Browser Compatibility
Edge, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, etc. and possibly even IE6~10.

## License
MIT License

## Upstream
 * https://github.com/davidshimjs/qrcodejs (idle since 2014)
 * https://github.com/jeromeetienne/jquery-qrcode (idle since 2017)
