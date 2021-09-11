# Regular Expressions

Regular expressions are used in programming languages to match parts of strings. You create patterns to help you do that matching.

## `.test()`

There are multiple ways to use regexes in JavaScript. One of them is using the `.test()` method.

```js
let str1 = "Amazon Kindle";
let str2 = "Amazon kindle";
let regex = /Kindle/;
regex.test(str1);
// Returns true
regex.test(str2);
// Return false
```

As `str1` and `str2` has different cases, they give different results. You could also create a regex to ignore cases, using the `i` flag.

```js
let regex2 = /Kindle/i;
regex2.test(str2);
// returns true
```

## `|` Operator

You could search for multiple patterns using the `alternation` or `|` operator.

```js
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/; 
let result = petRegex.test(petString);
// returns true
```

