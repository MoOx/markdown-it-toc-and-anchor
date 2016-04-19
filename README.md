# markdown-it-toc-and-anchor [![Travis Build Status](https://travis-ci.org/MoOx/markdown-it-toc-and-anchor.svg)](https://travis-ci.org/MoOx/markdown-it-toc-and-anchor)

> markdown-it plugin to add toc and anchor links in headings

## Installation

```console
$ npm install markdown-it-toc-and-anchor
```

## Usage

### ES6

```js
import markdownIt from "markdown-it"
import markdownItTocAndAnchor from "markdown-it-toc-and-anchor"

markdownIt({
    html: true,
    linkify: true,
    typography: true,
  })
    .use(markdownItTocAndAnchor, {
      // ...options
    })
    .render(md)
```

### ES5 / CommonJS

```js
var markdownIt = require('markdown-it'),
    markdownItTocAndAnchor = require('markdown-it-toc-and-anchor').default;

markdownIt({
    html: true,
    linkify: true,
    typography: true,
  })
    .use(markdownItTocAndAnchor, {
      // ...options
    })
    .render(md)
```

:information_source: Note that the 'default' property has to be used when requiring this plugin, this is due to the use of Babel 6 now making ES6 compliant exports ([Misunderstanding ES6 Modules, Upgrading Babel, Tears, and a Solution
](https://medium.com/@kentcdodds/misunderstanding-es6-modules-upgrading-babel-tears-and-a-solution-ad2d5ab93ce0#.enq6dfcnn))

### Options

#### `toc`

(default: `true`)

Allow you to enable/disable the toc transformation of `@[toc]`

#### `tocClassName`

(default: `"markdownIt-TOC"`)

Option to customize html class of the `<ul>` wrapping the toc

#### `tocFirstLevel`

(default: `1`)

Allow you to skip some heading level. Example: use 2 if you want to skip `<h1>`
from the TOC.

#### `tocLastLevel`

(default: `6`)

Allow you to skip some heading level. Example: use 5 if you want to skip `<h6>`
from the TOC.

#### `anchorLink`

(default: `true`)

Allow you to enable/disable the anchor link in the headings

#### `anchorLinkSymbol`

(default: `"#"`)

Allow you to customize the anchor link symbol

#### `anchorLinkSpace`

(default: `true`)

Allow you to enable/disable inserting a space between the anchor link and heading.

#### `anchorLinkSymbolClassName`

(default: `null`)

Allow you to customize the anchor link symbol class name. If not null, symbol will be rendered as `<span class="anchorLinkSymbolClassName">anchorLinkSymbol</span>`.

#### `anchorLinkBefore`

(default: `true`)

Allow you to prepend/append the anchor link in the headings

#### `anchorClassName`

(default: `"markdownIt-Anchor"`)

Allow you to customize the anchor link class

#### `resetIds`

(default: `true`)

Allow you to reset (or not) ids incrementation. Use it if you will have multiple
documents on the same page.

#### `indentation`

(default: `"  "`)

Allow you to customize indentation

---

## CONTRIBUTING

* ⇄ Pull requests and ★ Stars are always welcome.
* For bugs and feature requests, please create an issue.
* Pull requests must be accompanied by passing automated tests (`$ npm test`).

## [CHANGELOG](CHANGELOG.md)

## [LICENSE](LICENSE)
