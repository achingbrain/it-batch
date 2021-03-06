# it-batch

[![Build status](https://travis-ci.org/achingbrain/it-batch.svg?branch=master)](https://travis-ci.org/achingbrain/it-batch?branch=master) [![Coverage Status](https://coveralls.io/repos/github/achingbrain/it-batch/badge.svg?branch=master)](https://coveralls.io/github/achingbrain/it-batch?branch=master) [![Dependencies Status](https://david-dm.org/achingbrain/it-batch/status.svg)](https://david-dm.org/achingbrain/it-batch)

> Takes an async iterator that emits things and emits them as fixed-size batches

The final batch may be smaller than the max.

## Install

```sh
$ npm install --save it-batch
```

## Usage

```javascript
const batch = require('it-batch')
const all = require('it-all')

// This can also be an iterator, async iterator, generator, etc
const values = [0, 1, 2, 3, 4]
const batchSize = 2

const result = await all(batch(values, batchSize))

console.info(result) // [0, 1], [2, 3], [4]
```
