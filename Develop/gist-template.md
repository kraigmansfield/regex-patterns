# Email Regex Pattern Tutorial

This gist will go over regualr expressions or RegEx. Regex is a tool used to define a search term parameter. 


## Summary

The Regex we will be breaking down searches for an email pattern within a string.


```
[a-z0-9]+@[a-z]+\.[a-z]{2,3}
```

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

```
[a-z0-9]+@[a-z]+\.[a-z]{2,3}
```

The Regex can be broken down into three distinct elements.

Element 1: Username ```[a-z0-9]``` 
    This element searches for a username using alphanumeric characters. a-z denotes the alphabet and 0-9 denotes numbers. This particular example would fail if it included dashes, underscores, or special characters.

The @ character denotes the divide between Username and Domain.

Element 2: Domain ```[a-z]+```
    This element searches for a domain using letters.

The ```\.``` is a quantifier. It denotes the ```.``` between the Domain and the Suffix

Element 3: Suffix ```[a-z]{2,3}```
    This element searches for a suffix using letters. ```{2,3}``` is a quantifier, it is looking for a suffix between 2 and 3 characters long.

### Anchors

Anchors match a position before, after, or between characters. They are used to "anchor" the regex match at certain positions. This particular snippit does not contain any anchors.

### Quantifiers

```/.``` and ```{2,3}``` are quantifiers. This first, denotes the ```.``` between Domain and the Suffix. The latter, is looking for a suffix between 2 and 3 characters.
 
### OR Operator

The OR operator ```|``` denotes a choice between two options. ```[a-z]|[0-9]``` for example, this would search for either a through z OR 0-9.

### Character Classes

Regex has special character classes that match types of characters. 
```\d``` for example this is used to match any digit character. Our email Regex does not contain any character classes.

### Flags

Flags are captured at the end of a Regex. For example ```g``` does not return after the first match, restarting the subsequent searches. Our Regex does not contain any flags.

### Grouping and Capturing

Grouping and Capturing is done with ```()``` in regex. Anything within a set of parentheses is taken as a single group, which allows information to be treated as a single unit. Our regex does not contain grouping or capturing. 

### Bracket Expressions

A bracket expression represents a single character, which can be anything specified within the brackets. Our regex has three bracket expressions.
```[a-z0-9]```
```[a-z]```
```[a-z]```


## Author

Kraig Mansfield is a full-stack developer student at the University of Washington.
