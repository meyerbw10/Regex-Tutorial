# Regex (Regular Expressions) Tutorial

This regular expression (regex) tutorial was made in order to teach those who either want to brush up on the beginings of regex, or want to learn regex. Regex can be very useful in many cases, it all depends on your imagination and creativity, and its a very cool thing to learn about! 

## Summary

Regular Expressions are a string of characters that express a search pattern and this document will provide an expression to locate hex values as well as present a broad idea of regular expressions (regex). By the end of this document, you will read how to use regex on a basic level as well as have a better understanding on the syntax of regex.

Link to Repo https://github.com/meyerbw10/Regex-Tutorial

---
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)



![](/images/regex.jpeg)

## Regex Components

We are going to be using Matching an Email: **^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$** code as my example. It looks like Giberish now but by then end you'll be able to look at it and it make more sense.


---

## Anchors

The characters '^' and '$' are both considered to be anchors.

* The "^" tag can be used to search for characters where that line starts with that character or string. For example, if we had a line of code, "My Little Brother Ben is a lad.", "^M" will highlight the character "M", which indicates that this line of code starts with the character "M".

* The "Dollarsign" anchor tag is used to find keywords that end in whatever string or character you put right before the "Dollarsign" tag. If we are searching for an email, like we are in my example, "test@gmail.com" I would use ".com$" in order to search for an email. Of course, due to links also ending in ".com", I would have to specific further, which I will be going to explain further down below. But for the sake of this example visualize it that way looking back at our Main Email matcher example.


## Quantifiers

Now, picking up where I left off in the Anchors tag. the $ in our example code has these Brackets {} behind it with numbers inside them {2,6}. So based on what I said before then we are looking for something with the numbers 2 and 6 at the end. But thats not what it means. The {} Brackets are Quantifiers. Quantifiers can only be used in conjunction with other tags. They cannot be used separately. They are used in order to specify your search further.

* The "{}" tags are used to define how many times you want a character to repeat. Within our Matching an Email example, "([a-z\.]{2,6})", the "2" & "6" within the curly brackets ("{}") are specifying that we want What we are searching for to be between 2 and 6 characters , a-z or 0-9. It can be any combination, but it must only be letters between "a" and "z" or numbers between "0" and "9".

* The + tag is a quantifer. The Plus tag goes in at the end of our first two Parenthises paired Brackets. What the + tag is used for here is that it is telling us that we need to match with at least one of those paramaters in the brackets ([*here*]+)


## Grouping Constructs

Parenthesis, or "()" are used to group your string for one single search. Take our Emailer locator for example," ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ ". Within the parenthesis, we have 6 tags here that we use to define our constraints ("[] & +" , "[] & +" , "[] & {}").


## Bracket Expressions

In our Email locator, you will find "[a-z0-9\.-]". The hyphen, or "-" is similar to "through". "a-z" will be looking for letters "a" through "z". Same thing with number "0" through "9". Our expression will only be looking for characters "a-z" or "0-9". but also it has the "\" tag which adds thats its looking for "."'s and "-"'s as well!
 

## Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 

* "." is like an all search. It will highlight anything except for a line break (\n).

* "\d" refers to "digit". Essentially it is anything "0" through "9".

* "\w" refers to alphanumeric characters (Uppercase and lowercase A-Z, 0-9, and the "_" or underscore).

* "\s" refers to a space, line breaks, and tabs (basically any blank space).


## The OR Operator

The "|" tag is used as an OR operator, meaning that it will take "A" OR "B". Check this example below for a better visual

* "([a-z0-9]{6} | [a-z0-9]{3})"

* Our expression will take a six length string of characters "a" through "z" / "0" through "9" OR a three legnth string of characters "a" through "z" / "0" through "9". Remember, our "[]" define which characters we are looking for, and our "{}" will set the specific length we want those characters to be.


## Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex.

* "g" is a global search, meaning it will try every character within a string to see if it matches the constraints.

* "i" makes your search case-insensitive, so even if you search for "THE", "the" will still highlight.

* "m" is a multi-line search.

## Character Escapes

The "" tag ends your search for whatever you input for your search. Though we do not use "" within our function, you can use this tag in order to end your search. You can also use "" in order to search for specical characters. This would be useful if you are looking for brackets or any other specical character that we use to define our constraints for a search.


---
# Author

My name is Bradley Meyer, I am currently enrolled in The Ohio State University as a Full-Stack Developer Bootcamp student. I am open to learn any language and look forward to making connections with anyone within the computer science field.

Follow this link to my GitHub Profile: https://github.com/meyerbw10