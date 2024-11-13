![](https://badgen.net/badge/Editor.js/v2.0/blue)

# List Tool for Editor.js

This tool is deprecated and is no longer supported.
You can use the [New List tool](https://github.com/editor-js/list) with more functionality and compatibility with old data

![](assets/example.gif)

## Installation

Get the package

```shell
yarn add @editorjs/list
```

Include module at your application

```javascript
import List from "@editorjs/list";
```

Optionally, you can load this tool from CDN [JsDelivr CDN](https://cdn.jsdelivr.net/npm/@editorjs/list@latest)

## Usage

Add the List Tool to the `tools` property of the Editor.js initial config.

```javascript
import EditorJS from '@editorjs/editorjs';
import List from '@editorjs/list';

var editor = EditorJS({
  // ...
  tools: {
    ...
    list: {
      class: List,
      inlineToolbar: true,
      config: {
        defaultStyle: 'unordered'
      }
    },
  },
});
```

## Config Params

| Field        | Type     | Description                                                    |
| ------------ | -------- | -------------------------------------------------------------- |
| defaultStyle | `string` | type of a list: `ordered` or `unordered`, default is `ordered` |

## Tool's settings

![](https://capella.pics/bf5a42e4-1350-499d-a728-493b0fcaeda4.jpg)

You can choose list`s type.

## Output data

| Field | Type       | Description                              |
| ----- | ---------- | ---------------------------------------- |
| style | `string`   | type of a list: `ordered` or `unordered` |
| items | `string[]` | the array of list's items                |

```json
{
    "type" : "list",
    "data" : {
        "style" : "unordered",
        "items" : [
            "This is a block-styled editor",
            "Clean output data",
            "Simple and powerful API"
        ]
    }
},
```

## I18n support

This tool supports the [i18n api](https://editorjs.io/i18n-api).
To localize UI labels, put this object to your i18n dictionary under the `tools` section:

```json
"list": {
  "Ordered": "Нумерованный",
  "Unordered": "Маркированный"
}
```

See more instructions about Editor.js internationalization here: [https://editorjs.io/internationalization](https://editorjs.io/internationalization)
