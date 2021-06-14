# Regex 
For my regex tutorial, I decided to dp regexs and emails!

## Summary

Regex, or regular expression, allows you to create search patterns that will help match, locate, and manage text. In here, we will be going over how regex is used for helping in matching emails.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Back-references](#back-references)

## Regex Components
Email regex example: \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b
Now let's anaylize each part of the components.

- [A-Z0-9._%+-]+ (Name: this beginning section verfies each character will be upper or lower case, comparerable to "a-zA-Z" but here is upper case, then it's numbers 0-9, or then a special character.)

- @[A-Z0-9.-]+ (Domain: this piece is the same as the one but applies for validating the domain name for the email address.)

- [A-Z]{2,} (Extension: here is validating the email address extension, like ".com" or ".org". The email is able to end with 2 characters, example like ".co" address. But the minimum two characters is usually for the different country codes like .ca = Canada, .us = USA, .de = Germany)

### Anchors
The anchors included with an email vlaidation regex are the ^ and the $ in this example:

/^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/

The ^ signifies the regex will match with the code group in the first set of parantheses that the caret precedes meaning the information provided before the @ symbol appears in the rest of the code string preventing a user from simply submitting an '@(DOMAIN).com email address without the first required part of the email address, the NAME section.

The $ symbol signifies the string regex will match ends with the DOMAIN the dollar sign follows.

Examples:

Not matched: @yahoo.com; there is no NAME.

Not matched: sunisa@email.c; the extension is less than two letters, the minimum required for the extension.

Matched: dogs@email.co.uk; this email address has a name, domain name, extnesion, and an acceptable country code extension.

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references
Regular Expressions: https://www.regular-expressions.info/email.html


### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)