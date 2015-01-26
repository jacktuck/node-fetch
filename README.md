
node-fetch
==========

[![npm version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]

A light-weight module that brings `window.fetch` to node.js


# Motivation

I really like the notion of Matt Andrews' [isomorphic-fetch](https://github.com/matthew-andrews/isomorphic-fetch): it bridges the API gap between client-side and server-side http requests, so developers have less to worry about.

But I think the term [isomorphic](http://isomorphic.net/) is generally misleading: it gives developers a false sense of security that their javascript code will run happily on both controlled server environment as well as uncontrollable user browsers. When the latter is only true for a small subset of modern browsers, not to mention quirks in native implementation.

Instead of implementing `XMLHttpRequest` in node to run browser-specific [fetch polyfill](https://github.com/github/fetch), why not go from node's `http` to `fetch` API directly? Node has native stream support, browserify build targets (browsers) don't, so underneath they are going to be vastly different anyway.

IMHO, it's safer to be aware of javascript runtime's strength and weakness, than to assume they are a unified platform under a singular spec.

Hence `node-fetch`, minimal code for a `window.fetch` compatible API.


# Features

- Stay consistent with `window.fetch` API.
- Make conscious trade-off when following [whatwg fetch spec](https://fetch.spec.whatwg.org/) and [stream spec](https://streams.spec.whatwg.org/) implementation details, document known difference.
- Use native promise, but allow substituting it with [insert your favorite promise library].


# Difference to client-side fetch

- This module is WIP, see [Known limits](https://github.com/bitinn/node-fetch/blob/master/LIMITS.md) for details.

(If you spot a missing feature that `window.fetch` offers, feel free to open an issue. Pull requests are welcomed too!)


# Install

`npm install node-fetch --save`


# Usage

TODO


# License

MIT


# Acknowledgement

Thanks to [github/fetch](https://github.com/github/fetch) for providing a solid implementation reference.


[npm-image]: https://img.shields.io/npm/v/node-fetch.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/node-fetch
[travis-image]: https://img.shields.io/travis/bitinn/node-fetch.svg?style=flat-square
[travis-url]: https://travis-ci.org/bitinn/node-fetch
