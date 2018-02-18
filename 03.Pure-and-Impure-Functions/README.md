Pure and Impure Functions
=============

[Section 3](https://egghead.io/lessons/javascript-redux-pure-and-impure-functions?series=getting-started-with-redux)

This article describes the difference between [pure function](https://en.wikipedia.org/wiki/Pure_function) and impure function.

```js
// Pure functions
// - The return value depends on the parameter
// - The same parameter will always pass back the same return value
// - No Observable side effect, such as IO, Database access
// - does not modify the incoming parameter value
function square(x) {
  return x * x;
}
function squareAll(items) {
  return items.map(square);
}

// Impure functions
function square(x) {
  updateXInDatabase(x); // call Database
  return x * x;
}
function squareAll(items) {
  for (let i = 0; i < items.length; i++) {
    items[i] = square(items[i]);  // modify input parameter
  }
}
```
