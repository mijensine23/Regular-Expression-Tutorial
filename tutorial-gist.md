# Regular Expression (Regex) Tutorial 

A regular expression, also known as a regex, is a series of characters used to describe a certain search pattern. These patters are used to find or find and replace one or more characters in a string. This tutorial will display my understanding of regular expressions and their use, through the explanation of a given expression. 

## Summary

Since regular expressions are used to verify the content of a user input, they are commonly used to check the validity of entered usernames and email addresses. In this tutorial, we will cover how a regular expression is used to validate an email address "entered" by a user. The expression can be viewed below. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


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
Anchors in regular expressions signify the beginning and the end of the expression. In this case, the ^ at the start of the expression lets the reader know that the string we want to match will start with the characters following The ^ symbol. The $ lets the expression reader know that the code will end with the string information that preceds the $ symbol. 

### Quantifiers
Quantifiers in a regular expression set limits of the desired string we want to match, usually found before the $ achor and includes the minimum and maximum characters we're looking for. In this example, we're given {2,6}. When given two values inside of curly brackets, we know we are given a range of numbers. In this example {2,6} specifies that the string preceding these brackets, [a-z\.] has to be between 2 and 6 characters. 

### OR Operator
An OR operator, signified by (|) allows you to add grouping logic outside of bracket expression (which will be covered in one of the sections below). In this example, there is no use of OR operators. 

### Character Classes
Character classes are used to define character sets in regular expressions. In this expression, there are multiple examples of character classes. 
In the first bracket, [a-z0-9_\.-], 
[a-z]-lets us know we're looking for any character in range of a-z
[0-9]-lets us know we're looking for any character in range of 0-9
In the second bracket, [\da-z\.-]
[\d]- is equivalent to the [0-9] expression, letting us know we could have any digit between 0-9.
[a-z]-lets us know we're looking for any character in range of a-z. This is also found in the last bracket expression

### Flags
Flags in regular expressions define additional limits. For example, (i) would symbolize a case insensitve serach. There are 6 common flags the could be used in a regex. However, there are no examples in the expression in this tutorial

### Grouping and Capturing
Grouping and capturing in regular expressions to define logic accross multiple characters as a whole. This is usually expressed by wrapping the desired group in a set of parenthesis. In our email matching example, there are 3 different instances of grouping. 
([a-z0-9_\.-]+)
([\da-z\.-]+)
([a-z\.]{2,6})

### Bracket Expressions
In regular expressions, the characters found inside of square brackets () represents a series of characters we want to include. There 3 instances of bracket expression in our email matching example. In the first bracket [a-z0-9_\.-] we know our desired string can include [a-z], any letter from a-z, [0-9] any number from 0-9 and [_\.-], can contain underscores, a single period or hyphens. In the second, [\da-z\.-], [\d], can contain any digit between 0-9, [a-z], can contain any letter between a-z, and [\.-], can contain a single period or hyphen. 

### Greedy and Lazy Match
In regular expression, Greedy and Lazy quantifiers can be used to note how much of the string we want match. A greedy quantifier will match the longest string possible, signified by (.+), while a Lazy match, signified by ?, will match the shortest possible string. In our expression, we can see any example of a greedy quantifier inside of our first group, after our first bracket expression and inside of our second group, at the end of our second bracket expression. 

### Boundaries
In a regex, boundaries are signified by the anchor tag (/b). When found at the beginning of a string, the first character is a word character (any character that can be used to form words). If found after the last character of a string, the preceeding character is a word character. They can also be found inside of a string between a word character and a non-word character. In the email regular expression, there are no examples of a boundary being used. 

### Back-references
Back references allow you to match the same characters in a previous capturing group more than once and is defined by (\1). There are no uses of back-references in our expression. 

### Look-ahead and Look-behind
Look-aheads and Look-behinds, are matching parameters called "Lookarounds". Much like anchor tags, these define the start and end of a word, but instead of matching a specific matching characters in a string, they just signify whether the string is a match or not a match. They are signified by 
(?=) Lookahead-
(?<=) Lookbehind
(?!=) Negative Lookahead
(?<!=) Negative Lookbehind

## Author

My name is Michaela Jackson, and I'm a full-stack web developer completing a bootcamp with University of Arizona. I enjoy front-end development, especially custom CSS styling but I am learning to enjoy back-end development as well. Thank you for reading my tutorial! 

https://github.com/mijensine23
