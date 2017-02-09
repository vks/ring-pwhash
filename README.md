# ring-pwhash [![Latest Version][crate-image]][crate-link] [![Build Status][build-image]][build-link] [![Apache 2 licensed][license-image]][license-link]

[crate-image]: https://img.shields.io/crates/v/ring-pwhash.svg
[crate-link]: https://crates.io/crates/ring-pwhash
[build-image]: https://travis-ci.org/cryptosphere/ring-pwhash.svg?branch=master
[build-link]: https://travis-ci.org/cryptosphere/ring-pwhash
[license-image]: https://img.shields.io/badge/license-MIT-blue.svg
[license-link]: https://github.com/cryptosphere/ring-pwhash/blob/master/LICENSE

A collection of password hashing functions, using [*ring*][ring] cryptographic primitives

## Why?

The [*ring*][ring] library for Rust provides many high-performance cryptographic primitives,
but does not implement any password hashing functions except PBKDF2.

This library implements password hashing algorithms based on [*ring*][ring]'s cryptographic
primitives, serving as a "companion library" for applications that want to leverage
[*ring*][ring] as their one-and-only cryptography library, and also providing high-performance
password hash implementations thanks to the speed of [*ring*][ring]'s core primitives.

## Supported Algorithms

* [**scrypt:**][scrypt] Colin Percival's Salsa20/8+PBKDF2-based password hashing function

No other algorithms are supported at this time, although it'd be great to add additional algorithms!
Argon2 and bcrypt are both good candidates. Pull Requests Accepted!

## License

ring-pwhash is a fork of [rust-crypto], and is dual licensed under the MIT and
Apache 2.0 licenses, the same licenses as rust-crypto.

[ring]: https://github.com/briansmith/ring
[scrypt]: https://www.rfc-editor.org/rfc/rfc7914.txt
[rust-crypto]: https://github.com/DaGenix/rust-crypto
