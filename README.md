# A Beginner's Guide to Regular Expressions

This tutorial will guide you through the steps on how a regular expression works, the different components that make up a regular expression, and how they will ultimately simplify aspects of a search feature when implemented into your code. Regular expressions originate from a mathematical concept called "regular sets" but for our intents and purposes we can think of them as a sequence of characters that define a search pattern for a text. In a programming, these patterns can be used to match character combinations within strings, so that it is possible to find and replace a character or even a sequence of characters. Regular expressions are also often used to validate/verify user input data.   

## Summary

The tutorial will break down all of the components of a regular expression that are used to match Hex values. Hex values are used as color codes that tell the display how much of a color to show. So, if we break it down a hex code is a representation of hos much red, green, and blue are in a color. This code consists of six characters. The first two show how much red is in the color, the next two represent the green, and the last two show the amount of blue. These hex codes refer to specific colors that allow the designers or developers to easily depict the exact color they had in mind. We can even calculate the hexadecimal number that shows the intensity of these color segments, but for what we are studying here, we need only know that regular expressions can be used to match these useful hex codes. The regular expression used to do so looks likes the following.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The next steps will break this down and make it comprehensible. 

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
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author
Sharon J. Yoon

Sharon is a software engineer / programmer 
