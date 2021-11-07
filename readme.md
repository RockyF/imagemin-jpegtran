# imagemin-jpegtran

默认使用淘宝镜像，或者通过环境变量 `JPEGTRAN_BINARY_SITE` 设置

> jpegtran imagemin plugin

## Install

```
$ npm install --save imagemin-jpegtran
```

## Usage

```js
const imagemin = require('imagemin');
const imageminJpegtran = require('imagemin-jpegtran');

(async () => {
	await imagemin(['images/*.jpg'], {
		destination: 'build/images',
		plugins: [
			imageminJpegtran()
		]
	});

	console.log('Images optimized');
})();
```

## API

### imageminJpegtran(options?)(buffer)

Returns a promise for a buffer.

#### options

Type: `object`

##### progressive

Type: `boolean`\
Default: `false`

Lossless conversion to progressive.

##### arithmetic

Type: `boolean`\
Default: `false`

Use [arithmetic coding](http://en.wikipedia.org/wiki/Arithmetic_coding).

#### buffer

Type: `buffer`

Buffer to optimize.
