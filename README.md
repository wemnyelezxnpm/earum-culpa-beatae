# @wemnyelezxnpm/earum-culpa-beatae <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Set a function’s length.

Arguments:
 - `fn`: the function
 - `length`: the new length. Must be an integer between 0 and 2**32.
 - `loose`: Optional. If true, and the length fails to be set, do not throw. Default false.

Returns `fn`.

## Usage

```javascript
var setFunctionLength = require('@wemnyelezxnpm/earum-culpa-beatae');
var assert = require('assert');

function zero() {}
function one(_) {}
function two(_, __) {}

assert.equal(zero.length, 0);
assert.equal(one.length, 1);
assert.equal(two.length, 2);

assert.equal(setFunctionLength(zero, 10), zero);
assert.equal(setFunctionLength(one, 11), one);
assert.equal(setFunctionLength(two, 12), two);

assert.equal(zero.length, 10);
assert.equal(one.length, 11);
assert.equal(two.length, 12);
```

[package-url]: https://npmjs.org/package/@wemnyelezxnpm/earum-culpa-beatae
[npm-version-svg]: https://versionbadg.es/ljharb/@wemnyelezxnpm/earum-culpa-beatae.svg
[deps-svg]: https://david-dm.org/ljharb/@wemnyelezxnpm/earum-culpa-beatae.svg
[deps-url]: https://david-dm.org/ljharb/@wemnyelezxnpm/earum-culpa-beatae
[dev-deps-svg]: https://david-dm.org/ljharb/@wemnyelezxnpm/earum-culpa-beatae/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@wemnyelezxnpm/earum-culpa-beatae#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@wemnyelezxnpm/earum-culpa-beatae.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@wemnyelezxnpm/earum-culpa-beatae.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@wemnyelezxnpm/earum-culpa-beatae.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@wemnyelezxnpm/earum-culpa-beatae
[codecov-image]: https://codecov.io/gh/ljharb/@wemnyelezxnpm/earum-culpa-beatae/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@wemnyelezxnpm/earum-culpa-beatae/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@wemnyelezxnpm/earum-culpa-beatae
[actions-url]: https://github.com/wemnyelezxnpm/earum-culpa-beatae/actions
