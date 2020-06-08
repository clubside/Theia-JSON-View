# Theia JSON Viewer

> Display JSON objects in HTML including **collapsible** navigation.

**[Live Demo](https://clubside.github.io/Theia-JSON-View/)**

## Install

Copy sources from git repository and link the minified file to your HTML document:

```html
<script src="TheiaJSONViewer/dist/TheiaJSONViewer.min.js"></script>
```

## Usage

Create a new instance of the TheiaJSONView class passing it your data and ID of the HTML element in your document to serve as host:

```js
var data = {
  "foobar": "foobaz"
}
var tjt = new TheiaJSONView(data, 'mydiv')
```

## API

### `PPJSONView([json [, element[, config] ]])`

#### `json` (`Object` or `String`)

The JSON you want to display. If a string is passed during initialization it will be validated and converted if posible, or an error object will be inserted. Objects and arrays will be accepted as is.

#### `element` (`String`)

The ID of the element in your HTML document that will contain the control.

#### `config` (`Object`)

Default:

```js
{
  theme: 'default',
  fontfamily: '"Fira Code", "Roboto Mono", Consolas, "Courier New", monospace',
  fontsize: '1rem',
  autocollapse: 0,
  allowcollapse: true,
  itemcounts: false,
  itemnumbers: false,
  rollups: false
}
```

Available configurations:

#### Theme

* `theme`: a string that can be any of these options: `['default', 'dark', 'light', 'material']`.

#### Font Family

* `fontfamily`: a string that is a valid `font-family`.

#### Font Size

* `fontsize`: a string that is a valid `font-size`.

#### Auto Collapse

* `autocollapse`: a number representing how many levels deep to automatically collapse.

#### Allow Collapse

* `allowcollapse`: a boolean that determines whether or not expand/collapse functionality is available to the user. Combined with autocollapse you can restrict how deep the data is visible.

#### Item Counts

* `itemcounts`: a boolean that determines whether or not to display the number of children of an array/object.

#### Item Numbers

* `itemnumbers`: a boolean that determines whether or not to display the item numbers of children as a virtual key.

#### Roll-ups

* `rollups`: a boolean that determines whether or not to look at child objects for the singular of the parent and use that value as a key.

## License

[MIT](./LICENSE)
