# stemmer [![Build Status](https://travis-ci.org/wooorm/stemmer.svg?branch=master)](https://travis-ci.org/wooorm/stemmer) [![Coverage Status](https://img.shields.io/coveralls/wooorm/stemmer.svg)](https://coveralls.io/r/wooorm/stemmer?branch=master)

A pretty fast version of the [Porter stemming algorithm](http://tartarus.org/martin/PorterStemmer/).

## Installation

npm:
```sh
$ npm install stemmer
```

Component:
```sh
$ component install wooorm/stemmer
```

Bower:
```sh
$ bower install stemmer
```

## Usage

```js
var stemmer = require('stemmer');

stemmer("considerations"); // "consider"
stemmer("detestable"); // "detest"
stemmer("vileness"); // "vile"
```

## Other Porter Stemmer implementations

- [NaturalNode/natural](https://github.com/NaturalNode/natural) — Currently [buggy](https://github.com/NaturalNode/natural/issues/176).
- [jedp/porter-stemmer](https://github.com/jedp/porter-stemmer) — Has a nice memorizing feature, which might be useful!

## Benchmark

Run the benchmark yourself:

```sh
$ npm run install-benchmark # Just once of course.
$ npm run benchmark
```

On a MacBook Air, it runs about 751,000 op/s, which is more than twice as fast as the runner-up.

```
           stemmer — this module
  747 op/s » op/s * 1,000

           porterStemmer
  367 op/s » op/s * 1,000

           natural - fails on 558 out of 23532 unit tests
   59 op/s » op/s * 1,000
```

## License

MIT @ Titus Wormer
