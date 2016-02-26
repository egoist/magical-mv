# magical-move [![NPM version](https://img.shields.io/npm/v/magical-move.svg)](https://npmjs.com/package/magical-move) [![NPM downloads](https://img.shields.io/npm/dm/magical-move.svg)](https://npmjs.com/package/magical-move) [![Build Status](https://img.shields.io/circleci/project/egoist/magical-move/master.svg)](https://circleci.com/gh/egoist/magical-move)

> mv with data replacement.

## Install

```bash
$ npm install --save magical-move
```

## Usage

```js
const move = require('magical-move')

/** source.js:
hello {{ name }}
*/
move('./source.js', './output.js', {name: 'egoist'})
	.then(content => {
		console.log('Done!')
	})
/** output.js:
hello egoist
*/
```

## CLI

### Install

```bash
$ npm install -g magical-move
```

### Usage

```bash
# same result as above
$ move source.js output.js --name egoist
```

## API

### move(from, to, [data, handlebarsOpts])

**from** `String` source file

**to** `String` output file

**data** `Object` The data to render template

**handlebarsOpts** `Object` Options for `handlebars.compile`

### move.sync

Same options but synchronously.

## License

MIT © [EGOIST](https://github.com/egoist)
