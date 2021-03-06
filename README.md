# A Beginner's Guide to Regular Expressions

This tutorial will guide you through the steps on how a regular expression works, the different components that make up a regular expression, and how they will ultimately simplify aspects of a search feature when implemented into your code. Regular expressions originate from a mathematical concept called "regular sets" but for our intents and purposes we can think of them as a sequence of characters that define a search pattern for a text. In programming, these patterns can be used to match character combinations within strings, so that it is possible to find and replace a character or even a sequence of characters. Regular expressions are also often used to validate/verify user input data.   

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

## Regex Components

### Anchors
`/^#`?([a-f0-9]{6}|[a-f0-9]{3})`$/`

The highlighted portions of the regular expression are the anchors. The back slashes `/` signify the beginning and the end of the expression. The `^` symbol indicates that the string in question must begin with the next symbol in the sequence. In our case the next symbol in the sequence is #. This is significant because hex codes start with a # symbol. There is an anchor at the end of the expression as can be seen by the highlighted portion at the end of the expression. The `$` symbol is used to check if a string fully matches a pattern. This is similar to the `^` symbol, but `$` signifies that the end of the string ends with whatever symbols preceed $. In our case, the end of the string must match the 3-6 character pattern before the $ anchor. Which brings us to the next section.  

### Quantifiers
/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Quantifiers tell how many characters are expected. Quantifiers specifiy how many instances of a character, group, or character class must be there for a match to be found. By default, quantifiers are "greedy" which means they will match as many characters as possible. If the characters `+ ? {}` are found in an regex, they are considered quantifiers. The `?` tells the expression to match 0 or 1 time. Because there are two different types of ways hex codes can be written, this will help determine what kind they might be. This is indicated by the {6} or {3}. The {6} signifies the hex triple format and the {3} signifies the shorthand hex format. This indicates that the length of the component preceding these quantifiers shoud be 6 or 3. 
For reference the hex triple format look like #000000 and the shorthand hex format looks like #09C. The shorthand characters would be doubled when put into hex triple format. 

### Grouping Constructs
/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/

The highlighted portion is grouped together by the parentheses (). The parentheses represent remembered matches. The grouping treats the characters as a single unit. When a match is remembered you can use $n to refer to it starting with $1-$9 and you can refer to the entire subsection with $&. You can use this feature for find-and-replace operations or any time you need to do something with part of the match. Parentheses are also used to group parts of the expression together into subgroups. 

### Bracket Expressions
/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

Brackets indicate a set of characters to match. Any character within the brackets will match unless it is negated by the previously mentioned ^ symbol which means that it would make things optional. Bracket expressions also signify the beginning of a character class or quantifier statement. So if you look at our regex closely you can see that the match can be any letter from a-f and any number from 0-9 the first calls for one that is six characters long and the second part in brackets calls for the same but in this case the quantifier indicates that it should be three characters long. 

### Character Classes
/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

Character classes are the components within the regular expression. They tell us what type of characters to expect. In our case we can see that the character classes are contained within the brackets. There are two sets of character classes in our expression. It would be repetitive to go over the contents again so please see the section on bracket expressions for an explanation on the contents of the character classes. 

### The OR Operator
/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/

The "or" operator within regular expressions is symbolized with the "|" element as seen above. It indicates that it could match either of the components on either side of the "|" element. In the case seen above we see that it can be either the hex triple format or the hex shorthand format that could match. Essentially the character classes ask for the same characters letters a-f or numbers 0-9 but the difference as mentioned before is the length and by using this | symbol we know that it could match either of the two. 

## Author
Sharon J. Yoon

I am a software engineer /  programmer that is dedicated to the life long pursuit of learning. My goal is to create applications that are intuitive and accessible for all. 

Github: [Sharonjyoon](https://github.com/sharonjyoon)
