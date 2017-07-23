This fork has been modified to include a ![check](https://github.com/danielkberry/pronounceable/commit/cd55de0e23c3dd5621fefc43052c4d07e3cac6f3#diff-9180527083ad702353498dbbb188b3c7) which requires all pronounceable words to have at least one vowel in them. 

# pronounceable

[![Build Status](https://travis-ci.org/lukem512/pronounceable.svg?branch=master)](https://travis-ci.org/lukem512/pronounceable) ![Dependency Status](https://david-dm.org/lukem512/pronounceable.svg) [![npm](https://img.shields.io/npm/l/pronounceable.svg)](https://www.npmjs.com/package/pronounceable) [![npm](https://img.shields.io/npm/v/pronounceable.svg)](https://www.npmjs.com/package/pronounceable) [![npm](https://img.shields.io/npm/dm/pronounceable.svg)](https://www.npmjs.com/package/pronounceable)

Pronounceable is a small module that allows you to test a word for pronounceability.

To use it, simply install via NPM and include it in your project file.

```
const pronounceable = require('pronounceable');
```

Then, to test a word for pronounceability, use the `test` method.

```
console.log(pronounceable.test('samosa')); // true
console.log(pronounceable.test('xghsii')); // false
```

You can also use the module to score a word on its pronounceability, using the `score` method. The higher the output value the more pronounceable the word.

```
console.log(pronounceable.score('peonies')); // 0.10176356810708122
console.log(pronounceable.score('sshh')); // 0.0008556941146173743
```

To generate your own dataset use the `train` method.

```
pronounceable.train('dictionary.txt', function(probabilities) {
  // The data set has been returned
  console.log(probabilities);
});
```
