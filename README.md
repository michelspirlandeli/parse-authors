# parse-authors [![NPM version](https://img.shields.io/npm/v/parse-authors.svg)](https://www.npmjs.com/package/parse-authors) [![Build Status](https://img.shields.io/travis/jonschlinkert/parse-authors.svg)](https://travis-ci.org/jonschlinkert/parse-authors)

> Parse a string into an array of objects with `name`, `email` and `url` properties following npm conventions. Useful for the `authors` property in package.json or for parsing an AUTHORS file into an array of authors objects.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install parse-authors --save
```

## Usage

```js
var authors = require('parse-authors');

authors('Jon Schlinkert <jon.schlinkert@sellside.com> (https://github.com/jonschlinkert)');
//=> [{name: 'Jon Schlinkert', email: 'jon.schlinkert@sellside.com', url: 'https://github.com/jonschlinkert'}]

authors('Jon Schlinkert <jon.schlinkert@sellside.com>\nBrian Woodward (https://github.com/doowb)<');
//=>
// [
//  {name: 'Jon Schlinkert', email: 'jon.schlinkert@sellside.com', url: ''},
//  {name: 'Brian Woodward', email: '', url: 'https://github.com/doowb'}
// ]
```

Any of the properties can be used or missing:

```js
authors()
//=> {name: '', email: '', url: ''}

authors('Jon Schlinkert (https://github.com/jonschlinkert)');
//=> [{name: 'Jon Schlinkert', email: '', url: 'https://github.com/jonschlinkert'}]
```

## Related projects

* [author-regex](https://www.npmjs.com/package/author-regex): Regular expression for parsing an `author` string into an object following npm conventions. | [homepage](https://github.com/jonschlinkert/author-regex)
* [parse-author](https://www.npmjs.com/package/parse-author): Parse a string into an object with `name`, `email` and `url` properties following npm conventions.… [more](https://www.npmjs.com/package/parse-author) | [homepage](https://github.com/jonschlinkert/parse-author)
* [stringify-author](https://www.npmjs.com/package/stringify-author): Stringify an authors object to `name <email> (url)`. | [homepage](https://github.com/jonschlinkert/stringify-author)

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/parse-authors/issues/new).

## Building docs

Generate readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install verb && npm run docs
```

Or, if [verb](https://github.com/verbose/verb) is installed globally:

```sh
$ verb
```

## Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016 [Jon Schlinkert](https://github.com/jonschlinkert)
Released under the [MIT license](https://github.com/jonschlinkert/parse-authors/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on March 21, 2016._