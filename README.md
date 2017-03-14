# Fontello Webpack Plugin

WIP

---

## Install

```bash
npm install fontello-webpack-plugin
```

## Usage

`/webpack.config.js`
```js
const FontelloPlugin = require("fontello-webpack-plugin")

module.exports = {
	"entry": "index.js",
	/* ... */
	plugins: [
		new FontelloPlugin({
			config: require("./fontello.config.json")
			/* ...options */
		})
	]
}
```

## Options

```js
new FontelloPlugin(options: Object)
```

|Name|Type|Default|Description|
|----|----|-------|-----------|
|config|`Object`|-|Configuration generated by [http://fontello.com](Fontello.com).
|className|`String`|`""`|Base class name. Use this if your configuration doesn't have a prefix.<sup>1</sup>
|fonts|`Array`|`[ "eot", "woff", "woff2", "ttf", "svg" ]`|Font types supported.
|name|`String`|`"icons"`|Module name.
|output.css|`String`|`"[name].css"`|Css output path
|output.font|`String`|`"font/[name].[ext]"`|Fonts output path
<sup>1</sup> When `config.css_prefix_text` is empty a base class name is required to target all icons in css. If no prefix or class name is provided base styles are not emited.