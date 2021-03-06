# OpenLayers LayerSwitcher

Grouped layer list control with group selection checkbox for an OpenLayer map. 

To be shown in the layer switcher layers should have a `title` property; base
layers should have a `type` property set to `base`. Group layers
(`ol.layer.Group`) can be used to visually group layers together; a group with
a `fold` property set to either `open` or `close` will be displayed with a
toggle. See [Examples](#examples) for usage.

Compatible with OpenLayers version 3, 4 and 5 (see note in [Install - Parcel,
Webpack etc.](#parcel-webpack-etc) regarding installing the appropriate version
of `ol-layerswitcher` for OpenLayers).



## Examples

The examples demonstrate usage and can be viewed online thanks to [raw.githack.com](http://raw.githack.com/):

-   [Basic usage](https://raw.githubusercontent.com/munna/ol3-layerswitcher/master/examples/layerswitcher.html)
    -   Create a layer switcher control. Each layer to be displayed in the layer switcher has a `title` property as does each Group; each base map layer has a `type: 'base'` property.
    `allowSelection` property will enable checkbox to show/hide complete group on map.
    `fold` property will allow you to collaspe\expand group.
    `enableOpacitySliders` property on layer will enable slider to manage opacity.

The source for all examples can be found in [examples](examples).

## Install

### Browser

#### JS

Load `ol-layerlist.js` after OpenLayers. The layerswitcher control is available as `LayerSwitcher` or `ol.control.LayerSwitcher`.

```HTML
<script src="https://unpkg.com/ol-layerlist@1.1.8"></script>
```

#### CSS

```HTML
<link rel="stylesheet" href="https://unpkg.com/ol-layerlist@1.1.8/src/ol-layerlist.css" />
```

### Parcel, Webpack etc.

NPM package: [ol-layerlist](https://www.npmjs.com/package/ol-layerlist).

#### JS

Install the package via `npm`

    npm install ol-layerlist --save

:warning: If you're using the [`ol` package](https://www.npmjs.com/package/ol) prior to v5 you'll need to install `ol-layerlist@v1.1.8`.

#### CSS

## Tests

To run the tests you'll need to install the dependencies via `npm`. In the root of the repository run:

    npm install

Then run the tests by opening [test/index.html](test/index.html) in a browser.

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [LayerSwitcher](#layerswitcher)
    -   [setMap](#setmap)
    -   [showPanel](#showpanel)
    -   [hidePanel](#hidepanel)
    -   [renderPanel](#renderpanel)
    -   [renderPanel](#renderpanel-1)
    -   [forEachRecursive](#foreachrecursive)
    -   [uuid](#uuid)
    -   [toggleFold\_](#togglefold_)

### LayerSwitcher

**Extends ol.control.Control**

OpenLayers Layer Switcher Control.
See [the examples](./examples) for usage.

**Parameters**

-   `opt_options` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** Control options, extends olx.control.ControlOptions adding:  
    **`tipLabel`** `String` - the button tooltip.

#### setMap

Set the map instance the control is associated with.

**Parameters**

-   `map` **ol.Map** The map instance.

#### showPanel

Show the layer panel.

#### hidePanel

Hide the layer panel.

#### renderPanel

Re-draw the layer panel to represent the current state of the layers.

#### renderPanel

**Static** Re-draw the layer panel to represent the current state of the layers.

**Parameters**

-   `map` **ol.Map** The OpenLayers Map instance to render layers for
-   `panel` **[Element](https://developer.mozilla.org/docs/Web/API/Element)** The DOM Element into which the layer tree will be rendered

#### forEachRecursive

**Static** Call the supplied function for each layer in the passed layer group
recursing nested groups.

**Parameters**

-   `lyr` **ol.layer.Group** The layer group to start iterating from.
-   `fn` **[Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)** Callback which will be called for each `ol.layer.Base`
    found under `lyr`. The signature for `fn` is the same as `ol.Collection#forEach`

#### uuid

**Static** Generate a UUID  
Adapted from <http://stackoverflow.com/a/2117523/526860>

Returns **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** UUID

#### toggleFold\_

Fold/unfold layer group

**Parameters**

-   `lyr`  
-   `li`  

## License

MIT (c) 
