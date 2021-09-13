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

## `.match()`

The `match()` function works opposite to `test()`.

```js
'string'.match(/regex/);
/regex/.test('string');
```

Using the `match()` function, returns when a "match" is found.

```js
let strRegex = /some/;
let str = "This is some str";
str.match(strRegex);
// Returns ["str"]
```

To find multiple "matches" instead of one, use the `g` flag.

```js
let repeatRegex = /again/g;
let str = "again and again and again";
str.match(repeatRegex);
// Returns ["again", "again", "again"]
```

## Wildcard

Using the wildcard operators allows you to match for 0 or any number of characters.

```js
let myRegex = /ha./;
// This regex would match with hat, ham, had
```

## Character Classes

To match a class of characters at a particular position, you could use character classes.

```js
let bgRegex = /b[aiu]g/; 
let bigStr = "big";         // Matches the regex
let bagStr = "bag";         // Matches the regex
let bugStr = "bug";         // Matches the regex
let bogStr = "bog";         // Doesn't match the regex
```

To include a range of characters, you could use the `-` character.

```js
let bgRegex = /b[a-d]s/;
```

You could also include numbers.

```js
let bgRegex = /b[a-z0-9]i/;
```

You could also create a negated chracter set, where only the characters that are *not* part of the set are matched.

```js
let bgRegex = /b[^aeiou]/gi;
// Only the characters which are not a vowel (including symbols) will be matched
```

