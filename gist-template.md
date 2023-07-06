# Hex Value Regex Tutorial!

Hello! This short tutorial will help you understand more about how the Regex function (as seen below) works to verify that what you have typed, is actually a proper Hex value! (such as #123456 is a dark shade of cyan-blue!)

## Summary

Do you want to see what the expression looks like? Look no further! The expression below checks to make sure you have a proper hex value input!

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Pretty cool huh? Let's jump in and learn how it works!

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

A regex is considered a literal, so the pattern must be wrapped in slash characters (/).

View our expression below again, you'll notice the sections we are talking about are bolded and cyan!

<span style="color:#6fcb9f; font-weight: bold">/</span>`^#?([a-f0-9]{6}|[a-f0-9]{3})$`<span style="color:#6fcb9f; font-weight: bold">/</span>

(fun fact, instead of just using color:cyan, a certain string of numbers followed by a hash symbol was used 😉)

On to the rest of the components!

## <span style="color:#9bcd9b">Anchors</span>

The characters ^ and $ are both considered to be anchors.

`/`<span style="color:#6fcb9f; font-weight: bold">^</span>`#?([a-f0-9]{6}|[a-f0-9]{3})`<span style="color:#6fcb9f; font-weight: bold">$</span>`/`

In this example, the ^ anchor signifies the beginning of the string, while the $ anchor signifies the end of it! 

## <span style="color:#9bcd9b">Quantifiers</span>

Quantifiers are interesting! These are mainly what you find inside of the curly brackets! Aside from just that though, they also include the +, *, and ? symbols!

`/^#`<span style="color:#6fcb9f; font-weight: bold">?</span>`([a-f0-9]`<span style="color:#6fcb9f; font-weight: bold">{6}</span>`|[a-f0-9]`<span style="color:#6fcb9f; font-weight: bold">{3}</span>`)$/`

In this case, the ? symbol makes sure that the number of #s is appearing either 0 or 1 time!

The {6} defines that you are matching the pattern exactly 6 times.

Likewise with {3} it is defining that you are matching the pattern exactly 3 time!

## <span style="color:#9bcd9b">Grouping Constructs</span>

The main way that you group a section of a regex is with parenthesis. In normal cases any extra parenthesis inside the parent parenthesis, become known as a subexpression. However in our case, we don't use inner parenthesis, we use `[brackets!]`

`/^#?`<span style="color:#6fcb9f; font-weight: bold">(</span>`[a-f0-9]{6}|[a-f0-9]{3}`<span style="color:#6fcb9f; font-weight: bold">)</span>`$/`

In this case, the one pair of parenthesis wraps the entirety of what can appear after the # symbol! We'll learn about the brackets next!

## <span style="color:#9bcd9b">Bracket Expressions</span>

Utilizing the brackets as a subexpression as detailed above, we make sure that the input matches the characters enclosed inside of them!

`/^#?(`<span style="color:#6fcb9f; font-weight: bold">[a-f0-9]</span>`{6}`|<span style="color:#6fcb9f; font-weight: bold">[a-f0-9]</span>`{3})$/`

In our case, each bracket is making sure that our input only includes letters between a and f, as well as numbers between 0 and 9!

## <span style="color:#9bcd9b">Character Classes</span>

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## <span style="color:#9bcd9b">The OR Operator</span>

The OR Operator is the fancy little | symbol! It signifies that you can have this set of input OR this set of input.

`/^#?([a-f0-9]{6}`<span style="color:#6fcb9f; font-weight: bold">|</span>`[a-f0-9]{3})$/`

In our case it is saying `[a-f0-9]{6}` OR `[a-f0-9]{3}`

They are both almost identical, but it signifies that it is either looking for a string of either 3 or 6 characters that fall within the proper characters as listed in the above section!

## <span style="color:#9bcd9b">Flags</span>

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## <span style="color:#9bcd9b">Character Escapes</span>

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
