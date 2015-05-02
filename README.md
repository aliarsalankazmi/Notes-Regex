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

Using these literally in regex requires escaping with a backslash.

## Character classes or sets
A character class is made by enclosing characters with [], and matches only one of the several characters. 
A range of characters can be specified using a hypen, e.g. ```[0-9a-z]```.

