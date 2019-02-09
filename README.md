# feathers-query-filters-aggregate

[![Greenkeeper badge](https://badges.greenkeeper.io/feathersjs/feathers-query-filters.svg)](https://greenkeeper.io/)

NOTE: This fork provides limited support for the following aggregate functions:
- $groupBy
- $min
- $max
- $sum

> Adds support for special query string params used for filtering data in [FeatherJS](https://github.com/feathersjs)

[![Build Status](https://travis-ci.org/feathersjs/feathers-query-filters.png?branch=master)](https://travis-ci.org/feathersjs/feathers-query-filters)
[![Code Climate](https://codeclimate.com/github/feathersjs/feathers-query-filters/badges/gpa.svg)](https://codeclimate.com/github/feathersjs/feathers-query-filters)
[![Test Coverage](https://codeclimate.com/github/feathersjs/feathers-query-filters/badges/coverage.svg)](https://codeclimate.com/github/feathersjs/feathers-query-filters/coverage)
[![Dependency Status](https://img.shields.io/david/feathersjs/feathers-query-filters.svg?style=flat-square)](https://david-dm.org/feathersjs/feathers-query-filters)
[![Download Status](https://img.shields.io/npm/dm/feathers-query-filters.svg?style=flat-square)](https://www.npmjs.com/package/feathers-query-filters)
[![Slack Status](http://slack.feathersjs.com/badge.svg)](http://slack.feathersjs.com)


## Getting Started

`feathers-query-filters-aggregate` is used internally by the [database service adapters](http://docs.feathersjs.com/databases/readme.html) to support [pagination and sorting](http://docs.feathersjs.com/databases/pagination.html).

To install:
- npm install feathers-query-fitlers-aggregate --save

## To Use
You will need to make a minor edit to the feathers-waterline node module as follows:

1. Open /node_modules/feathers-waterline/lib/index.js in your code editor
2. Find the line at the require block at the top of the file that requires feathers-query-filters. In the current version as of the writing of this documentation, it is line 18, and reads 'var _feathersQueryFilters = require('feathers-query-filters');'
3. Replace 'feathers-query-filters' with 'feathers-query-filters-aggregate'

Restart feathers to refresh the node module linking. You will now be able to add the $groupBy, $sum, $min and $max functions to your query syntax.

## License

[MIT](LICENSE)

## Author

[Feathers contributors](https://github.com/feathersjs/feathers-query-filters/graphs/contributors)
