# Email Matching Using Regular Expression

A regex is a sequence of characters that defines a specific search pattern. Other use cases include: finding/replacing characters in a string and validating user input.

It's critically important in web development to validate user input. Below is a tutorial that explains how to use a regular expression, or "regex", to match and validate emails.

## Summary

The purpose of this tutorial is to break down the expression below and explain each component:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 


## Table of Contents

- [Regex Components](#regex-components)
- [Anchors](#anchors)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Character Classes](#character-classes)
- [Author](#author)

## Regex Components

Our regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has the following components:
- Anchors `^` `$`
- Quantifiers `+` `{}`
- Captures and Groups `([a-z0-9_\.-]+)`
- Bracket Expressions `[ ]`
- Character Classes `[a-z\d]`

Because regex's are literal, the pattern needs to be wrapped with `/` characters.

### Anchors
Notice the characters `^` and `$` at the bookends of the regex:
-`^` - The caret anchor matches the beginning of the string.
-`$` - The dollar anchor matches the end of the string.

In our regex, the string must start and end with: `[a-z0-9_\.-]`

### Grouping and Capturing

### Bracket Expressions

### Quantifiers
Quantifiers set limits on the string, or individual parts of a string that matches your regex, including both the min. and max. number of characters that your regex requires.

Our regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has the following quantifiers:
- `{2, 6}`: requires the final bracket expression `[a-z\.]` must be between 2 and 6 characters and include lowercase characters `a-z` as well as the dot character `.`.
-- typically this is standardized as `.com` at the end of an email.
- `{+}`: connects the email's 3 parts: `username + @email-provider + .com`

### Greedy and Lazy Match

### Character Classes

## Author

I am an aspiring Product Manager currently enrolled in The Coding Bootcamp at The University of Texas at Austin Center for Professional Education.

[Brian's Github](https://github.com/BrianLalli)
