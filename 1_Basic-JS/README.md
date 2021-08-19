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

