# Regex

Notes for regular expressions from [this](www.regular-expressions.info) site.

## Regex Metacharacters

There are 12 characters in regular expressions that have a special meaning:

```
\
^
$
.
|
?
*
+
(
)
[
{
```

Using these literally in regex requires escaping with a backslash. This is **not** the case when using these in character classes - then the only metacharacters are `] \ ^ -`. In the latter case, escaping using a backslash is required again,

## Character classes or sets
A character class is made by enclosing characters with [], and matches only one of the several characters. 
A range of characters can be specified using a hypen, e.g. ```[0-9a-z]```.

## Shorthand character classes
`\d` matches a single character that is a digit.
`\w` matches a "word character" (alphanumeric characters and underscore).
`\s` matches a whitespace character.

## Anchors
`^` refers to the first position in a character/string.
`$` refers to the last position in a character/string.
`^b` matches only the first b in `bob`.
Adding a caret sign `^` at the beginning of a character class is used to negate the class.
`\b` refers to word boundary. `\B` matches at every position where `\b` does not match.
`\w` refers to a word.

##Alternation

`|` is used to refer to OR.

##Repetition
`?` makes the preceding token in a regular expression optional.
`*` makes the preceding token repeat 0 or more times.
`+` makes the preceding token repeat 1 or more times.
These quantifiers are greedy, and the `?` is put after them to make them lazy.

##Grouping
Place `()` around tokens to group them together. For example, `Set(Value)?` matches `Set` or `SetValue`.

##Backreference
Within the regular expression, you can use the backreference `\1` to match the same text that was matched by the capturing group.
