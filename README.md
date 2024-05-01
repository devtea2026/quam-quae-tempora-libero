ArrayBuffer.prototype.detached <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![Build Status][travis-svg]][travis-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

[![browser support][testling-svg]][testling-url]

An ES6 spec-compliant `ArrayBuffer.prototype.detached` shim. Invoke its "shim" method to shim ArrayBuffer.prototype.detached if it is unavailable.
*Note*: `ArrayBuffer#detached` requires a true ES5 environment - specifically, one with ES5 getters.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES5-supported environment and complies with the proposed [spec](https://tc39.es/proposal-arraybuffer-transfer/#sec-get-@devtea2026/quam-quae-tempora-libero).

Most common usage:
```js
var detached = require('@devtea2026/quam-quae-tempora-libero');

assert(detached(new ArrayBuffer('a') === false);

if (!ArrayBuffer.prototype.detached) {
	detached.shim();
}

assert(new ArrayBuffer('a').detached, false);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@devtea2026/quam-quae-tempora-libero
[npm-version-svg]: http://versionbadg.es/devtea2026/quam-quae-tempora-libero.svg
[travis-svg]: https://travis-ci.org/devtea2026/quam-quae-tempora-libero.svg
[travis-url]: https://travis-ci.org/devtea2026/quam-quae-tempora-libero
[deps-svg]: https://david-dm.org/devtea2026/quam-quae-tempora-libero.svg
[deps-url]: https://david-dm.org/devtea2026/quam-quae-tempora-libero
[dev-deps-svg]: https://david-dm.org/devtea2026/quam-quae-tempora-libero/dev-status.svg
[dev-deps-url]: https://david-dm.org/devtea2026/quam-quae-tempora-libero#info=devDependencies
[testling-svg]: https://ci.testling.com/devtea2026/quam-quae-tempora-libero.png
[testling-url]: https://ci.testling.com/devtea2026/quam-quae-tempora-libero
[npm-badge-png]: https://nodei.co/npm/@devtea2026/quam-quae-tempora-libero.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@devtea2026/quam-quae-tempora-libero.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@devtea2026/quam-quae-tempora-libero.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@devtea2026/quam-quae-tempora-libero
