# Filter

[![NPM version][npm-image]][npm-url]
[![Build status][travis-image]][travis-url]
[![Test coverage][coveralls-image]][coveralls-url]
[![Gittip][gittip-image]][gittip-url]

Filter an object, array or string and keep the result as the same type.

## Installation

```
npm install util-filter --save
```

## Usage

```javascript
var filter = require('util-filter');

// Filter over objects.
filter({
  a: 0,
  b: 1,
  c: 2
}, function (value, key, obj) {
  return value < 2;
});
//=> { a: 0, b: 1 }

// Filter over arrays.
filter(['a', 'b', 'c'], function (value, key, obj) {
  return key % 2;
});
// => ['b']

// Filter over strings.
filter('abc', function (value, key, obj) {
  return true;
});
//=> 'abc'
```

## License

MIT

[npm-image]: https://img.shields.io/npm/v/util-filter.svg?style=flat
[npm-url]: https://npmjs.org/package/util-filter
[travis-image]: https://img.shields.io/travis/blakeembrey/filter.svg?style=flat
[travis-url]: https://travis-ci.org/blakeembrey/filter
[coveralls-image]: https://img.shields.io/coveralls/blakeembrey/filter.svg?style=flat
[coveralls-url]: https://coveralls.io/r/blakeembrey/filter?branch=master
[gittip-image]: https://img.shields.io/gittip/blakeembrey.svg?style=flat
[gittip-url]: https://www.gittip.com/blakeembrey
