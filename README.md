![jaco](http://jaco-project.github.io/docs/jaco.png)
====

Japanese Character Optimizer.

[![NPM version](https://badge.fury.io/js/jaco.svg)](http://badge.fury.io/js/jaco)
[![Bower version](https://badge.fury.io/bo/jaco.svg)](http://badge.fury.io/bo/jaco)
[![Build Status](https://travis-ci.org/jaco-project/jaco-js.svg)](https://travis-ci.org/jaco-project/jaco-js)
[![Dependency Status](https://david-dm.org/jaco-project/jaco-js.svg)](https://david-dm.org/jaco-project/jaco-js)
[![devDependency Status](https://david-dm.org/jaco-project/jaco-js/dev-status.svg)](https://david-dm.org/jaco-project/jaco-js#info=devDependencies)

## What is

This module optimize Japanese characters.

Convert to Katakana from Hiragana mutually, or sort list by natural phonetic order, or convert to halfwidth from fullwidth mutually.

## functions

- Convert Hiragana <-> Katakana
- Convert halfwidth <-> fullwidth
- Check Hiragana, Katakana, halfwidth, fullwidth, and so on.
- Sort by natural phonetic order.
  - Supported voiced marks, prolonged sound marks, iteration marks.
- Has compatible native string object API.

## install

### for browser

```sh
$ bower install jaco
```

### for NodeJS

```sh
$ npm install jaco
```

### CLI

```sh
$ npm install -g jaco
```

## Usage

### for browser

```html
<script src="jaco.min.js"></script>
<script>
jaco.katakanize('ニホンゴのモジなど'); // => ニホンゴノモジナド
jaco.hiraganize('ニホンゴのモジなど'); // => にほんごのもじなど

var jStr01 = new jaco.Jaco('ニホンゴのモジなど');
jStr01.toKatakana(); // => ニホンゴノモジナド
</script>
```

### for NodeJS

```javascript
var jaco = require('jaco');

jaco.katakanize('ニホンゴのモジなど'); // => ニホンゴノモジナド
jaco.hiraganize('ニホンゴのモジなど'); // => にほんごのもじなど

var jStr01 = new jaco.Jaco('ニホンゴのモジなど');
jStr01.toKatakana(); // => ニホンゴノモジナド
```

### CLI

```
Usage: jaco [options] <string> [fileOption] <path>

Options:

    -h, --help                 output usage information
    -V, --version              output the version number
    -f, --file <path>          convert in file
    -o, --output <path>        output to file
    -K, --katakanize [string]  katakanize method
    -H, --hiraganize [string]  hiraganize method
```

## Methods

### Static Functions

```javascript
jaco.katakanize('ニホンゴのモジなど');
```

name|return type
---|---
[katakanize](http://jaco-project.github.io/jaco/docs/modules/jaco.html#katakanize)|`string`
[hiraganize](http://jaco-project.github.io/jaco/docs/modules/jaco.html#hiraganize)|`string`
hiraganaOnly|`boolean`
katakanaOnly|`boolean`
naturalKanaSort|`Array`

### Instance methods of Class Jaco

```javascript
var instance = new jaco.Jaco('ニホンゴのモジなど');
instance.toString();
```

name|return type|bang|chainable
---|---|---|---
[toString](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tostring)|`string`|✗|✗
[valueOf](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#valueof)|`string`|✗|✗
[concat](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#concat)|`Jaco`|✓|✓
[slice](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#slice)|`Jaco`|✗|✓
[substr](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#substr)|`Jaco`|✗|✓
[substring](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#substring)|`Jaco`|✗|✓
[append](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#append)|`Jaco`|✓|✓
[prepend](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#prepend)|`Jaco`|✓|✓
[replace](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#replace)|`Jaco`|✓|✓
[trim](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#trim)|`Jaco`|✓|✓
[remove](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#remove)|`Jaco`|✓|✓
[test](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#test)|`Jaco`|✓|✓
[is](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#is)|`boolean`|✗|✗
[isEmpty](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#isempty)|`boolean`|✗|✗
[isOnly](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#isonly)|`boolean`|✗|✗
[isOnlyHiragana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#isonlyhiragana)|`boolean`|✗|✗
[isOnlyKatakana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#isonlykatakana)|`boolean`|✗|✗
[isNumeric](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#isnumeric)|`boolean`|✗|✗
[toNumeric](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tonumeric)|`Jaco`|✓|✓
[combinate](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#combinate)|`Jaco`|✓|✓
[toLowerCase](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tolowercase)|`Jaco`|✓|✓
[toUpperCase](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#touppercase)|`Jaco`|✓|✓
[toHiragana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tohiragana)|`Jaco`|✓|✓
[toKatakana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tokatakana)|`Jaco`|✓|✓
[toNarrowKatakana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tonarrowkatakana)|`Jaco`|✓|✓
[toWideKatakana](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#towidekatakana)|`Jaco`|✓|✓
[toNumber](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#tonumber)|`number`|✗|✗
[size](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#size)|`number`|✗|✗
[byteSize](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#bytesize)|`number`|✗|✗
[clone](http://jaco-project.github.io/jaco/docs/classes/jaco.jaco.html#clone)|`Jaco`|✓|✓
toNarrowJapneseSymbol|`Jaco`|✓|✓
toWideJapnese|`Jaco`|✓|✓
toNarrow|`Jaco`|✓|✓
toWide|`Jaco`|✓|✓
addVoicedMarks|`Jaco`|✓|✓
addSemivoicedMarks|`Jaco`|✓|✓
removeVoicedMarks|`Jaco`|✓|✓
convertProlongedSoundMarks|`Jaco`|✓|✓
convertIterationMarks|`Jaco`|✓|✓
toBasicLetter|`Jaco`|✓|✓
hasSmallLetter|`boolean`|✗|✗
toPhoeticKana|`Jaco`|✓|✓
replaceMap|`Jaco`|✓|✓

## Documents

[http://jaco-project.github.io/docs/](http://jaco-project.github.io/docs/)
