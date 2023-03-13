# Regular Expression for Validating Emails


## Summary

Regular expressions, or Regex as they’ve become known, is a sequence of characters that defines a specific search pattern. This can be used to achieve certain tasks such as finding usernames, emails, URLS, Hex values, or HTML tags. To help further understand what exactly a regex is and how they function, let's dive deeper into an example. We're gonna look at an example of matching an Email address and breakdown each part of how exactly this works. 

`Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

As stated earlier, regular expressions are a series of special characters that define a search pattern and allow us to search through a string of text. When looking at the regex example above, it's tough to visualize this as anything more than just a random mixture of characters; however, there is actually good reasoning for this. Pertaining to our Email matching example, the regular expression is a key piece for creating secure apps and being able to match. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Sources](#sources)

## Regex Components

### Anchors
The anchor is what starts and ends the regular expression. In the matching email code,

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

the anchors are the ^ and the $. This code specifically is saying that we are looking for something that starts with...

`^([a-z0-9_\.-]+)`

we will define what everything inside the parentheses later in this tutorial, but what the anchor means is that if we are to find a match it has follow those initial guidelines. It also has to end with...

`.([a-z\.]{2,6})$.`

It HAS TO start and end with the given parameters within the code. If it does not, then it is not a match and a error will appear .

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, `xyz+` then this will match any string `xy` followed by at least one `z`. Now if we look at our code for matching the email:

`([a-z0-9_\.-]+)`

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier + means that it has to contain at least one of this in order to have a match.


### Grouping and Capturing

Regular expressions are generally broken up into sections using parentheses `()`. The groups within this example are of the capture category, meaning the save matched sequences for reuse. Looking at the above example, you can see it is  broken into three separate sections: `([a-z0-9_.-]+)`, `([\da-z.-]+)`, and `([a-z.]{2,6})`. Within each group construct, you can see a set of characters within brackets ([]), and these are called...

### Bracket Expressions

A bracket expression is anything found within brackets `[]` and creates a range of characters which tell us what we want to match within the text. In our example, we can find three bracket expressions: `[0-9]`, `[a-z]`, and `[_.-]`.

`[0-9]` denotes any number between 0 and 9. `[a-z]` denotes any lowercase letter from a to z. If you wanted to also include uppercase letters, you would need to use 
`[a-zA-Z}`. Lastly, `[.-]` denotes the special characters that can be used: underscore `_`, backwards slash `/`, period `.`, and dash `-`.

### Character Classes

Simply put, a character class can define a set of characters which occurs in input strings in order to full-fill a match. The bracket expressions mentioned previously are examples of this. There are two more instances of this that can be found in our email example.

A period `.` matches any character except the newline character `\n`.

The last instance of this in for our email example is, `\d`. This denotes any Arabic number and is equal to the bracket expression `[0-9]`.

### Conclusion 
While regular expressions can be very confusing at first, I think that after breaking them down to their individual components we can agree that they really are not too scary. I highly recommend taking a lot at regexr.com when working with regular expressions because it is a great way to visualize the regex and understand the components better. 


### sources
The Full-Stack Blog 
https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial

MDN Web Docs for Regular Expressions
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

regexr website 
https://regexr.com/
## Author
 Alex Biggs is a Full Stack web developer who is always trying to expand his knowledge and help anyone understand coding concepts at a deeper level. 