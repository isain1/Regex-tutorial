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

The + is signifying that there must be at least one or more instance of that character or group of characters, so in this case it is making sure that the email doesnt have a blank beggining

The {2,6} or generally speaking {n,m} for any numbers n and m is signifying that there is at least n characters matching and no more than m characters that match. More specifically in this case the end of the email should be in between 2 and 6 characters.

### OR Operator

In regex the or operator " | " is used to say that either either the preceding expression or the following expression can be used as a search parameter. However, in the case of an email there is no need for an or operator. 

### Character Classes

In regex character classes are groups of characters enclosed in square brackets. They are used to describe what kind of character to expect.

Some examples of them include 
- [abc] which represents a, b, or c.
- [^abc] which represents the negation of the above class.(any character except a, b, or c).
- [a-z] which represents any character in between a and z.
- [0-9] which represents any number in between 1 and 9
- \d which represents digits.
- \D which represents not digits.
-\w which represents words.
-\W which represents not words.

In the expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ there is two character classes used. [a-z0-9_.-] and \d meaning that any character in betrween a-z and any number in between 1-9 alonmg with hyphens and dashes can be in the string.

### Flags

In Regex there are 6 "flags" that affect search criteris. They are i, g, m, s, u, and y.

- i removes case sensitivity meaning that letters like a and A are considered the same letter.
- g makes the search identyfy all matches. only the first match is identified without it.
- m is the multiline mode and it affects the behavior of $ and ^ through multiple lines when searching.
- s enables dotall mode in order to match newline character.
- u enables full unicode support, which allows for the correct processing of surrogate pairs.
- y enables sticky moode which searchjes at the exact position of the text.

There are noo flags in this regex.

### Grouping and Capturing

In regex grouping and capturing is the act of using parenthesis to group an expression so that quantifiers can be applied to what is inside of the parenthesis. In this expression it is used 3 times to signify that the first part can contain any letter, number, underscore, or hyphen followed by an @ symbol followed by more digits in between a-z followed by a period and followed by any 2 to 6 letters in between a-z. 

### Bracket Expressions

Bracket expressions are used in regex to indicate which set of characters whould match. In this example they are used three times inside of the parenthesis.

### Greedy and Lazy Match

In regex the difference between a greedy and lazy match is that the lazy maatch will more than likely be a shorter result. The reason for this is that the greedy match continues to search and gives the largest possible result, whereas the lasy match looks for the shortest possible match. A greedy match can bne turned into a lazy match by adding a ? to the end. This example uses neither of them.

### Boundaries

Boundaries are denoted byu \b and the purpose of it is to determine if one side of it is a word and the other side of it is not a word. There was no boundary in this expression.

### Back-references

Back references are used to identify the same text that has already been matched. There were back references in this expression.

### Look-ahead and Look-behind

Look ahead is used to determine when a patern matches if it is followed by another pattern, and look-behind does the opposite where it looks at patterns that precede it. There were no look-ahead or look-behind in this expression.

## Author

This Github Gist was created by Isain Ibarra. For more visit [my github](https://github.com/isain1)
