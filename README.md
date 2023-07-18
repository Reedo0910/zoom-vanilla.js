# zoom-vanilla.js (no offset on the enlarged images)

A simple library for image zooming; [as seen on Medium][medium-zoom-article].
It zooms in really smoothly and zooms out when you click again, scroll away,
or press the <kbd>esc</kbd> key.

If you hold the <kbd>⌘</kbd> or <kbd>Ctrl</kbd> key when clicking the image, it
will open the image in a new tab instead of zooming it.

_This is a fork of the [zoom-vanilla.js][zoom-vanilla]_. Please refer to the original doc and repo for demos and more details. These are the key
differences:

1. No offset on the enlarged images.

## Installation

1. Download the JS and CSS files by:    
    
	- Manually download `dist/zoom-vanilla.min.js` and `dist/zoom.css` from
	  GitHub

2. Add the `zoom-vanilla.min.js` and `zoom.css` files to your HTML page:

    ```html
    <!-- inside <head> -->
    <link href="path/to/dist/zoom.css" rel="stylesheet">

    <!-- before </body> -->
    <script src="path/to/dist/zoom-vanilla.min.js"></script>
    ```

    You can also `import` them if you're using webpack:

    ```javascript
    import "path/to/dist/zoom.css"
    import "path/to/dist/zoom-vanilla.min.js"
    ```

## Usage

Add a `data-action="zoom"` attribute to the images you want to make
zoomable:

```html
<img src="img/blog_post_featured.png" data-action="zoom">
```

## Browser support

zoom-vanilla.js should (in theory) work in all modern browsers. If not, create
an issue! Thanks!

[medium-zoom-article]: https://medium.com/designing-medium/image-zoom-on-medium-24d146fc0c20
[zoom-vanilla]: https://github.com/spinningarrow/zoom-vanilla.js

## Known issues

- The image is appended to the body; use an appropriate CSS selector for extra
  styling
- Zooming may not be quite right if the aspect ratio of the image is changed

## Build

- `git clone` the repo
- `npm i` to install dev dependencies
- `npm start` to start a simple HTTP server (makes it easy to view the demo
  page)
- `npm run build` to build the minified JS and vendor-prefixed CSS
- `npm run watch` to rebuild when any JS files change (recommended for
  development)
