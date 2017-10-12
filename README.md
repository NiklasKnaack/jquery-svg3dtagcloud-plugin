# SVG 3D Tag Cloud jQuery plugin
(jquery-svg3dtagcloud-plugin)

## Preview

![Alt text](https://user-images.githubusercontent.com/10435486/31490134-3dc7ef7a-af43-11e7-8acf-4e2c6aca3721.png "Preview")

## Description

A very small and CSS-less jQuery plugin for drawing a 3D, interactive, SVG based and fully customizable sphere tag cloud from an array of html links.

## Examples

### JSFiddle

* <https://jsfiddle.net/NiklasKnaack/wr9moazp/>

### More Examples

* <http://nkunited.de/jquery/plugins/svg3dtagcloudV2/example1.html>
* <http://nkunited.de/jquery/plugins/svg3dtagcloudV2/example2.html>
* <http://nkunited.de/jquery/plugins/svg3dtagcloudV2/example3.html>
* <http://nkunited.de/jquery/plugins/svg3dtagcloudV2/example4.html>

## Installation

Coming soon.

## Example Usage

### HTML

```html
<script src='https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js'></script>
<script src='js/jquery.svg3dtagcloud.min.js'></script>

<link href='https://fonts.googleapis.com/css?family=Oswald&subset=latin,latin-ext' rel='stylesheet' type='text/css'>
```

### Define entries (text tags):
```js
var entries = [ 
    
    { label: 'Dev Blog', url: 'http://niklasknaack.blogspot.de/', target: '_top' },
    { label: 'Flashforum', url: 'http://www.flashforum.de/', target: '_top' },
    { label: 'jQueryScript.net', url: 'http://www.jqueryscript.net/', target: '_top' },
    { label: 'Javascript-Forum', url: 'http://forum.jswelt.de/', target: '_top' },
    { label: 'JSFiddle', url: 'https://jsfiddle.net/user/NiklasKnaack/fiddles/', target: '_top' },
    { label: 'CodePen', url: 'http://codepen.io/', target: '_top' },
    { label: 'three.js', url: 'http://threejs.org/', target: '_top' },
    { label: 'WebGLStudio.js', url: 'http://webglstudio.org/', target: '_top' },
    { label: 'JS Compress', url: 'http://jscompress.com/', target: '_top' },
    { label: 'TinyPNG', url: 'https://tinypng.com/', target: '_top' },
    { label: 'Can I Use', url: 'http://caniuse.com/', target: '_top' },
    { label: 'URL shortener', url: 'https://goo.gl/', target: '_top' },
    { label: 'HTML Encoder', url: 'http://www.opinionatedgeek.com/DotNet/Tools/HTMLEncode/Encode.aspx', target: '_top' },
    { label: 'Twitter', url: 'https://twitter.com/niklaswebdev', target: '_top' },
    { label: 'deviantART', url: 'http://nkunited.deviantart.com/', target: '_top' },
    { label: 'Gulp', url: 'http://gulpjs.com/', target: '_top' },
    { label: 'Browsersync', url: 'https://www.browsersync.io/', target: '_top' },
    { label: 'GitHub', url: 'https://github.com/', target: '_top' },
    { label: 'Shadertoy', url: 'https://www.shadertoy.com/', target: '_top' },
    { label: 'Starling', url: 'http://gamua.com/starling/', target: '_top' },
    { label: 'jsPerf', url: 'http://jsperf.com/', target: '_top' },
    { label: 'Foundation', url: 'http://foundation.zurb.com/', target: '_top' },
    { label: 'CreateJS', url: 'http://createjs.com/', target: '_top' },
    { label: 'Velocity.js', url: 'http://julian.com/research/velocity/', target: '_top' },
    { label: 'TweenLite', url: 'https://greensock.com/docs/#/HTML5/GSAP/TweenLite/', target: '_top' },
    { label: 'jQuery', url: 'https://jquery.com/', target: '_top' },
    { label: 'jQuery Rain', url: 'http://www.jqueryrain.com/', target: '_top' },
    { label: 'jQuery Plugins', url: 'http://jquery-plugins.net/', target: '_top' },

];
```

### Define entries (text tags with tooltips):
```js
var entries = [ 
    
    { label: 'Dev Blog', url: 'http://niklasknaack.blogspot.de/', target: '_top', tooltip: 'Lorem ipsum' },
    { label: 'Flashforum', url: 'http://www.flashforum.de/', target: '_top', tooltip: 'Dolor sit amet' },
    { label: 'jQueryScript.net', url: 'http://www.jqueryscript.net/', target: '_top', tooltip: 'Consetetur sadipscing' },
    { label: 'Javascript-Forum', url: 'http://forum.jswelt.de/', target: '_top', tooltip: 'Sed diam' },
    { label: 'JSFiddle', url: 'https://jsfiddle.net/user/NiklasKnaack/fiddles/', target: '_top' },
    { label: 'CodePen', url: 'http://codepen.io/', target: '_top', tooltip: 'At vero' },
    { label: 'three.js', url: 'http://threejs.org/', target: '_top', tooltip: 'Nonumy eirmod' },
    { label: 'WebGLStudio.js', url: 'http://webglstudio.org/', target: '_top', tooltip: 'Stet clita' },
    { label: 'JS Compress', url: 'http://jscompress.com/', target: '_top', tooltip: 'Justo duo' },
    { label: 'TinyPNG', url: 'https://tinypng.com/', target: '_top', tooltip: 'Ut wisi enim' },
    { label: 'Can I Use', url: 'http://caniuse.com/', target: '_top', tooltip: 'Minim veniam' },
    { label: 'URL shortener', url: 'https://goo.gl/', target: '_top', tooltip: 'Quis nostrud' },
    { label: 'HTML Encoder', url: 'http://www.opinionatedgeek.com/DotNet/Tools/HTMLEncode/Encode.aspx', target: '_top' },
    { label: 'Twitter', url: 'https://twitter.com/niklaswebdev', target: '_top', tooltip: 'Veniam isictus' },
    { label: 'deviantART', url: 'http://nkunited.deviantart.com/', target: '_top', tooltip: 'Autem insto' },
    { label: 'Gulp', url: 'http://gulpjs.com/', target: '_top', tooltip: 'Officia dolor' },
    { label: 'Browsersync', url: 'https://www.browsersync.io/', target: '_top', tooltip: 'Digi tal' },
    { label: 'GitHub', url: 'https://github.com/', target: '_top', tooltip: 'Amet et quam' },
    { label: 'Shadertoy', url: 'https://www.shadertoy.com/', target: '_top', tooltip: 'Meno equox' },
    { label: 'Starling', url: 'http://gamua.com/starling/', target: '_top', tooltip: 'Duis autem' },
    { label: 'jsPerf', url: 'http://jsperf.com/', target: '_top', tooltip: 'Soluta nobis' },
    { label: 'Foundation', url: 'http://foundation.zurb.com/', target: '_top', tooltip: 'Blandit praesent' },
    { label: 'CreateJS', url: 'http://createjs.com/', target: '_top', tooltip: 'Dignissim qui' },
    { label: 'Velocity.js', url: 'http://julian.com/research/velocity/', target: '_top', tooltip: 'Et iusto odio' },
    { label: 'TweenLite', url: 'https://greensock.com/docs/#/HTML5/GSAP/TweenLite/', target: '_top', tooltip: 'Facilisis at vero' },
    { label: 'jQuery', url: 'https://jquery.com/', target: '_top', tooltip: 'Dolore eu' },
    { label: 'jQuery Rain', url: 'http://www.jqueryrain.com/', target: '_top', tooltip: 'In vulputate' },
    { label: 'jQuery Plugins', url: 'http://jquery-plugins.net/', target: '_top', tooltip: 'In vulputate' }

];
```

### Define entries (image tags):
```js
var entries = [ 

    { image: './img/Basket.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Briefcase.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Brush.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Calendar.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Camera.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Cassette.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Clock.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Cloud_Download.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Cloud_Upload.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Coffee.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Comments.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Credit_Card.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Diary.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Document.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Envelope.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Eraser.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/File_Browser.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Games.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Headphones.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Heart.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Home.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/ID.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/iPod.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Key.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Location.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Location_Map.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Map.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Megaphone.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Message.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Microphone.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Mobile.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Money.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Padlock.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Pencil.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Photo.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Polaroid.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Printer.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Record.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Save.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Scissors.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Spanner.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Toolbox.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' },
    { image: './img/Umbrella.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top' }

];
```

### Define entries (image tags with tooltips):
```js
var entries = [ 
   
    { image: './img/Basket.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Lorem ipsum' },
    { image: './img/Briefcase.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Dolor sit amet' },
    { image: './img/Brush.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Consetetur sadipscing' },
    { image: './img/Calendar.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Sed diam' },
    { image: './img/Camera.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'At vero' },
    { image: './img/Cassette.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Nonumy eirmod' },
    { image: './img/Clock.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Stet clita' },
    { image: './img/Cloud_Download.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Justo duo' },
    { image: './img/Cloud_Upload.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Ut wisi enim' },
    { image: './img/Coffee.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Minim veniam' },
    { image: './img/Comments.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Quis nostrud' },
    { image: './img/Credit_Card.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Exerci tation' },
    { image: './img/Diary.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Duis autem' },
    { image: './img/Document.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Vel eum iriure' },
    { image: './img/Envelope.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Dolor in hendrerit' },
    { image: './img/Eraser.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'In vulputate' },
    { image: './img/File_Browser.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Velit esse' },
    { image: './img/Games.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Molestie consequat' },
    { image: './img/Headphones.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Vel illum' },
    { image: './img/Heart.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Dolore eu' },
    { image: './img/Home.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Feugiat nulla' },
    { image: './img/ID.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Facilisis at vero' },
    { image: './img/iPod.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Eros et accumsa' },
    { image: './img/Key.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Et iusto odio' },
    { image: './img/Location.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Dignissim qui' },
    { image: './img/Location_Map.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Blandit praesent' },
    { image: './img/Map.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Nam liber' },
    { image: './img/Megaphone.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Soluta nobis' },
    { image: './img/Message.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Magna aliquam' },
    { image: './img/Microphone.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Duis autem' },
    { image: './img/Mobile.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Lori novis' },
    { image: './img/Money.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Meno eqiam' },
    { image: './img/Padlock.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Meno equox' },
    { image: './img/Pencil.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Iri orem' },
    { image: './img/Photo.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Orel pas' },
    { image: './img/Polaroid.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Psi sit' },
    { image: './img/Printer.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Amet et quam' },
    { image: './img/Record.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Molare cons' },
    { image: './img/Save.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Digi tal' },
    { image: './img/Scissors.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Felenope liber' },
    { image: './img/Spanner.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Officia dolor' },
    { image: './img/Toolbox.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Autem insto' },
    { image: './img/Umbrella.png', width: '50', height: '50', url: 'http://niklasknaack.de/', target: '_top', tooltip: 'Veniam isictus' }

];

```

### Define settings:
```js
var settings = {

    entries: entries,
    width: 480,
    height: 480,
    radius: '65%',
    radiusMin: 75,
    bgDraw: true,
    bgColor: '#111',
    opacityOver: 1.00,
    opacityOut: 0.05,
    opacitySpeed: 6,
    fov: 800,
    speed: 2,
    fontFamily: 'Oswald, Arial, sans-serif',
    fontSize: '15',
    fontColor: '#fff',
    fontWeight: 'normal',//bold
    fontStyle: 'normal',//italic 
    fontStretch: 'normal',//wider, narrower, ultra-condensed, extra-condensed, condensed, semi-condensed, semi-expanded, expanded, extra-expanded, ultra-expanded
    fontToUpperCase: true,
    tooltipFontFamily: 'Oswald, Arial, sans-serif',
    tooltipFontSize: '11',
    tooltipFontColor: '#fff',
    tooltipFontWeight: 'normal',//bold
    tooltipFontStyle: 'normal',//italic 
    tooltipFontStretch: 'normal',//wider, narrower, ultra-condensed, extra-condensed, condensed, semi-condensed, semi-expanded, expanded, extra-expanded, ultra-expanded
    tooltipFontToUpperCase: false,
    tooltipTextAnchor: 'left',
    tooltipDiffX: 0,
    tooltipDiffY: 10

};
```

### jQuery:

```js
$( '#holder' ).svg3DTagCloud( settings );
```

### JS:

```js
var svg3DTagCloud = new SVG3DTagCloud( document.getElementById( 'holder'  ), settings );
```

## License

This plugin is available under [the MIT license](http://mths.be/mit).

## Author

_– [Niklas](http://niklasknaack.de/)_