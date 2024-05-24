# @patrten/minus-architecto <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@patrten/minus-architecto');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@patrten/minus-architecto
[npm-version-svg]: https://versionbadg.es/inspect-js/@patrten/minus-architecto.svg
[deps-svg]: https://david-dm.org/inspect-js/@patrten/minus-architecto.svg
[deps-url]: https://david-dm.org/inspect-js/@patrten/minus-architecto
[dev-deps-svg]: https://david-dm.org/inspect-js/@patrten/minus-architecto/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@patrten/minus-architecto#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrten/minus-architecto.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrten/minus-architecto.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@patrten/minus-architecto.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrten/minus-architecto
[codecov-image]: https://codecov.io/gh/inspect-js/@patrten/minus-architecto/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@patrten/minus-architecto/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@patrten/minus-architecto
[actions-url]: https://github.com/inspect-js/@patrten/minus-architecto/actions
