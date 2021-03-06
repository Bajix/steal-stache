[![Build Status](https://travis-ci.org/canjs/steal-stache.png?branch=master)](https://travis-ci.org/canjs/steal-stache)

# steal-stache



Load can-stache templates with StealJS

## Usage

This package will configure Steal so that you can import templates. Start by installing with NPM.

```shell
npm install steal-stache --save
```

And then assuming you are using NPM with Steal like:

```html
<script src="node_modules/steal/steal.js"></script>
```

All you have to do is import the template:

```js
import template from "./main.stache";
```


- <code>[__steal-stache__ Object](#steal-stache-object)</code>
  - <code>[STACHE_MODULE_NAME!steal-stache](#stache_module_namesteal-stache)</code>

## API


## <code>__steal-stache__ Object</code>

A [StealJS](http://stealjs.com) extension that allows stache templates as dependencies.


### <code>STACHE_MODULE_NAME!steal-stache</code>


Import a [can-stache stache] module in your code and use it to render.

```js
var template = require("./main.stache");
var Map = require("can-map");

var map = new Map();
var frag = template(map);

// frag is a live-bound DocumentFragment
```


1. __STACHE_MODULE_NAME__ <code>{moduleName}</code>:
  The module name of a stache template. This
  will typically be something like `templates/main.stache`.


- __returns__ <code>{can-stache.renderer}</code>:
  A renderer function that will render the template into a document fragment.

## Contributing

### Making a Build

To make a build of the distributables into `dist/` in the cloned repository run

```
npm install
node build
```

### Running the tests

Tests can run in the browser by opening a webserver and visiting the `test.html` page.
Automated tests that run the tests from the command line in Firefox can be run with

```
npm test
```
