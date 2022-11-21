# Title (replace with your title)

Regular expressions define a search pattern that are used by programmers to parse out large bodies of text. Today, I will be detailing a regular expression used to parse out email addresses from strings of text.
## Summary

The regular expressions in question is as follows: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. We'll go into more detail later, but in short, the regular expression is broken down into three parts encased in parentheses. The first part searches letters and numbers. The second part searches for letters and numbers. The third part searches for letters with a length of 2-6 characters. 

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

The first thing you will notice when reading this expression is a '/'. This is because a regular expression is a literal. All literals are encased in a '/', which is why there is another one at the end of the expression. There are a few literal characters, namely the '@' symbol between the first and second part and '.' between the second and third part. The characters inside the parentheses are meta characters. Meta characters do not define a specific character but a type of character. Some examples of meta characters used in this expression are '\d' which means 'any number 0-9', '.' which means 'any character at all', 'a-z' which means 'any lowercase letter'.

### Anchors

The anchors used in this regular expression are '^' and '$' found at the beginning and end of the expression, respectfully. The carrot and dollar sign anchors are universal so expect to see them elsewhere. 

### Quantifiers

The quantifiers of this regular expression refer to the '+' at the end of the first part of the expression. In this context, '+' means "must have 1 letter, minimum, with no upper limit'. 

### Grouping Constructs

The 'grouping constructs' in this expression refer to the parts that I've described throughout this summary. By using parentheses to split up their expression, programmers can search for different characters at different points in any given string. This allows programmers to hone on similar strings, such as one finds with emails and telephone numbers.

### Bracket Expressions

The 'bracket' expressions are used by programmers to set quantifiers within the parent construct and to define a pattern at a specific point in the search query. In the given email expression, the '+' quantifier is found outside the bracketed search query, but inside the parentheses. '([a-z]+)' means there must be at least one letter. Were the '+' to be inside the bracket, then it would suggest another set of characters to define a search query that will be added to the 'a-z' query. 

### Character Classes

The character classes refer to the sets of characters previously discussed. For example, '\d' is an example of a character class, as is 'a-z'. 

### The OR Operator 

N/A

### Flags

N/A

### Character Escapes

Character escapes are used to search for a specific character that might otherwise be used in a meta search. You could say that character espaces 'literalize' meta characters. In the email expression, '\.' is used to search for a '.' given that '.' normally searches for any character.

## Author

If you enjoyed my write-up on expressions and would like to see more of my content, check out my GitHub at https://github.com/zorobijan.
