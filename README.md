[![NPM Version](https://badge.fury.io/js/states-us.svg)](https://badge.fury.io/js/states-us)
[![Build Status](https://travis-ci.org/justinlettau/states-us.svg?branch=master)](https://travis-ci.org/justinlettau/states-us)
[![Dev Dependency Status](https://david-dm.org/justinlettau/states-us/dev-status.svg)](https://david-dm.org/justinlettau/states-us?type=dev)
[![codecov](https://codecov.io/gh/justinlettau/states-us/branch/master/graph/badge.svg)](https://codecov.io/gh/justinlettau/states-us)

# US States

List of US states and territories.

# Installation

```bash
npm install states-us --save
```

# Usage

```js
import states from 'states-us';

console.log(states);
// => all states and territories

const example1 = states.filter(x => x.contiguous);
console.log(example1);
// => contiguous states only

const example2 = states.filter(x => x.territory);
console.log(example2);
// => territories only

const example3 = states.map(x => x.abbreviation);
console.log(example2);
// => all state/territory abbreviations
```

The default export from `states-us` is an array of object with the following structure:

| Property       | Type      | Description                            | Example  |
| -------------- | --------- | -------------------------------------- | -------- |
| `name`         | `string`  | State name.                            | `Alaska` |
| `abbreviation` | `string`  | State abbreviation.                    | `AK`     |
| `territory`    | `boolean` | Indicates if the state is a territory. | `false`  |
| `contiguous`   | `boolean` | Indicates if the state is contiguous.  | `false`  |

# Development

```
npm install
npm run build
```
