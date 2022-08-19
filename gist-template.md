# Email Matching Using Regular Expression

A regex is a sequence of characters that defines a specific search pattern. Other use cases include: finding/replacing characters in a string and validating user input.

It's critically important in web development to validate user input. Below is a tutorial that explains how to use a regular expression, or "regex", to match and validate emails.

## Summary

The purpose of this tutorial is to break down the expression below and explain each component:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)

## Regex Components

This regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has the following components:
- Anchors ^ $
- Quantifiers + {}
- Captures and Groups ([a-z0-9_\.-]+)
- Bracket Expressions [ ]
- Character Classes [a-z\d] etc

Because regex's are literal, the pattern needs to be wrapped with `/` characters.

### Anchors
Notice the characters `^` and `$` at the bookends of the regex:
^ - The caret anchor matches the beginning of the string.
$ - The dollar anchor matches the end of the string.

In this regex, the string must start and end with: `[a-z0-9_\.-]`

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

I am an aspiring Product Manager currently enrolled in The Coding Bootcamp at The University of Texas at Austin Center for Professional Education.

[Brian's Github](https://github.com/BrianLalli)
