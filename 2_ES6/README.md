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

## Rest Parameter

With rest parameter, you can create functions that take a variable number of arguments.

```js
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2));
```

The rest parameter eliminates the need to check the args array and allows us to apply `map()`, `filter()` and `reduce()` on the parameters array.

```js
const sum = (...args) => {
  return args.reduce((a, b) => a + b, 0);
}
```

## Spread Operator

The spread operator allows you to unpack an array.

```js
const arr = [3, 5, 2, 4];
const max = Math.max(...arr);
```

**NOTE:** The spread operator only works in-place, like in an argument to a function or an array literal.

```js
const arr1 = [2, 45, 4, 3];

const a = ...arr1;
// ERROR

const arr2 = [...arr1];
// arr2 will have contents of arr1
```

## Destructuring Assignment

Destructuring assignment is special syntax introduced in ES6, for neatly assigning values taken directly from an object.

- *ES5*:
```js
const book = { name: "Atomic Habits", pages: 250 };

const name = book.name;
const pages = book.pages;
```

- *ES6*:
```js
const { name, pages } = book;
```

To give a different variable name, use:
```js
const { name: bookName, pages: bookPages } = book;
```

> `book.name` stored in the variable `bookName` and `book.pages` stored in `bookPages`

You could also use destructing assginment for nested objects:

```js
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

const { today: { low: lowToday, high: highToday } } = LOCAL_FORECAST;
```

> `low` value of `today` will be assigned to the variable `lowToday`
> `high` value of `today` will be assigned to the variable `highToday`

You could destructure arrays!

```js
const [a, b,,c] = [1, 2, 3, 4, 5];
// a = 1
// b = 2
// c = 4
```

