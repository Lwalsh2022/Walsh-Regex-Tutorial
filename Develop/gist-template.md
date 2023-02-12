# REGEX TUTORIAL

Regular expressions, or "Regex", are a sequence of characters that define a search pattern. The are used to search and edit data. This tutorial explains the regex components using an email address as an example. 

## Summary

The regex for this tutorial is for an email address and is below:
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

A Regex always starts with the / character. In this example the @ symbol matches "@", because all special charcters match themselves. The components of the email address regex are anchors, quantifiers, bracket expressions, character classes, grouping, capturing, escape characters and greedy matches. 

### Anchors

^ and $ are the anchors. The ^ begins the string and signifies possible matches because of the brackets that follow it. The $ ends the string and also signifies possible matches becuase of the brackets that preceed it. 

### Quantifiers

Quantifiers specify how many times a character or group of characters can repeat. Here the quantifiers are the + and {2,6}. The + character within the paranthesis seen here ([a-z0-9_.-]+) and ([\da-z.-]+), means the characters within the brackets can be matched 1 or more times. The curly brackets around 2 and 6 {2,6}, means that the preceeding pattern (a-z here), must have at least 2 character matches, but no more than 6. Any characters allowed within the brackets counts as a match, and they don't have to be exact. "Aa" would match, but "ab" or "ac" would also match. 

### OR Operator

### Character Classes

A character class is a set of characters to be matched, and matches any one of the enclosed characters. You can specify a range using -, but if the - appears as the first or last charcter in the [], it is taken as a literal - to be included in the character class. In this email example the character classes are a-z (any lowercase letter from a to z and 0-9, any number from zero to nine).



### Grouping and Capturing

The parenthesis are used to group characters within an expression. This is known as a subexpression. The subexpression looks for an exact match. In this email address there are 3 sets of parenthesis. All are surrounding a bracket expression. The first ([a-z0-9_.-]+) and second ([\da-z.-]+) set both have the character + within the parenthesis, but outside the brackets. The + meaning was discussed in the quantifier section.
The third parenthesis is ([a-z.]{2,6}). The {2,6} is outside of the brackets, but within the parenthesis. 

### Bracket Expressions

This email code contains 3 bracket expressions. The characters for bracket expressions are []. The brackets contain characters that are wanted in the email address. This is also known as a positive character group. The first bracket expression is [a-z0-9_.-]. Within the brackets are a-z representing any lowercase letter from a to z, 0-9 representing any number from 0 to 9, and the special characters _, ., and - mean that those characters can be included. The second set is [\da-z.-]. Inside these brackets are \d which has the same meaning as 0-9 which represents any number 0-9. Next is a-z, meaning any lowercase letter from a to z. And special characters . and - which are literal matches. Note that the - character is literal in this case because it is the last character within the brackets. The last set of brackets is [a-z.]. In the brackets, a-z mean any lowercase letter. Followed by the special character ".". 

### Greedy and Lazy Match

The repetition operators are greedy operators, and by default grasp as many characters as possible for a match. In this email address the greedy operators are the + and {2,6}. Lazy operators are the opposite. They match as few characters as possible. In this example there are no lazy operators.



## Author

Lisa Walsh is a student in UNC Chapel Hill's full stack developer boot camp. 
Github profile: https://github.com/Lwalsh2022
