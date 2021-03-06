# Remove Symbol Description [![Build Status](https://travis-ci.org/kentor/babel-plugin-remove-symbol-description.svg)](https://travis-ci.org/kentor/babel-plugin-remove-symbol-description)

A [Babel][b] plugin to remove [Symbol][s] descriptions.

## What?

In:

```js
Symbol('some description');

var someIdentifier = 'some description';
Symbol(someIdentifier);
```

Out:

```js
Symbol();

var someIdentifier = 'some description';
Symbol();
```

## Why?

Symbol descriptions are useful in development for debugging, but they can safely
be removed in production to save bytes.

## Installation

```
npm install -D babel-plugin-remove-symbol-description
```

[b]: http://babeljs.io/
[s]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol
