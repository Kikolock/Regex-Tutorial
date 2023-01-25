### Title (replace with your title)

This gist is a tutorial for a regex expression that matches a valid URL address.

### Summary
This tutorial will cover a step by step deconstruction of a regex that matches a valid URL address.

The regex expression we will be decoding is  ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$

### Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Final Test](#final-test)
- [Author](#author)

### Regex Components

### Anchors
Anchors match a position before or after characters.

- `^` - The caret anchor matches the beginning of the text. 
- `$` - The dollar anchor matches the end of the text.

In our example `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we have one anchor `^`  meaning where to start a matching pattern.

### Quantifiers
In our example `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we specify how many instances of a character, group, or character class must be present in the string matched.

In the case of `https?` : `https?` 

We will match zero or one string as dictated by the `?` sign after `https`, meaning that the URL can either start with "http" or "https".

In the case of `([\da-z\.-]+)` : `([\da-z\.-]+)` 

We will match one or more instances of the characters in the square brackets `[]`. This group matches the subdomain, domain name and top-level domain of the URL.

In the case of `([\/\w \.-]*)*` : `([\/\w \.-]*)*` 

We will match zero or more instances of the characters in the square brackets `[]` as dictated by the `*` sign after the group. This group matches the path and any query parameters in the URL.

In the case of `\/?$` : `\/?$`

The `\/?` matches an optional forward slash at the end of the URL, and the `$` anchor matches the end of the text.

### Character Classes
In our example `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we have [] square brackets, these are used to match different types of characters in order to match what you are looking for.

- `\da-z\.-]` in `([\da-z\.-]+)` matches digits, lowercase letters, period and hyphen.
- `\/\w \.-` in `([\/\w \.-]*)*` matches forward slash, word characters, space, period and hyphen.

### The OR Operator
In our example, we don't have any OR operator to match the pattern.

### Flags
In our example, we don't have any flags to match the pattern.

### Character Escapes
In our example, we use some escape characters to match the pattern:

- `\/` in `https?:\/\/` and `([\/\w \.-]*)*\/?` matches the forward slash.
- `.` in `([\da-z\.-]+)` and `([a-z\.]{2,6})` is used as an escape character to match the period character itself.

### Final test
![My Remote Image](https://github.com/Kikolock/Regex-Tutorial/blob/main/test%20done.JPG)

### Author
* <a href = "https://github.com/Kikolock"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a>
* <a href = "mailto:icaro12@hotmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>