# Theia JSON View

> Display JSON objects in HTML including **collapsible** navigation.

**[Live Demo](https://clubside.github.io/Theia-JSON-View/)**

## Install

Copy sources from git repository and link the minified file to your HTML document:

```html
<script src="TheiaJSONView/dist/TheiaJSONView.min.js"></script>
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

### `TheiaJSONView([json [, element[, config] ]])`

#### `json` (`Object` or `String`)

The JSON you want to display. If a string is passed during initialization it will be validated and converted if posible, or an error object will be inserted. Objects and arrays will be accepted as is.

#### `element` (`String`)

The ID of the element in your HTML document that will contain the control.

#### `config` (`Object`)

Default:

```js
{
  theme: 'default',
  fontfamily: 'ui-monospace, Menlo, Monaco, "Cascadia Mono", "Segoe UI Mono", "Roboto Mono", "Oxygen Mono", "Ubuntu Monospace", "Source Code Pro", "Fira Mono", "Droid Sans Mono", "Courier New", monospace',
  fontsize: '1rem',
  autocollapse: 0,
  allowcollapse: true,
  itemcounts: false,
  itemnumbers: false,
  rollups: false
}
```

Available configurations:

| Property | Value |
| --- | --- |
| `theme` | a `string` that must be one of these Themes: `['default', 'dark', 'light', 'material']`. |
| `fontfamily` | a `string` that is a valid CSS `font-family` |
| `fontsize` | a `string` that is a valid CSS `font-size` |
| `autocollapse` | a `number` representing how many levels deep to automatically collapse. |
| `allowcollapse` | a `boolean` that determines whether or not expand/collapse functionality is available to the user. Combined with autocollapse you can restrict how deep the data is visible. |
| `itemcounts` | a `boolean` that determines whether or not to display the number of children of an array/object. |
| `itemnumbers` | a `boolean` that determines whether or not to display the item numbers of children as a virtual key. |
| `rollups` | a `boolean` that determines whether or not to look at child objects for the singular of the parent and use that value as a key. |

## License

[MIT](./LICENSE)
