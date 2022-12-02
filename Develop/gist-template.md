# Matching an Email Using Regex Tutorial

In this tutorial I will be demonstrating how Regex is used to determine if a portion of a text is an email.

## Summary

Regular expression or regex is an expression that uses different characters to specify a pattern so that it can be used as a search parameter. In this particular case we will be displaying the regex that helps in identifying an email address, for which the expression is: 
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

There are two anchors used in regex, them being ^ and $.

The ^ is signifying that the following character or group of characters must be at the beggining of the string, and the $ is signifying that the preceding character or group of characters is at the end of a string.

In this case the ^ is used to signify that the email must start with any characters within [a-z0-9_.-] and the email should end in something of the form [a-z.]{2,6}

### Quantifiers

Quantifiers are used to determine how many characters are to be expected. 

In this particular regex we are using two different quantifiers, + and {2,6}.

The + is signifying that there must be at least one instance of that character or group of characters, so in this case it is making sure that the email doesnt have a blank beggining

The {2,6} or generally speaking {n,m} for any numbers n and m is signifying that there is at least n characters matching and no more than m characters that match. More specifically in this case the end of the email should be in between 2 and 6 characters.

### OR Operator



### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
