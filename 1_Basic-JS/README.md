# Basic JavaScript

## Comments

```js
// in-line comment (single-line)
```

```js
/* Multi -
Line Comment */
```

## Variables

There are 8 different data types in JavaScript:
- `undefined`
- `null`
- `boolean`
- `string`
- `symbol`
- `bigint`
- `number`
- `object`

To declare a variable, use the keyword `var`:
```js
var myVariable;
myVariable = 89;
var anotherVar = 1;
anotherVar = myVariable;
```

**NOTE:** 
- Variable names can consist of numbers, letters, and `$` or `_`
- JavaScript variables have an initial value of `undefined`
- All variables and function names are case-sensitive
- Use *camelCase* for best practice

### Increment/decrement a number

```js
i++;
i = i + 1;
i += 1;
```

### Escape Literal Quote

```js
var myString = "Then Voldemort told, \"Avada kedavera!\"";
```

**NOTE:** Strings could be made with single quotes as well.

### Escape sequence

- `\'` - single quote
- `\"` - double quote
- `\\` - backslash
- `\n` - newline
- `\r` - carriage return
- `\t` - tab
- `\b` - word boundary
- `\f` - form feed

### String concatenation

```js
var myName = "Thanos";
myName += " Stark";
```

### String Length

```js
var myStr = "Hi Bro";
console.log(myStr.length);
```

**NOTE:** Strings in JavaScript are *immutable*. i.e., individual characters of a string cannot be changed.

```js
var str = "Hi";
str[0] = "B"; // Not valid
str = "Bye";  // Valid
```

## Arrays

Store serveal pieces of data in one place.

```js
var operatingSystems = ["MacOS", "Windows", "Linux", 1, 2];
```

You can also nest arrays within arrays.

```js
var matrix = [[1,"Slack"], [2, "Discord"]];
```

### `push()`

`push()` function lets you append data to the end of an array.

```js
var arr = [1, 2];
arr.push(["What?", "Why?"]);
// arr = [1, 2, ["What?", Why?"]]
```
### `pop()`

`pop()` function is used to pop a value off of the end of an array.

```js
var arr = [1, 45, 90];
var data = arr.pop();
// data = 90
// arr = [1, 45]
```

### `shift()`

`shift()` function works just like `pop()`, except that it removes the first element instead if the last.

```js
var arr = ["Joey", "Ross"];
var data = arr.shift();
// data = "Joey"
// arr = ["Ross"]
```

### `unshift()`

`unshift()` works just like `push()`, but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.


```js
var lst = ["KFC", "Mcd", "Starbucks"];
var.unshift(["Popeyes"]);
// lst = ["Popeyes", "KFC", "Mcd", "Starbucks"]
```

## Functions

We can break down our code into reusable parts called as Fucntions.

```js
function reusableFunction() {
  console.log("Hi World");
}
reusableFunction();
```

### Parameters

Paramteres are variables that are sent as *inputs* to a function, when it is called.

```js
function functionWithArgs(a, b) {
  console.log(a + b);
}
functionWithArgs("Wingardium", " Leviosa");
```

## Conditional Logic

### If Statements

In a programming language, it is essential to make decisions, based on some given conditional. Thankfully, `If` statements does just that! 

```js
function condtionalStat (condition) {
    if (cond) {
        return "Condition was true!";
    }
    return "Condition was false!";
}
```

#### Equality Operator

Using the equality operator, you could check if two values are the same.

```js
1 == 1
// true

2 == 3
// false

"3" == 3
// true
```

- Equality operator changes the type of data, if the values being checked deosn't have the same data type.

#### Strict Equality Operator

To avoid the changing the type of data (*as compared to the last example*), strict equality operator could be used.

```js
"345" === 345
// false

345 === 345
// true
```

#### Inequality Operator

Similarly like Equality operator, Inequality operator checks if the two given are **not** equal.

```js
12 != 13
// true

123 != 123
// false

"10" != 10
// false
```

- Inequality operator changes the type of data, if the values being checked deosn't have the same data type.

#### Strict Inequality Operator

Similarly like Strict Equality Operator, it doesn't change the type of data while checking the values.

```js
90 !== "90"
// true

90 !== 90
// false
```

### Switch Statements

If you have many options to choose from, use a switch statement. A switch statement tests a value and can have many case statements which define various possible values. 

```js
switch(myVar) {
  case "a":
    console.log("a");
    break;
  case "b":
    console.log("b");
    break;
  default:
    console.log("Invalid!");
    break;
}
```

## Objects

Objects are similar to `arrays`, except that instead of using indexes to access and modify their data, you access the data in objects through what are called `properties`.

```js
var book = {
  "name": "Atomic Habits",
  author: "James Clear",
  "pages": 226
};
```

- Yep, `JSON`!
### Accessing Object Properties

The `object` properties could be accessed by using the `.` notation or the `[ ]` notation.

```js
var anObj = {
  p1: "val1";
  p2: "val2";
};

// Dot notation
var p1Val = anObj.p1;
var p2Val = anObj.p2;

// Bracket notation
var p1ValB = anObj["p1"];
var p2ValB = anObj["p2"];
```

### Modifying Object Properties

The object properties could be modified by using the dot or the bracket notation.

```js
var obj = {
  "prop1": 12,
  "prop2": "value"
};

obj.prop1 = 54;
obj.prop2 =  "other value";
```

### Add New Properties

You can add new properties to existing JavaScript objects the same way you would modify them.

```js
var obj = {
  "prop1": 12,
  "prop2": "value"
};

obj.prop3 = true;
obj["prop4"] = 1.29;
```

### Delete Properties

We can delete object properties using the `delete` keyword.

```js
var obj = {
  "prop1": 12,
  "prop2": "value",
  "prop3": true,
  "prop4": 1.29
};

delete obj.prop4;
delete obj["prop3"];
```

### Lookup!

Objects can be thought of as a key/value storage, like a dictionary.

```js
var lookup = {
  alpha: "Adams",
  bravo: "Boston",
  charlie: "Chicago",
  delta: "Denver",
  echo: "Easy",
  foxtrot: "Frank"
}

console.log(lookup[alpha]);
// Adams
```

### Testing Objects

`.hasOwnProperty(pname)` could be used to check if an object has any given property.

```js
var obj = {
  "prop1": 12,
  "prop2": "value",
  "prop3": true,
  "prop4": 1.29
};

obj.hasOwnProperty("prop1");
// true

obj.hasOwnProperty("something");
// false
```

## Loops!

### While Loop

`while` loop keeps running while a specified condition is true, and stops once that conditions is no longer true.

```js
var i = 0;
while (i < 5){
  console.log(i);
  i++;
}
// 0
// 1
// 2
// 3
// 4
```

### For Loop

```js
for (var i = 0; i < 3; i++) {
  console.log(i);
}
// 0
// 1
// 2
```

