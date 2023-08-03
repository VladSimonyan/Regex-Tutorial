# Regex Tutorial
Regular Expressions, commonly known as Regex, are powerful tools for pattern matching and text manipulation. They allow you to search for, match, and manipulate strings based on specific patterns. In this tutorial, we will cover the basics of using Regex in JavaScript. In this tutorial you will be walked through the differnnet ways to use Regex and will be given examples and will be provided information on what all the components do.

# Summary

In JavaScript, you can create a regular expression using the 'RegExp' object or by using a regex literal with slashes ('/').

Using 'RegExp' object:

const regexObj = new RegExp('pattern');

Using regex literal:

const regexLiteral = /pattern/;

Regular expressions are composed of characters and metacharacters that form patterns. For example, the pattern '/hello/' will match the string "hello". To test if a string matches a pattern, use the 'test()' method.

const pattern = /hello/;
const str = "hello world";

if (pattern.test(str)) {
  console.log("Pattern matched!");
} else {
  console.log("Pattern not found.");
}

Metacharacters and Quantifiers:

'.' - Matches any single character except a newline.

'*' - Matches zero or more occurrences of the preceding character.

'+' - Matches one or more occurrences of the preceding character.

'?' - Matches zero or one occurrence of the preceding character.

'{n}' - Matches exactly 'n' occurrences of the preceding character.

'{n,}' - Matches 'n' or more occurrences of the preceding character.

'{n,m}' - Matches between 'n' and 'm' occurrences of the preceding character.

const pattern = /a.c/;

console.log(pattern.test("abc")); // true

console.log(pattern.test("ac")); // false

const quantityPattern = /go{2,4}gle/;

console.log(quantityPattern.test("gooogle")); // true

console.log(quantityPattern.test("google")); // false

Character classes allow you to match a set of characters within square brackets '[ ]'.

'[abc]' - Matches either 'a', 'b', or 'c'.

'[a-z]' - Matches any lowercase letter.

'[^0-9]' - Matches any character except digits.

'\d' - Matches any digit (equivalent to [0-9]).

'\w' - Matches any word character (letters, digits, or underscore).

'\s' - Matches any whitespace character.

const pattern = /[aeiou]/;

console.log(pattern.test("hello")); // true

const digitPattern = /\d{3}/;

console.log(digitPattern.test("123")); // true

Anchors and Boundaries help math patterns at specific positions in the string.

'^' - Matches the start of a string.

'$' - Matches the end of a string.

'\b' - Matches a word boundary.

const pattern = /^hello/;

console.log(pattern.test("hello world")); // true

console.log(pattern.test("world hello")); // false

const endPattern = /world$/;

console.log(endPattern.test("hello world")); // true

console.log(endPattern.test("world hello")); // false

Grouping and Alternation:

Parentheses '()' are used for grouping, and the pipe '|' represents alternation (OR).

const pattern = /(apple|banana)/;

console.log(pattern.test("I love apples")); // true

console.log(pattern.test("I prefer oranges")); // false

Flags modify the behavior of regular expressions. Commonly used flags are:

'i': Case-insensitive matching.

'g': Global matching (find all occurrences).

'm': Multiline matching.

const pattern = /apple/gi;

const str = "An apple a day keeps the doctor away. Apple is a fruit.";

console.log(str.match(pattern)); // ['apple', 'Apple']

Regular expressions are powerful tools for pattern matching and text manipulation in JavaScript. Understanding the basic syntax and metacharacters will allow you to write complex patterns for various use cases, such as form validation, string manipulation, and data extraction. Practice and experimentation will further enhance your regex skills.

# Table of Contents

Anchors

Quantifiers

OR Operator

Character Classes

Flags

Grouping and Capturing

Bracket Expressions

Greedy and Lazy Match

Boundaries

Back-references

Look-ahead and Look-behind

Regex Components

Anchors

Quantifiers

OR Operator

Character Classes

Flags

Grouping and Capturing

Bracket Expressions

Greedy and Lazy Match

Boundaries

Back-references

Look-ahead and Look-behind

# Author

Vlad is a student attending UCI Irvine Bootcamp. He has passion to keep trying to he succeeds and learn new things as he goes. The coding world has been a rollercoaster for him but hes taking it step by step and learning new ways to code his way to success. Although he enjoys the coding world he also has a passion for sports and gaming. He wants to take all that he is learning in the coding world and implement it into the sports and gaming world. He has many ideas that can have a postitive affect in both the gaming and sports world.

https://github.com/VladSimonyan
