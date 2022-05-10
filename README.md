# Regular Expressions Tutorial (regex Made Simple)

In many aspects of our lives exist patterns, and methods for fiding such. Ever needed to verify an email or password? How about identification at the DMV? Sure you have. And although the aformentioned methods may seem different in use cases, there stands a commonality -- patterns. At a DMV, the clerk would go through your information and check that it matches whatever is found in the database. The same goes for your personal information on the web. But have you ever wondered how a computer searches for commonalities? While it may be straightforward to imagine a human such as yourself completing this type of task, but it's a little different for a set of wires and components. Though, just as in the first example, there yet exists, you guessed it... patterns! More specific: `Regular Expressions`, or `regex` for short. 

Here's the catch: They've been made simple for your brains consumption! 

## Summary

Since this shouldn't be too difficult for your comprehension, we'll break down each level of how a regular expression works. Let's look at a basic `Matching email` regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 

"Simple? There's no way all of this mumble jumble could be simple!" This may look difficult now, but keep this mind as you read: What you're looking at is ENGLISH. If a human brain could come up with this, then yours can definitely decipher it in no time!

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
The components which make up a regex include the following which you will read through. One thing to note: Due to being known as a `literal`, or including basic datatypes `(Booleans, Strings, Numerals, Integers, Characters, Floating-Point Numerals, etc)`, a regex must use 'literal notition'. In other words, all components are to be wrapped in `/`. Keep this in mind as we cascade through the intruiging anatomy of the regex.

### Anchors
The first aspect of a regex we'll be discussing is an `Anchor`. Two very prominent anchors included in our example include `^` and `$`. The `^` signifies a string which begins with its following characters. The `$` does the same thing, but at the end of a regex for all preceding characters.

For matching an email, you'd need to tell the code where to start as well as where to end. Think of them like a race; a race has a beginning and ending endpoint, no?

### Quantifiers
Now it's time to get a little greedy... What do I mean by that? When discussing `Quantifiers`, it's hard not to be. Notice the `{2,6}` at the end of our example? This is known as a quantifier, and its job is to limit the string which your regex will match. The `3` is the minimum number of characters the regex will search for, while the `6` is the maximum. 

More quantifiers include `*, +, ?, and {}`. The `+` included above will check the regex matches the specified pattern one or more times.  The `{}` which holds our min and max specifications provide three separate ways to limit matches: `{ n }` matches just a certain number of times, `{ n, }` matches at LEAST a certain number of times, and `{ n, x }` matches a minimum and a maximum number of times.

### Grouping Constructs
Not every regex is going to be held within the same container. Just as a bag of oranges serves its role, so too, does a bundle of apples. Each holds a separate fruit, yet when totaled, can be described as a 'bunch [of fruit]'. In a similar way, a regex holds different constructs which, while different, can add into a greater whole. 

If the apples and oranges analogy doesn't create a spark in your brain, think of Legos: Each piece, while separate, some yet similar, when added together into sections, can create new entities entirely. In a regex, this is known as `Grouping Constructs`.

`()` is what holds section pieces together. Take, for example, `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})`. The first construct gives a set of specifications, and so too do the second and third follow suit. When these individual pieces are formed, the posibilities for what the regex can search for are expanded to fit your specific needs!

### Bracket Expressions
We've touched a bit on `()`, but you may have seen its cousin, `[]`. These `Bracket Expressions` represent a range of characters needing to be matched. For example, `[a-z]` is the equivalent to `[abcdefghijklmnopqrstuvqxyz]`. That hyphen (`-`) and underscore (`_`) you see here `([a-z0-9_\.-]+)` are special characters, which allow us to include ranges, but only within these brackets is it possible.

### Character Classes
You've seen `/`. We discussed this special piece at the beginning of this tutorial. But you might be wondering what `\` is all about, or `.`? These are known as `Character Classes`, which define a set of characters, any one of which can occur in an input string to submit a match.  

The `\d` is equivalent to `[0-9]`. The `.` matches any character except `\n`, or newline character, which is a line separator.

### The OR Operator
Something not present in our example, but necessary nontheless, are `OR` `|` operators. Just like in other parts of code, the OR is used to search for a specific characters, either this OR that. For example, `(a|b|c)` will search for either an a, b, or c. This could come in great handy when attempting to find one OR the other of a pattern.
 
### Flags
`Flags`, like the OR operator, aren't something we'll be using, however, it can provide much needed assistance in a regex. Some of the most well known flags include `g` (global search), `i`(case-insensitive search), and `m`(multi-line search). These are useful when not using slash characters. You don't need them when working with flags. The more you know!

### Character Escapes
Last but not least, we'll take a look at an `Escape`. A character escape looks something like this: `\`. Our example has a few, and they are used to escape characters which would be interpreted literally if not for them. This means that instead of defining a specific character, say `{`, as a quantifier, the escape will instead search for an actual, literal curly brace.

## Author
And that ends our tutotial! Did you find easy to understand? If you're in need of any further help with regular expressions, here's a helpful link.<br/>

[Regex Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)<br/>

James Edwards<br/>

[My Github](https://github.com/jimbolikesgithub)<br/>
[Regex Tutorial Repo](https://github.com/jimbolikesgithub/Regex-Tutorial-17)

