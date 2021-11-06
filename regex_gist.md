# A Brief Introduction to Regex

"Regex" is a portmanteau of the words "regular" and "expression," and refers to a set of strings used to create patterns that assist in the matching, locating and management of text. They are accessible in a wide-range of applicatons ranging from the command line, to text-editors, and have made complex functions otherwise required for the same functionality redundant. Created in 1951 by mathematician [Stephen Cole Kleene](https://www.britannica.com/biography/Stephen-Cole-Kleene), Regex entered popular use in 1968 after being popularized by text-editors and compilers. It is now a common concept in programming and development, where it has considerably shortened the ammount of code required to achieve the same task.

In this brief introduction to Regex, we will cover a specific example in order to facilitate grasping the concept, utility and usefulness of Regex.

## Summary

For our example, we will use the following regex:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

Together we will decipher what may at first appear like hieroglyphs, in order to gain an understanding of the convenience Regex provides. As you may have concluded after noticing the "https" embedded within the string - eagle eyes! - this Regex assists in locating URLs in a text.

## Table of Contents

- [A Brief Introduction to Regex](#a-brief-introduction-to-regex)
    1. [Anchors](#anchors)
    2. [Quantifiers](#quantifiers)
    3. [Grouping Constructs](#grouping-constructs)
    4. [Bracket Expressions](#bracket-expressions)
    5. [Character Classes](#character-classes)
    6. [The OR Operator](#the-or-operator)
    7. [Flags](#flags)
    8. [Character Escapes](#character-escapes)
    9. [Practice](#practice)
    10. [Sources and References](#sources-and-references)
    11. [Author](#author)

## Regex Components

Regex syntax consists of two components:

1. Basic Elements
2. Qualifying Characters

Basic Elements assist by defining, and grouping values in a Regex, while Qualifying Characters allow us to represent certain qualification criteria in a shorter number of characters in order to sort. In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
The caret "^" (which matches a string where a specified pattern occurs) is a Basic Element, while the "*" asterix (which matches zero "0" or more occurances in the element that preceeds it) is a Qualifying Character. We'll further break down why each belong to either category, and learn what a nifty tool the "wild-card" asterix is. 

### Anchors

Anchors allow us to define the begining or end of a string by denoting either it's begingin with a caret "^" or a dollar-sign 
"$" at its end. In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
The second character (or caret) signifies that the content required needs to begin with the characters contained in the parenthesis that follows it "https?:\/\/" as grouped together. The character second-from-last (or dollar-sign) specifies that the forward slash ("/") preceding it is where the URL format ends.

### Quantifiers

Quantifers define specific requirements for the string and can be thought of as "search parameters." In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
The plus ("+") sign specifies the ammount of times the preceding conditions need to be met, and will match as many examples as possible unless more conditions are set make the requirements more narrow.

### Grouping Constructs

Similar to when used in mathematical operations, grouping constructs allow us to group a certain ammount of characters and or conditions so that other conditions. In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
and as we've noted before, the "(https?:\/\/)" has been grouped together in our example.

### Bracket Expressions

Bracket expressions allow us to denote a range of characters we are lookign for, and are placed in square braackets ("[","]"). In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
 they're used to specify a range of of possibilities "[a-z\.]" for what comes after the domain.

### Character Classes

Characters definate character sets. In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
the period (".") in this grouping "([\da-z\.-]+)" is a character class, and ensures any character (outside of the newline "\n") is matched.

### The OR Operator

The OR Operator (|) allows us to set more than one condition that needs to be met. We do not have an example of this in our example, as URLS are usually very specific in syntax.

### Flags

Flags are used to define the scope of the string, and are used at the end of a Regex. While not used in our example, they allow us to add very specific conditions to our search such as:
    1. Searching globally by using the letter "g."
    2. Case-sensitive searching by using the letter "i." and
    3. Searching multiple lines of code by using the letter "m."

### Character Escapes

Character Escapes are any characters preceeded by a backslash ("\") such as the "\n" example we've mentioned while breaking down character classes. They simply allow us to use characters reserved in Regex, so they are not understood as a part of the search pattern. In our example:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
the backslash ("\") is used to allow for the use of a forward slash ("/") as a part of our URL search "\/\/" in the "(https?:\/\/)" grouping. 

### Practice

Now that you've learned about Regex, and have a basic understanding of how it works; head over to [regexr.com](https://regexr.com/) to get some practice creating and deciphering Regex strings.

### Sources and References
1.  "[2.1: Introduction to Regular Expressions - Programming with Text ](https://www.youtube.com/watch?v=7DG3kCDx53c)" by [The Coding Train](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw) YouTube Channel.
2.  "[Regular Expression Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)" by Request-Response, [The Full-Stack Blog](https://coding-boot-camp.github.io/full-stack/).
3.  "[Regular Expressions (RegEx) Tutorial #1 - What is RegEx?](https://www.youtube.com/watch?v=r6I-Ahc0HB4)" by [The Net Ninja](https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg) YouTube Channel.
4.  "[Learn Regular Expressions In 20 Minutes](https://www.youtube.com/watch?v=rhzKDrUiJVk)" by the [Web Dev Simplified](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw) YouTube Channel.
5.  "[RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)" by Mozilla's [MDN Web Docs](https://developer.mozilla.org/en-US/).
6.  [How To Use Gists](https://www.youtube.com/watch?v=wc2NlcWjQHw) by [Digital Horizon](https://www.youtube.com/channel/UCTaWTebJrEc4S80GgBnivpw) YouTube Channel.
7.  Wikepedia Article on "[Regular Expressions](https://en.wikipedia.org/wiki/Regular_expression)".
8.  "[What is a Regex (Regular Expression)?](https://www.computerhope.com/jargon/r/regex.htm)" article on [ComputerHope.com](https://www.computerhope.com/). 
9.  Live instructon from Class Instructor [Deep Patel](https://github.com/dpat0074), and Teaching Assistants [Luca Beyrute](https://github.com/LHBO19) & [Devon Brewster](https://github.com/D-Brewst) at the [University of Toronto](https://www.utoronto.ca/) [Full-Stack Flex](https://bootcamp.learn.utoronto.ca/) coding Bootcamp.

## Author

[Aar Kaiser](https://github.com/AarKaiser) is new to the world of development, a novice coder passionate about learning and sharing information. At the time of writing this gist, Aar was in week 9 of 12 in the [University of Toronto](https://www.utoronto.ca/)'s [Full-Stack Flex](https://bootcamp.learn.utoronto.ca/) coding Bootcamp.

Aar's Gitub Profile: [Aar Kaiser](https://github.com/AarKaiser).
