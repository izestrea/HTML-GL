<img alt="HTML GL" src="http://pixelscommander.com/polygon/htmlgl/figures/logo-blue.png"/>

60 FPS by rendering HTML/CSS in WebGL, framework agnostic
=========================================================

[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/PixelsCommander/HTML-GL)

Smooth animations and responsive interactions are top priority problems of cross-platform Web development. Since desktop browsers are mostly fine with handling animations, mobile and embedded devices still provide bad user experience.
The biggest reason for animations to be janky is that "DOM is slow". It is true since DOM is quite complex model and every DOM change create a ripple of events or chain reaction over whole document.

[Article about](http://pixelscommander.com/en/web-applications-performance/render-html-css-in-webgl-to-get-highest-performance-possibl/)

HTML GL solves "the slow DOM problem" by creating WebGL representations of DOM elements and hiding actual DOM after. As a result you still work with HTML/CSS as you are common to, but DOM elements are just facades to their WebGL represenations. These GPU accelerated textures are very effective from resources consuming perspective and are very cheap to transform or animate.

Usage
-----

As jQuery plugin

```html
    $('.some div').htmlgl();
'''

As Web Component

```html
<html-gl>
    This element`s content is rendered in <h1>WebGL</h1>
    <span style="color: green;">was it easy?</span>
    Feel free to use CSS, images and all you are common to in HTML/CSS world.
</html-gl>
```

No DOM + WebGL rendering = highest FPS possible for Web platform
-------------------------------------------------------

<img alt="HTML GL flow diagram" src="http://pixelscommander.com/polygon/htmlgl/figures/htmlgl-flow-diagram.png"/>

Demos
-----

- [Basic HTML GL](http://pixelscommander.com/polygon/htmlgl/demo/basic-webgl.html) demo shows how to use HTML GL and animate GL Elements. It also demonstrate that HTML GL handle content change events and repaints element`s WebGL representation
- [Basic DOM](http://pixelscommander.com/polygon/htmlgl/demo/basic-dom.html) this is the same project as previous. The only difference is that htmlgl.js is not included
- [Advanced content HTML GL](http://pixelscommander.com/polygon/htmlgl/demo/advanced-content-webgl.html) slider with nested content rendered via WebGL and animated, ability to move with mouse horizontaly
- [Advanced content DOM](http://pixelscommander.com/polygon/htmlgl/demo/advanced-content-dom.html)

How to use?
-----------
Use tag name ```<html-gl>``` on elements you are going to animate. These elements will be rendered in WebGL also their CSS Transform properties will be mapped to WebGL representation transformations. So DOM element itself will not be animated or displayed in order to avoid resources consuming.
HTML GL is framework agnostic and is easy to inject into existing project which needs performance tweaking.

License
-------
MIT: http://mit-license.org/

Copyright 2015 Denis Radin aka [PixelsCommander](http://pixelscommander.com)
