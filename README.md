# QRCode.js
QRCode.js is javascript library for making QRCodes as SVG, canvas/PNG ot table.
QRCode.js has no dependencies, not even for the demo anymore.

## Basic Usages
```
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://example.com");
</script>
```

or with some options

```
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://example.com",
	width: 128,
	height: 128,
	output: "svg", // or "table" or the default "canvas" to generate a PNG data-URL.
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H
});
</script>
```

and you can use some methods

```
qrcode.clear(); // clear the code. Important if switching output method!
qrcode.makeCode("http://naver.com"); // make another code.
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License

## Upstream
 * https://github.com/davidshimjs/qrcodejs (idle since 2014)
 * https://github.com/jeromeetienne/jquery-qrcode (idle since 2017)
