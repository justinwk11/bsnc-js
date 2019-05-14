# BSNC_Javascript API
[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

## Examples

``` javascript
var bitcoin = require('bitcoinjs-lib') // v3.x.x
var bsncJS = require('bsnc-js')
```

> sign(message, privateKey, compressed[, network.messagePrefix])

Sign a Bitcoin message
``` javascript
var keyPair = bitcoin.ECPair.fromWIF('5KYZdUEo39z3FPrtuX2QbbwGnNP5zTd7yyr2SC1j299sBCnWjss')
var privateKey = keyPair.privateKey
var message = 'This is an example of a signed message.'

var signature = bitcoinMessage.sign(message, privateKey, keyPair.compressed)
console.log(signature.toString('base64'))
// => 'G9L5yLFjti0QTHhPyFrZCT1V/MMnBtXKmoiKDZ78NDBjERki6ZTQZdSMCtkgoNmp17By9ItJr8o7ChX0XxY91nk='
```

> verify(message, address, signature[, network.messagePrefix])

Verify a Bitcoin message
``` javascript
var address = '1HZwkjkeaoZfTSaJxDw6aKkxp45agDiEzN'

console.log(bitcoinMessage.verify(message, address, signature))
// => true
```

## LICENSE [MIT](LICENSE)
