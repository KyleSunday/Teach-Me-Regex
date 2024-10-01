# Regex URL Tutorial

### A regex expression that will search for text resembling a website URL

## Summary

### In this tutorial we will breaking down a regex snippet into its identifying components and reviewing their concepts.
### The regex we will be using throughout this tutorial is /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/.
### This regex will search for a url in a page of text



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)




## Regex Components

#### Expression: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

### Anchors

- " ^ " capturing group that follows the anchor is the start of a string
- " $ " capturing group that precedes the anchor is the end of a string
#### Example:
##### " ^ " asserts the first capturing group (https?:\/\/) as the start of the string

### Quantifiers
- " + " capturing group or character that precedes "+" appears one or more times
- " * " capturing group or character that precedes "*" appears zero or more times
- " {2,6} " capturing group or character that precedes "{2,6}" appears 2-6 times

### OR Operator
- " [] " matches any character or meta-character within "[]", just has to match with one of the characters 

### Character Classes
- " \d " a meta-character that matches a single character that is a digit
- " \w " a meta-character that matches a single character that is a digit
#### Example:
##### " \d " in group [\da-z\\.-], the "\d" matches a digit (equivalent to [0-9]) 
##### " \w " in group [\/\w \\.-], the "\w" matches any word character (equivalent to [a-zA-Z0-9_])
### Grouping and Capturing
- " () " creates a capturing group from the character(s), meta-character(s), or expression withing the "()"
#### Example:
##### " () " that surrounds ([\da-z\\.-]+) forms a capturing group. A capturing group creates a string in which an operator, such as a quantifier, can act on the group of characters as a whole

### Grouping and Capturing
#### It matches the capturing groups "(https?:\/\/)", "([\da-z\\.-]+)", "\\.", "([a-z\\.]{2,6})", "([\/\w \\.-]*)", and "\/"
- "(https?:\/\/)" matches a string that resembles "https://"
- "([\da-z\\.-]+)" matches a string with a numerical digit, an alphabetical character, a period, or a dash
- "\." matches a period, for example the "dot" in ".com"
- "([a-z\\.]{2,6})" matches an alphabetical characters or a dot, for example the "com" in ".com"
- "([\/\w \\.-]*)" matches a dash, an alphabetical character, a period, or a dash, for example a parameter "/profile" that comes after ".com"
- "\/" matches a slash, for example a slash that closes a url
- " () " creates a capturing group from the character(s), meta-character(s), or expression withing the "()"
#### Example:
##### " () " that surrounds ([\da-z\\.-]+) forms a capturing group. A capturing group creates a string in which an operator, such as a quantifier, can act on the group of characters as a whole

### Bracket Expressions

### Greedy and Lazy Match
#### -  Greedy: expand as far as they can within the provided text
- " + "
- " * "
#### -  Lazy: terminates the search after the preceding capturing group
- " $ "


### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author
### Kyle Sunday
github link:https://github.com/KyleSunday

## References
- https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285
- https://regex101.com/r/cO8lqs/2
