A simple client-side qr library that returns data URI,
packaged as a nodejs module for use with [browserify](http://browserify.org/).
Requires [canvas support](http://caniuse.com/#feat=canvas).

Originally written by Kang Seonghoon (http://hg.mearie.org/qrjs/),
packaged as a nodejs module with a slightly modified public API.

For a server-side library, see [node-qr](https://github.com/bcelenza/node-qr).

### Usage
Install with `npm install qruri` and call
`require('qruri')(data[, options ])` to get a data URI.

### Options:
- version: an integer in [1,40]. when omitted (or -1) the smallest possible
  version is chosen.
- mode: one of 'numeric', 'alphanumeric', 'octet'. when omitted the smallest
  possible mode is chosen.
- ecclevel: one of 'L', 'M', 'Q', 'H'. defaults to 'L'.
- mask: an integer in [0,7]. when omitted (or -1) the best mask is chosen.
- modulesize: a number. this is a size of each modules in pixels, and
  defaults to 5px.
- margin: a number. this is a size of margin in *modules*, and defaults to
  4 (white modules). the specficiation mandates the margin no less than 4
  modules, so it is better not to alter this value unless you know what
  you're doing.

### License
Released under qr.js's original license:

This source code is in the public domain; if your jurisdiction does not
recognize the public domain the terms of Creative Commons CC0 license
apply. In the other words, you can always do what you want.
