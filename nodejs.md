# Node.js JavaScript Guidelines

## Three Golden Rules

1. Comment and document liberally
2. Write test cases first
3. Prefer pure functions

## General Guidelines

### Resources

* Use [Mocha](http://visionmedia.github.io/mocha/) for testing
* Use [JSDoc](http://usejsdoc.org/) for documentation
* Prefer using [libraries](https://www.npmjs.org/) over writing code
* Read [JavaScript: The Good
  Parts](http://books.google.com/books/about/JavaScript_The_Good_Parts.html?id=PXa2bby0oQ0C)

### Style

* *Avoid global states*. States in modules and closures are fine (and
  often necessary).
* *Prefer pure functions*. Corollary to avoiding global states. Functions which
  produce effect as output (e.g. `Math.random`) are fine, just not side-effects
  (e.g. `this.a = 1`).
* *Avoid prototypes*. Corollary to preferring pure functions.
* *Prefer module pattern*. Corollary to avoiding prototypes. The module pattern
  is superior to the prototype/object patterns because states are enclosed
  lexically via closure rather than dynamically.
* *Prefer simple modules*. Corollary to preferring using module patterns. When
  you have a module that creates sub-modules inside it, it may be a sign of
  troubles to come.