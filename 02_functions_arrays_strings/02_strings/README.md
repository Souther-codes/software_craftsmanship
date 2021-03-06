## Strings

We briefly discussed strings in chapter 1. We're going to take a deeper dive in
this section, exploring some a few utilities that will make our lives much
easier.

A string is a (possibly empty) list of characters that are grouped together. You
can create them manually, or get a string from what the user typed with `input`
in Python, `readline` in TypeScript, or `scanf` in C. Once we have a string, we
have seen how to compare it to match exactly the contents of another string.
That does have the consequence of needing to be case sensitive, so if we want to
check if the user typed a "y", we would probably need to check for both `"Y"`
and `"y"`.

Once we have some strings, we've seen one way to put them together - using the
`+` sign. For numbers, this adds them, but for strings, it joins them together
into a bigger longer string. We can use that to put the result of a variable
into a bit of text formatted for human readability. To do this, we do have to
ensure all the things we're concatenating in this way are themselves strings.
Python and C have specific functions to do this, while TypeScript does it
implicitly. There are also functions in all our languages to take a string and
parse it (read the characters and determine the appropriate value) into any of
our other data types, most often a number of some sort.

Because this process of joining strings, and using functions to convert to and
from strings, is tedious and error prone, we have tools that can take a
"template string" and fill in the values per some specification. This achieves
several benefits. For one, it means that the template string itself can be a
single entity we pass around, rather than a complex expression. This lets us
change the text quickly, without having to change where we `+` the strings
together. The template strings have facilities to describe how we want our data
formatted. When we have printed out floating point numbers, we often
accidentally get things like `4.0000000000001` as a result of round off. With
template strings, we can ask for at most 2 or 3 digits, and fill them in with
`0` if the number is whole.

There are a few more common operations on strings that we have libraries for.
These usages don't come up every day, but do show up regularly enough that we
can discuss them & see some examples, so you'll at least have the memory they
exist when you come across a problem that could use them.

The first is the idea of substrings. A **substring** is exactly what it sounds
like - a part of a larger string. Substrings are used regularly when you need
to do any of your own parsing - any time you need to write a program that
looks into a string and pulls content out of its data. Substrings are always
specified as the starting index within the string, and either the end index
(exclusive) or the number of characters to take. The ability to change and
edit a string based on its substring depends on each language, but each
language does provide a mechanism to do so.

An **index** in this context is just a numerical count of number of
characters into the string to look at. It's important to know and remember
that indicies start at `0` - the don't give you the `1st` or `3rd` character
in the string, but rather specify the number of characters to skip before it
starts reading. So the `1st` character is at substring index `0`.

Finally, there are a few methods that a string lets us use to manipulate it.
We can take a string and make it all **uppercase** or all **lowercase** (or
get a substring and make that substring all upper or all lower). You can
often **count** the number of occurances of a character or (shorter) string
inside another. And there are utilities to **find** occurances of a string in
another, and then **replace** those occurances with some other value.

[python](./01_python.md)