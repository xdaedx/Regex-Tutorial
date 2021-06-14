# Regex Validating Emails
For my regex tutorial, I decided to do regexs and emails!

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
Quantifiers indicate the amount of characters the regex will match.

The + quantifier will match 1 or more characters. The * quantifier will match 0 or more characters. The ? quantifier will match 0 or 1 characters. The {n} quantifier will match n characters. The {a,b} quantifier will match an expression that is at least a characters, but no more than b characters.

The quantifier often follows a character class or bracket expression that defines what characters the regex will match.

### OR Operator
This will match the expression before or after the | and can operate within a group or as a whole. The patterns will be tested in order just as java will match either set of characters.

### Character Classes
The character class in regex below is the \d within the second set of braces.

The \d character class matches a single digit. The \w character class matches a single alphanumeric character or underscore. The \s character class matches a single white space such as a space or tab.

Capitalizing the letter will negate the character class, so case is important when using these in your regex. 

### Flags
Flags in regex are used for more advanced searching. This allows the expression to be on multiple lines without breaking the code.

### Grouping and Capturing
Paranteses are used for grouping in the regex. Grouping is used to seperate meta characters from literal characters; grouping and capturing can also be used to isolate part of a string to back reference or replace a part of the string.

### Bracket Expressions
Bracket expressions are used to define what caracters will be matched with the regex, as explained in the very beginning where the brackets around the A-Z for upper case letters and numbers 0-9.

### Boundaries
Boundaries here is in email validation since the '@' symbol will already act as a boundary for a given email address and name, domain, extension - but will not really need boundaries elsewhere. 

### Back-references
Back refrences isn't truly needed since this is alike to an HTML refrence/element to the text between tags in the HTML.

### Refrences
Regular Expressions: https://www.regular-expressions.info/email.html

Email Diagram: https://emailregex.com/wp-content/uploads/sites/2/2014/06/General-Email-Regex-Railroad-Diagram-emailregex.com_.png

Validation Emails: https://mkyong.com/regular-expressions/how-to-validate-email-address-with-regular-expression/

## Author
Hi hope you enjoyed the tutorial and have a good understanding, you can continue to find me here: https://github.com/xdaedx