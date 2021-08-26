# ES6

## `var` and `let`

`var` and `let` are both used for variable declaration in javascript but the difference between them is that `var` is function scoped and `let` is block scoped.
It can be said that a variable declared with `var` is defined throughout the program as compared to `let`.

```js
var myVariable;
let myVar;
```

When you declare a variable with the `var` keyword, it is declared globally, or locally if declared inside a function.

The `let` keyword behaves similarly, but with some extra features. When you declare a variable with the `let` keyword inside a block, statement, or expression, its scope is limited to that block, statement, or expression.

## `const` Keyword

The keyword `let` is not the only new way to declare variables. In ES6, you can also declare variables using the `const` keyword.

**NOTE**: They are read only variables, with the features that `let` has.

```js
const BEST_BRO = "Habibi";
BEST_BRO = "Habibti";
// ERROR
```
