# lazy-cache [![NPM version](https://badge.fury.io/js/lazy-cache.svg)](http://badge.fury.io/js/lazy-cache)

> Cache requires to be lazy-loaded when needed.

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i lazy-cache --save
```

## Usage

```js
var lazyCache = require('lazy-cache');
var glob = lazyCache(require)('glob');

// `glob` is a now a function that should be called when needed
glob().sync('foo/*.js');
```

The module is also added as a property to the `lazy` function
so it can be called without having to call a function first.

```js
var lazy = lazyCache(require);
lazy('glob');

// `lazy.glob` is not a getter property that can be used.
lazy.glob.sync('foo/*.js');
```

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/lazy-cache/issues/new)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2015 Jon Schlinkert
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on August 18, 2015._