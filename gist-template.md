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
- [Resources](#resources)
- [Author](#author)

## Regex Components

Our regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has the following components:
- Anchors `^` `$`
- Grouping and Capturing `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, `([a-z\.]{2,6})`
- Bracket Expressions `[a-z]`, `[0-9]`, `[_\.-]`
- Quantifiers `+` `{}`
- Character Classes `([\da-z\.-]+)`

Because regex's are literal, the pattern needs to be wrapped with `/` characters.

### Anchors
Notice the characters `^` and `$` at the bookends of the regex:
- `^` - The caret anchor matches the beginning of the string.
- `$` - The dollar anchor matches the end of the string.

In our regex, the string must start and end with: `[a-z0-9_\.-]`

### Grouping and Capturing
We can group a regex by reating ***subexpressions***. To create ***subexpression*** you must use partentheses `()`. 

Our regex contains 3 subexpressions:

- `([a-z0-9_\.-]+)`
- `([\da-z\.-]+)`
- `([a-z\.]{2,6})`

Therefore, when a user inputs an email they can use any lowercase letter `a-z`, any number from `0-9`, and special characters `_`, `.`, or `-` and in any order they choose. The pattern does not need to include characters from all groups however, it must include at least one character group.

Below are some examples that meet this requirement:
- "michael"
- "michael-scarn44"
- "michael.scarn_007"

### Bracket Expressions
Bracket Expressions `[]` allow us to match any characters that are inside. In other words, they define the characters that we want included. These patterns are also known as, "positive character groups."

Our regex has 3 different groupings:
- `[a-z]` -- The string can contain any **lowercase** letter between `a - z`. 
- `[0-9]` -- the string can contain any number between `0 - 9`.
- `[_\.-]` -- the string can contain an underscore, period, or hyphen `_ . -` special characters.

### Quantifiers
Quantifiers set limits on the string, or individual parts of a string that matches your regex, including both the min. and max. number of characters that your regex requires.

Our regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has the following quantifiers:
- `{2, 6}`: requires the final bracket expression `[a-z\.]` must be between 2 and 6 characters and include lowercase characters `a-z` as well as the dot character `.`.
(Typically this is standardized as `.com` at the end of an email.)
- `{+}`: connects the email's 3 parts: `username + @email-provider + .com`

### Greedy and Lazy Match
Quantifiers are characterized as either "Greedy" or "Lazy".

- Greedy qualifiers match elements as many times as possible and can be changed to Lazy qualifiers by adding a `?`.
- Lazy qualifiers match elements as few times as possible.

Our regex uses Greedy quantifiers:
- `+`
- `{}`

### Character Classes
Character classes define a set of characters. 

Our regex has one character class:
- `\d` -- Equivalent to the bracket expression `[0-9]`

It can be found in the second subexpression of our regex: 

- `([\da-z\.-]+)`

Threfore for this section of the email, numbers (`0-9`), characters (`a-z`) and special characters, (`.-`) are valid inputs.

## Resources
[Chelsea Sexton](https://github.com/chelsea314)
[Andrada Gacichevici](https://gist.github.com/andradag)
[how to create a gist](https://help.github.com/en/github/writing-on-github/creating-gists)
[video on how to use gists](https://www.youtube.com/watch?v=wc2NlcWjQHw)
[Regex Tutorial: Matching a Username](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)

## Author

I am an aspiring Product Manager currently enrolled in The Coding Bootcamp at The University of Texas at Austin Center for Professional Education.

[Brian's Github](https://github.com/BrianLalli)
