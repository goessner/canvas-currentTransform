# Canvas-currentTransform

HTML canvas element's CanvasRenderingContext2D has a property [currentTransform](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-canvas-element.html#dom-context-2d-currenttransform) defined. This represents a transformation matrix as a SVGMatrix object.

There seems to be no browser [implementation activity](https://code.google.com/p/chromium/issues/detail?id=277107) at [current](https://bugzilla.mozilla.org/show_bug.cgi?id=928150).

Having this property natively supported would be of great help, as we can modify the transformation matrix by `setTransform`, `transform`, `translate`, ... methods, but we are not able to access the current transform matrix element values.

This polyfill uses the experimental `mozCurrentTransform` or `webkitCurrentTransform` properties if available or implements a lightweight transformation matrix stack otherwise.
