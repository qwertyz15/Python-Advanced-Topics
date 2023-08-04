# Regular Expressions (Regex)

Regular expressions (regex) are versatile tools for pattern matching and text manipulation. Here's a guide to frequently asked questions about regular expressions in interviews:

## Table of Contents

- [Understanding Regular Expressions](#understanding-regular-expressions)
- [Creating Regular Expressions in Python](#creating-regular-expressions-in-python)
- [Using `re.search()`](#using-research)
- [Global Search with `re.findall()`](#global-search-with-refindall)
- [`re.match()` vs. `re.search()`](#rematch-vs-research)
- [Using `re.sub()`](#using-resub)
- [Character Classes](#character-classes)
- [Metacharacters](#metacharacters)
- [Anchors (`^` and `$`)](#anchors--and-)
- [Non-Capturing Groups](#non-capturing-groups)
- [Quantifiers](#quantifiers)
- [Backreferences](#backreferences)
- [Case-Insensitive Matching](#case-insensitive-matching)

## Understanding Regular Expressions

- A regular expression is a sequence of characters defining a search pattern.
- It's used for matching and manipulating strings based on a specified pattern.

## Creating Regular Expressions in Python

- Use the `re` module in Python to create and work with regular expressions.
- For example: `import re pattern = r'\d+'` (matches one or more digits).

## Using `re.search()`

- `re.search()` searches for a pattern within a string and returns the first match found.

## Global Search with `re.findall()`

- `re.findall()` finds all occurrences of a pattern in a string and returns them as a list.

## `re.match()` vs. `re.search()`

- `re.match()` searches for the pattern only at the beginning of the string.
- `re.search()` searches for the pattern anywhere in the string.

## Using `re.sub()`

- `re.sub()` replaces occurrences of a pattern in a string with a specified replacement.

## Character Classes

- Character classes, denoted by square brackets, match any character from a set.
- For example: `[aeiou]` matches any vowel.

## Metacharacters

- Metacharacters are characters with special meanings in regular expressions.
- `.` matches any character, `*` matches zero or more occurrences, etc.

## Anchors (`^` and `$`)

- `^` matches the start of a string, and `$` matches the end.
- They anchor the pattern to specific positions.

## Non-Capturing Groups

- `(?: ... )` is a non-capturing group for logical grouping without capturing the matched text.

## Quantifiers

- Quantifiers specify how many times a character or group should appear.
- `*` for zero or more, `+` for one or more, `?` for zero or one.

## Backreferences

- Backreferences (`\1`, `\2`, etc.) match the same text as previously matched by a capture group.

## Case-Insensitive Matching

- Use the `re.IGNORECASE` flag or `(?i)` within the pattern for case-insensitive matching.

---

Illustrate your proficiency in regular expressions by explaining these concepts, providing practical examples, and discussing how regex can effectively handle pattern matching and text manipulation tasks.
