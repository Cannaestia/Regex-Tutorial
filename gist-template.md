# Regex Tutorial

This is a short tutorial on how to create and understand what a Regex is.

## Summary

I will be explaining how to match a Hex Value using Regex I will be using the Regex /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The ^ and $ symbol are both considered to be anchors. 
The ^ anchor signals that a string begins with the characters that follow directly after the anchor.
* For example ^# will match anything that directly starts with a #.

The $ anchor on the other hand signals that the string ends with the value that proceeds it. 
* In our expression for example, the $ signifies that our expression must end with [a-f0-9].

### Quantifiers
Quantifiers define thelimits of the string that matches your regex. They can sometimes include the min and max numbers that 
your regex is looking to match. Quantifiers include:
* *-Matches the pattern zero or more times.
* +-Matches the pattern one or more times.
* ?-Matches the pattern zero or one time.
* {}-The curly brackets provide 3 different wasy to set limits.
  - { n }-Matches the pattern EXACTLY n number of times.
  - { n,  }-Matches the pattern at LEAST n number of times.
  - { n, x }-Matches the pattern a minimun of n number of times and max x number of times.
* For example, in our expression we see {6} and {3}. 
  This means those sections match exactly 6 number of times and 3 number of times. 
* the ? at the start of our expression /^#? <== means that the patterned can be matched zero or only 1 time. 

### Grouping Constructs
The way to group sections of your expression is by using parentheses (). These sections are called subexpressions.
* In our Hex expression we have a subexpression ([a-f0-9]{6}|[a-f0-9]{3}) as it is being grouped together in the parentheses ().

### Bracket Expressions
Anything that is in square brackets ([]) indicates a range of charcters we are attempting to match.
* Our expression [a-f0-9] indicates that we are looking for something in the range of a-f and or between 0-9. 

### Character Classes
In regex a Character Class is defined as a set of characters, any one of which can occur in an input string to fulfill a match.
Some of the common character classes include:
* .-Matches any character except the newline character(\n)
* \d-Matches any number or digit. This can also be written as [0-9].
* \w-Matches any letter from the alphabet and can include the _. This is also equivalent to [A-Za-z0-9_]
* \s-Matches a single whitespace character, including tabs and breaks.

### The OR Operator
In our expression we see the OR Operator between our Bracket expressions. This indicates that we can match either the 
[a-f0-9]{6} or the [a-f0-9]{3}.


### Flags
Typically a regex is wrapped in forward slash characters (/ regex here /), unless a flag is being used. Flags are placed
at the end of the expression and define additional functionality or limits that the regex can have. 
The most commonly used flags are:
* g-Global search: the regex should be tested against all possible matches in that string.
* i-Case-inssensitive search: case should be ignored while attempting a match in a string.
* m-Multi-line search: a multi-line input string should be treated as multiple lines.

### Character Escapes
The \ backslash is used in a regex to prevent a character from being interrupted. This is mostly used when looking for strings that include special characters.

## Author
Hello, my name is Jennifer and I am an aspiring full stack developer. 
https://github.com/Cannaestia

)