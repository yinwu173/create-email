# Regular Expression (Regex) - Matching an Email

For this gist, we are going to learn how to utilize a regular expression (regex) for validating email addresses. 

## Summary

To briefly summarize the Match an Email Regex, it is a sequence of characters that is primarily used to match specific patterns in email addresses. In this gist, we will be breaking down and analyzing the various components of a email regex. The following expression is employed to match an email address: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors

There are two types of anchors in the Match an Email regex. The first anchor being `^`. This anchor demonstrates the start of our email string. In other words, our email address input has to match the starting character of our regex.

The second achor would be `$`. This anchor highlights the end of our string. What this means is the pattern our our email address input must finish matching to the last character of our string. Let use the following email address as an example: `john@gmail.com hello`. This example would not work because it does not match our regex pattern.

### Quantifiers

The `+` and `{2,6}` are the quantifiers in this regex. The `+` will link the name part of the email to the domain portion of the email. For example, `([a-z0-9_\.-]+)` defines the name / characters prior to the domain.com and `([\da-z\.-]+)` defines the email service.

The `{2,6}` quantifier specifies the occurence of the character. In the case for `([a-z\.]{2,6})`, it must match between at least 2 and at most 6 times.


### Character Classes

The first character class in the Match an Email regex is `[a-z0-9_\.-]`. This character class matches any single character that is an lowercase letter (a to z), digit (0 to 9), underscore, period, along with hyphen.

For `[\da-z\.-]`, it would match an email address to a digit (0 to 9), lowercase letter (a to z), period, and hyphen. 

Finally, `[a-z\.]` corresponds to a lowercase letter (a to z) and a period. 

### Grouping and Capturing

There are three capturing groups in this regex.
Capturing Group 1 `[a-z0-9_\.-]`: represents the local part (i.e. characters prior to the `a`)
Capturing Group 2 `[\da-z\.-]`: domain of the email (i.e. gmail.com)
Capturing Group 3 `[a-z\.]`: (i.e. .com)

### Bracket Expressions

There are three brackets in the Email regex. The first bracket `[a-z0-9_\.-]` is used to match characters prior to the `@`. The `[\da-z\.-]` is to match the domain and `[a-z\.]` is used to match those after the period (.).

### Greedy and Lazy Match

The following regex only contains a Greedy Match. It is greedy because it utilizes the `+` quantifier. The `+` will try to match as many times as possible from the email address string.

### Boundaries

`^` and `$` represents the starting and ending of the string and serves as boundaries. These boundaries forces the string to match the pattern. If they don't match then the regex would not work. 

## Author

Link to my github profile: https://github.com/yinwu173
