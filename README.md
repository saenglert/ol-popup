# OpenLayers Popup

Basic popup overlay for an ['ol'](https://github.com/openlayers/openlayers) map. By
default the map is centred so that the popup is entirely visible.

Compatible with OpenLayers version 3, 4, 5 and 6 (see note in [Install - Parcel,
Webpack etc.](#parcel-webpack-etc) regarding installing the appropriate version
of `ol-popup` for OpenLayers).

## Examples

The examples demonstrate usage and can be viewed online thanks to [raw.githack.com](http://raw.githack.com/):

-   [Basic usage](http://raw.githack.com/walkermatt/ol-popup/master/examples/popup.html)
    -   Create a popup instance, show it on single-click specifying the content
-   [DOM Events](http://raw.githack.com/walkermatt/ol-popup/master/examples/dom-events.html)
    -   Handle DOM events triggered by interacting with elements within the popup content
-   [Scroll](http://raw.githack.com/walkermatt/ol-popup/master/examples/scroll.html)
    -   Controlling popup dimensions and scrolling overflowing content
-   [Multiple popups](http://raw.githack.com/walkermatt/ol-popup/master/examples/multiple.html)
    -   Add a new popup each time the maps is clicked
-   [Bundling with `ol` package (Parcel, Webpack...)](https://github.com/walkermatt/ol-popup-examples)
    -   To use the popup with the [`ol` package](https://www.npmjs.com/package/ol) and a module bundler such as Parcel, Webpack etc. see [ol-popup-examples](https://github.com/walkermatt/ol-popup-examples).

The source for all examples can be found in [examples](examples).

## Install

### Browser

#### JS

Load `ol-popup.js` after OpenLayers. The popup overlay is available as `Popup` or `ol.Overlay.Popup`.

```HTML
<script src="https://unpkg.com/ol-popup@5.0.0"></script>
```

#### CSS

```HTML
<link rel="stylesheet" href="https://unpkg.com/ol-popup@5.0.0/src/ol-popup.css" />
```

### Parcel, Webpack etc.

NPM package: [ol-popup](https://www.npmjs.com/package/ol-popup).

#### JS

Install the package via `npm`

    npm install ol-popup --save

:warning: If you're using the [`ol` package](https://www.npmjs.com/package/ol) prior to v5 you'll need to install `ol-popup@v3.0.0`.

#### CSS

The CSS file `ol-popup.css` can be found in `./node_modules/ol-popup/src`

To use the popup with the [`ol` package](https://www.npmjs.com/package/ol) and a module bundler such as Parcel, Webpack etc. see [ol-popup-examples](https://github.com/walkermatt/ol-popup-examples).

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [Popup](#popup)
    -   [show](#show)
    -   [hide](#hide)
    -   [isOpened](#isopened)

### Popup

**Extends ol.Overlay**

OpenLayers Popup Overlay.
See [the examples](./examples) for usage. Styling can be done via CSS.

**Parameters**

-   `opt_options` **olx.OverlayOptions** options as defined by ol.Overlay. Defaults to
    `{autoPan: true, autoPanAnimation: {duration: 250}}`

#### show

Show the popup.

**Parameters**

-   `coord` **ol.Coordinate** Where to anchor the popup.
-   `html` **([String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [HTMLElement](https://developer.mozilla.org/docs/Web/HTML/Element))** String or element of HTML to display within the popup.

Returns **[Popup](#popup)** The Popup instance

#### hide

Hide the popup.

Returns **[Popup](#popup)** The Popup instance

#### isOpened

Indicates if the popup is in open state

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Whether the popup instance is open

## Contributing

Contributions are welcome, please [create an issue](https://github.com/walkermatt/ol-popup/issues) first to discuss any potential contributions.

### Updating README.md

The API section of the `README.md` is generated from the [JSDoc](http://usejsdoc.org/) comments in the source code. To update the API docs edit the comments in the code then run:

    npm run doc

In order to use the `doc` npm script you will need to install the `devDependencies`:

    npm install --only=dev

## License

MIT (c) Matt Walker.

## Credit

Based on an example by [Tim Schaub](https://github.com/tschaub) posted on the
[OL3-Dev list](https://groups.google.com/forum/#!forum/ol3-dev).

## Also see

If you find the popup useful you might also like the
[ol-layerswitcher](https://github.com/walkermatt/ol-layerswitcher).
