[Base64](https://en.wikipedia.org/wiki/Base64) encoding and decoding
from [CryptoJS](https://code.google.com/p/crypto-js/).

[![Build Status](https://travis-ci.org/p-j/meteor-crypto-base64.svg)](https://travis-ci.org/p-j/meteor-crypto-base64)

Dependency
----------
- [`jparker:crypto-core`](https://github.com/p-j/meteor-crypto-core).

Install
-------

Inside your project folder run
```
$ meteor add jparker:crypto-base64
```
The following methods under the `CryptoJS` namespace will now be available
on **both the client and server**:

* `var words  = CryptoJS.enc.Base64.parse('SGVsbG8sIFdvcmxkIQ==');`
* `var base64 = CryptoJS.enc.Base64.stringify(words);`


Usage
-----

Base64 encode a literal string:
```javascript
CryptoJS.enc.Base64.stringify(CryptoJS.enc.Utf8.parse('Hello, World!'));
// "SGVsbG8sIFdvcmxkIQ=="
```

Note that Base64 encoding is done on *byte arrays*, not character arrays
(i.e. strings). Strings are logical character arrays, not byte arrays.
Character arrays need to first be transformed into byte arrays by choosing
a character encoding (Utf8, Utf16 or Utf16LE) to transform each character
into a sequence of one or more bytes. Once you've got a byte array,
then you can Base64 encode it.


See also
--------
The CryptoJS project lives at <https://code.google.com/p/crypto-js/> and
the documentation for encoders, including Base64, is at
<https://code.google.com/p/crypto-js/#Encoders>.


Related packages
----------------

- [`jparker:crypto-md5`](https://github.com/p-j/meteor-crypto-md5)
- [`jparker:crypto-sha1`](https://github.com/p-j/meteor-crypto-sha1)
- [`jparker:crypto-sha256`](https://github.com/p-j/meteor-crypto-sha256)
- [`jparker:crypto-hmac`](https://github.com/p-j/meteor-crypto-hmac)
- [`jparker:crypto-aes`](https://github.com/p-j/meteor-crypto-aes)

Credits
-------

Based on [Dan Dascalescu's work](https://github.com/dandv/meteor-crypto-base64)
