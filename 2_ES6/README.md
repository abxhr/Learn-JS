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

- Arrays and functions assigned to a variable using a `const` are still mutable. Using the `const` declaration only prevents reassignment of the variable identifier.

```js
const arr = [10, 20, 30];
arr = [40, 50, 60];
// ERROR

arr[0] = 1;
console.log(arr);
// arr = [1, 20, 30]
```

## `Object.freeze()`

To ensure your data doesn't change, you could use the function `Object.freeze()` to prevent data mutation.

Once frozen, you won't be able to add, update or delete properties of that object.

```js
const myObj = {
    a: 10;
    b: 20;
};
Object.freeze(myObj);
myObj.b = 324;
// ERROR;
```

## Arrow Functions

In JavaScript, we often don't need to name our functions, especially when passing a function as an argument to another function. Instead, we create inline functions.

```js
const myValue = function() {
    const var = "value";
    return var;
}
```

In **ES6**, you can write anonymous functions using the arrow function syntax.

```js
const myValue = () => {
    const var = "value";
    return var;
}
```

- You can also pass arguments to an arrow function.

```js
const square = (number) => number * number;
square(2);
```

- You can use default paramters too!

```js
const sayHi = (name = "Human") => "Hello, " + name;

console.log(sayHi());
// Hello, Human
```

