# Email Matching Regex Tutorial 

Regular expressions (shortened regex) are strings of characters used to find other strings that matches the criteria in the expression.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

The regex I'll be explaining is to match an email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

I'll describe the parts of this regular expression, what they do, and how they work with eachother to match a valid email.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Author](#author)

## Regex Components
    This regular expression includes anchors, quantifiers, character classes, groups and bracket expressions.

### Anchors
    Anchors ensure that the matched expression is at a certain position in the string. The anchors in this expression are ^ (to matching the beginning of a string) and $ (that matches the end of a string). The anchors are on either end of the regex to ensure that the matched expression is both the beginning and the end of the string.

### Quantifiers
    Quantifiers specify how many of the character or expression. The quantifiers used in this expression are + (for 1 or more characters) and {min, max} (to specify range of characters). The + quantifier is placed after the first 2 character sets to only allow 1 or more characters for the initail email string and the website. The {min, max} quantifier is put at the end to only allow 2-6 charcters (for the domain).

### Character Classes
    Character classes (defined by []) allow you to define a the set of characters allowed, by putting the allowed characters in square brackets. This expression use of character classes in the beginning ([a-z0-9_\.-]) to allow any character a-z, any digit 0-9, underscores, periods, and heiphens. The second use of character classes ([\da-z\.-]) is essentailly the same (because /d means any digit 0-9) but this one doesn't allow underscores. The last use of character classes ([a-z\.]) only allows character a-z and periods. 

### Grouping and Capturing
    Regex groups (defined by parentheses) isolate parts of an expression. In this expression it is used inbetween the necessary parts of the email (like the @ and period in the website) to isolate the parameters for each section.

### Bracket Expressions
    The bracket expressions used are the character classes, quantifiers, and the groups ([]s, {}s, and ()s)

### Greedy and Lazy Match
    Greedy quantifiers match the largest string possible and lazy quantifiers match the shortest string. By defualt a quantifier is greedy but can be made lazy by adding a ?.

## Author

Cody Cooper (Konopie) is an aspiring software developer currently in a coding bootcamp
GitHub: Konopie
Email: codycooper06@gmail.com