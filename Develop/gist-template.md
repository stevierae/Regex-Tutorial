# Fundamentals of Regex Tutorial

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The above line of code is a regex that validates whether or not input is an email address. This code will be broken down by individual regex items in order to explain what it does.

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

### Anchors (#anchors)
An anchor is a piece of text which marks the beginning and/or the end.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

In our example the "^" defines the beginning of the string and the "$" defines the end of the string.

- ### Quantifiers (#quantifiers)

A quantifier specifies how many instances of a character, group, or character class must be present in the input for a match to be found. Quantifiers can be considered either lazy or greedy. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The plus + will match one or more of the preceding token. In this case it will attempt to match [a-z0-9_\.-]. {2,6} indicates two to six characters in the group [a-z\.].

- ### OR Operator (#or-operator)
The [] OR operator is used in this regex. For example, [a-z0-9_\.-] means any character a-z (case insensitive), any digit 0-9, _, ., or -. 

- ### Character Classes (#character-classes)
A character class will match one out of several characters. The order of the characters within the character class does not matter.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

A character set [ABC] will match any single character in the set. In the example [a-z0-9_\.-] will match any character within the square brackets. A range [A-Z] will match a character included between the two characters separated by the hyphen. In the example a-z will match any character between a and z. 0-9 will match any character between 0 and 9.

- ### Flags (#flags)
Flags will always follow the closing forward slash of an expression, and modifies its behavior of searching. A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way 

- ### Grouping and Capturing (#grouping-and-capturing)
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

In our example () parentheses are used to capture a group. The first set of () captures the username of the email address, the second set captures the domain name, and the final set captures the domain.

### Bracket Expressions
[] create a character or group range and represent a single character. In regards to the regex expression this tutorial is covering, the brackets are used to separate each character class. The character can be anything specified within the brackets.

Example: [a-z0-9_\.-] -> this character can be matched with any lowercase letters from a-z, and digit from 0-9, an underscore _, a period ., or a dash -.

### Greedy and Lazy Match
Quantifers can be either greedy or lazy. A greedy quantifer will attempt to match as many characters as possible as it goes backwards through the regex string. A lazy quantifier will attempt to match as few characters as possible as it goes back through the regex string.

### Boundaries
Boundary markers such as ^ and $ allow you to anchor the regex pattern to the beginning and end of the line (or string depending on which flags you use). This means that when you want to match a literal ^ or $ , you need to escape these special characters with a backslash.

### Back-references
Back-references are commands which refer to a previous part of the matched regular expression. They are generally specified with a backslash and a single digit.

### Look-ahead and Look-behind
Lookarounds will match a group of characters either before or after a pattern, but will allow for it to not be included as part of the result. Lookbehinds are specific for groups that are before the pattern, and lookaheads are for groups after the pattern.


## Author

Stefanie Fisher is a registered nurse enrolled in Penn's coding bootcamp who has a newfound passion for full stack web development. She currently resides in Philadelphia, PA but is always mentally on a tropical island. Please visit link(s) for more information:
