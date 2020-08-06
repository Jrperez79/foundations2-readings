# Reading-04b

## RegExr
Character classes
.	any character except newline
\w\d\s	word, digit, whitespace
\W\D\S	not word, digit, whitespace
[abc]	any of a, b, or c
[^abc]	not a, b, or c
[a-g]	character between a & g

Anchors
^abc$	start / end of the string
\b\B	word, not-word boundary

Escaped character
\.\*\\	escaped special characters
\t\n\r	tab, linefeed, carriage return

Groups & Lookaround
(abc)	capture group
\1	backreference to group #1
(?:abc)	non-capturing group
(?=abc)	positive lookahead
(?!abc)	negative lookahead

Quantifiers & Alternation
a*a+a?	0 or more, 1 or more, 0 or 1
a{5}a{2,}	exactly five, two or more
a{1,3}	between one & three
a+?a{2,}?	match as few as possible
ab|cd	match ab or cd

## Regex Tutorial
Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).

Fields of application range from validation to parsing/replacing strings, passing through translating data to other formats and web scraping.

Basic topics
Anchors — ^ and $
Quantifiers — * + ? and {}
OR operator — | or []
Character classes — \d \w \s and .
Use the . operator carefully since often class or negated character class (which we’ll cover next) are faster and more precise.
Flags
- g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
- m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
- i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

Intermediate topics
Grouping and capturing — ()
This operator is very useful when we need to extract information from strings or data using your preferred programming language. Any multiple occurrences captured by several groups will be exposed in the form of a classical array: we will access their values specifying using an index on the result of the match.

Bracket expressions — []
Remember that inside bracket expressions all special characters (including the backslash \) lose their special powers: thus we will not apply the “escape rule”.

Advanced Topics
Boundaries — \b and \B
\b represents an anchor like caret (it is similar to $ and ^) matching positions where one side is a word character (like \w) and the other side is not a word character (for instance it may be the beginning of the string or a space character).

Back-references — \1
Look-ahead and Look-behind — (?=) and (?<=)

## Regex 101
- regex101.com for trying and testing strings
