# lexicmp

The lexicmp library enables comparing and sorting strings using lexicographical and natural sorting semantics. This means that any Unicode characters such as `á` or `ß` are treated like their closest ASCII character: `á` is treated as `a`, `ß` is treated as `ss`. This library also ensures that emojis are transliterated before being sorted. When using natural sorting, numbers are sorted naturally, ensuring that `50` is sorted before `100`, skipping characters that aren't alphanumeric, ensuring that `f-5` is next to `f5`. If different strings have the same ASCII representation (e.g. `"Foo"` and `"fóò"`), it falls back to the default method from the standard library, ensuring that sorting is always deterministic, and constitute a [total order](https://en.wikipedia.org/wiki/Total_order).

[![](https://img.shields.io/badge/status-stable-ff00bb.svg?style=flat-square)](https://github.com/surrealdb/lexicmp) [![docs.rs](https://img.shields.io/docsrs/lexicmp?style=flat-square)](https://docs.rs/lexicmp/) [![Crates.io](https://img.shields.io/crates/v/lexicmp?style=flat-square)](https://crates.io/crates/lexicmp) [![](https://img.shields.io/badge/license-MIT-00bfff.svg?style=flat-square)](https://github.com/surrealdb/lexicmp) 

#### Features

- Compare strings lexicographically
- Compare strings naturally with support for numbers
- Compare strings sensitively and case insensitively
- Compare strings, skipping non-alphanumeric characters
- Compare strings lexicographically and naturally together
- Handle unicode characters, foreign languages, and emoji characters
- Does not allocate memory on the heap, instead using iterators

#### Original

This code is forked originally from [lexical-sort](https://crates.io/crates/lexical-sort), licensed under the [Apache 2.0](https://choosealicense.com/licenses/apache-2.0/) and [MIT](https://choosealicense.com/licenses/mit/) licenses.