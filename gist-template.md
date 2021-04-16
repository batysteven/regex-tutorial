# Regex Tutorial Matching Email

Hi, my name is Steve Baty. I am currently a student in a Full Stack Web Developer Bootcamp. Part of the course is to pick a regex sequence and describe, to our best ability, how that regex works. Let's go ahead and jump in as a try my best!

## Summary

The regex we will be using is, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.
In this tutorial I will be explaining the different components of this regex matching an email and how they work.

## Table of Contents

- [Regex Tutorial Matching Email](#regex-tutorial-matching-email)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors
The anchor in this regex is the second char, the carrot "^". The anchor is what the regex is looking for to start matching and end. In this case with this sequence we are looking for ([a-z0-9_\.-]+). These are the starting characters before the @ in an email. Here we are looking for any alphabetical character a-z, any number from 0-9, and special characeters _, ., -.
The ending anchor in this sequence is the dollar sign "$". In this case we are looking for .([a-z\.]{2,6})$. We are looking for the ".com" here. After the period ".", we are looking for up to 2 - 6 copies of any set of characters from a-z including periods.

### Quantifiers
 In this sequence we have three quantifiers. ([a-z0-9_\.-]+), ([\da-z\.-]+), ([a-z\.]{2,6}). In these 3 parts we are looking at the plus "+" in the first two and the curly brackets "{}" in the last one. What the plus sign means, we are looking for the set of characters in front of it followed by one or more of those same characters. The curly brackets are a litte different. The curly brackets mean we are looking for a string followed by 2 up to 5 copies of the seqeunece that procedes them, in this case that would be ([a-z\.]. 

### OR Operator
 In this sequence there are 3 operators. All of them are the brackets "[]". [a-z0-9_\.-], [\da-z\.-], [a-z\.]. All this means is we are matching the string inside of the brackets. The first set is any string a-z, 0-9, and special characters. The second set is matching any digit and single character from a-z. The last set is any characters from a-z and periods.

### Character Classes
 In this sequence there is one character class. \da-z. As previouslyi mentioned this is looking for any digit 0-9 and single character from a-z.

### Flags
 The flag are the forward-slash characters at the start and end of the regex. The flags are saying "Look in here for the search pattern!"

### Grouping and Capturing
 This is a very important part of the regex. Grouping allows us to match sets of data. In this case we have three groupings. ([a-z0-9_\.-]+), ([\da-z\.-]+), ([a-z\.]{2,6}). The sequence is looking for data that matches what is inside these groups. This allows us to match before the @ in the email, after the @ sign but before the period, and then after the period.

### Bracket Expressions
 Bracket Expressions are very similar to grouping and capturing. We are looking for sets of data or strings inside the brackets. We again have 3 sets of these in this regex. [a-z0-9_\.-], [\da-z\.-], [a-z\.]. That first set is looking for any character from a-z, 0-9, _, ., -. That second set is looking for any digit, character from a-z, ., -. That last set is looking for any character from a-z and ".". 

### Greedy and Lazy Match
 There is one set of greedy operators in this regex towards the end. {2,6}. What this greedy operator is saying we are looking for 2 up to 6 sets of the data that comes before in the regex. In this case that would be the [a-z\.] right before. So we are looking for 2 to up to 6 sets of data that are composed of any character from a-z and periods. 

## Author

Steven Baty, Hard worker, Husband and best friend to my wifey! Two fur babies, always a gamer at heart!
https://github.com/batysteven