# Regular Expression Tutorial (Matching An Email)

There are many different ways to search for code & verify code in Javascript. Using search methods with your desktop/laptop (CTRL + F) & even embedded functions (.startsWith, endsWith & .includes). 

## Summary

In this tutorial, I will walk you through how we use Regex to essentially program with text. In this example, I will be using the Matching an Email Regex. 

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

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

A Regex is made up of a series of different components & is considered literal. So the pattern itself must be wrapped in a slash characters (/). Below, we will be able to dive deeper into each component and what their respective roles are. 

### Anchors
The Characters (`^`) and (`$`) are both considered anchors. There are differences between the two. The (`^`) anchor signifies a string that begins with the characters that follow it. The (`$`) signifies a string that ends with the characters that precede it. 

### Quantifiers
Quanitifiers are used to set limits of the string that your regex matches. Essentially msetting a min/max number of characters that your regex is looking for. (ex: `{2,6}`)

### Grouping Constructs
In the example shown, the "Matching an Email" regex is pretty straightforward and open-ended about what it accepts. As regular expressions grow & become complicated, you may want to check multiple parts of a string to determine that different sections fulfill different requirements. To break the sections up, we can use grouping constructs. The primary way to break up your regex into sections is using parentheses (`()`). Each section that you have in parentheses is known as a subexpression.

### Bracket Expressions
Bracket Expressions & anything inside of them, represents a range of characters that we want to match. They are also known as a positive character group. Reason being, they outline the characters we want to include. (ex: (`["a-z"])`).
### Character Classes
Character classes defines the set of characters, any of which can occur in an input string to fulfill a match. I'll give you a few common character classes that you may run into. (`., /d, /w, /s`). For this specific example, you will see that we are using /d, /. /d matches any Arabic numeral digit. Which in this case, is equivalent to the bracket express (`[0-9]`).
### The OR Operator
When using an OR Operator, remember that a bracket express does not require the string to meet all of the requirements in the pattern. An example of what that would look like, would be something like this (`[abc]`) could also be written as (`(a|b|c)`).

### Flags
As we know, regex's are pretty literal. They must be wrapped in slash characters. However, there is one exception. A component known as flags. Flags are placed at the end of a regex, after the second slash. They allow/define additional functionality of limits to the regex. We aren't using any in this example currently, here are some that you may encounter.

(`g`) - Global search; the regex should be testeda gainst all possible matches in a string.

(`i`) - Case-sensitive search. Case should be ignored while attempting a match in a string.

(`m`) - Multi-line search. A multi-line input string should be treated as multiple lines.

### Character Escapes
The (`/`) in a regex escapes a character that otherwise would be interpreted literaly. As an exmaple, the open (`{`) isused to being a quanitifier, but adding a backslash before the open curly brace (`/{`) means that the regex should look for that open curly brace character instead of trying to define a quanitifier. 
## Author

Hello! My name is Corey Skidmore. An aspiring Full-Stack Web Developer. Currently enrolled in Ohio State's Full-Stack Flex Web Development Bootcamp with plans to graudate January, 2023. I love learning new concepts, languages & programs & eager to get into the world of Software Development. If you would like to take a peak at some of the work I have done, I have linked my GitHub Repository below.