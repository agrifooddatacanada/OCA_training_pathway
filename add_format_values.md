# Add Format Values of the Data Fields

The format values entered for the format overlay are dependent on the [attribute types](create_first_schema.md#attribute-types) defined in the Capture Base. Especially, we have:
- **Text/Numeric**: Regular Expression (Regex)
- **Binary**: MIME type registered with the Internet Assigned Numbers Authority
- **DateTime**: date and time representation as defined by ISO 8601

## Regex

The regular expression, or shortened as "regex", is a powerful way to search and filter strings. You could build a search pattern using character literals, operators, or constructs to match specific types of characters in a string. The OCA uses the Rust regex Flavour, with the full documentation that could be found [here](https://docs.rs/regex/latest/regex/#syntax). 

### Frequently Used Regex Syntaxes

#### Character Classes and Ranges

The character classes and ranges would appear inside square brackets (`[...]`). A character class would match a single character with the following pattern:

- `[abc]` matches character `a`, `b`, or `c`.
- `[^abc]` matches any character that is not `a`, `b`, or `c`.
- `[a-c]` matches any character in the range `a-c`, that is, `a`, `b`, or `c`.
- `[a-zA-Z]` matches any character in the range of `a-z` or `A-Z`, that is, any uppercase or lowercase letter.
- `[0-9]` matches any single digit.

#### Composites and Repetitions

- `abc|xyz` matches `abc` or `xyz`.
- `a*` matches `a` repeated for **zero or more** times.
- `a+` matches `a` repeated for **one or more** times.
- `a?` matches `a` repeated for **zero or one** time.
- `a{n, m}` matches `a` repeated for **at least** `n` and **at most** `m` times.

#### Anchors

You may have noticed that the regular expressions allow partial matching by default. E.g. `abc` actually matches any string that **contains** the pattern `abc`; it could be `abc`, `abcde`, or `&0xyzabcdef-()`. 

The following anchors would help.

- `^` matches the beginning of the string. `^abc` only matches strings that **begin** with `abc`.
- `$` matches the end of the string. `abc$` only matches strings that **end** with `abc`.
- `^abc$` only matches the **exact string** `abc`.

#### Special Characters

- `.` matches for any character.
- `\` matches the following special character literally. `\*` matches the literal `*`.
- `\d` matches any single digit. It is equivalent to `[0-9]`.
- `\w` matches any letter, digit or underscore character.
- `\s` matches any space character.

### Text matching examples

| Target Strings | Regex Pattern | 
| -------------- | ------------- |
| codes contain any capital latter | `[A-Z]` |
| codes with only capital letters | `^[A-Z]*$` |
| codes with only capital letters, or only with lowercase letters | `^([A-Z]*\|[a-z]*)$` |
| 10 characters codes, with capital and lowercase letters only | `^[A-Za-z]{10}$` |
| 5-10 characters codes, with capital and small letters only | `^[A-Za-z]{5,10}$` |
| messages, 250 characters max | `^.{0,250}$` |
| Canadian postal codes (`A1A 1A1`) | `^[A-Z][0-9][A-Z]\s[0-9][A-Z][0-9]$` |

### Numeric matching examples:

In OCA, we also use regex to deal with numeric attributes. However, regex does not understand numbers; it only matches them as characters. E.g. if we want an integer within the range $[10, 30]$, we actually use pattern `^([1-2][0-9])|(20)$` to match "character `1` or `2` followed by any digit; or characters `30`". It may be tricky to deal with complicated numeric conditions.

| Target Strings | Regex Pattern | 
| -------------- | ------------- |
| any string starts with a digit `0-5` | `^[0-5]` |
| integer numbers between 1 and 50 | `^([1-9]\|[1-4][0-9]\|50)$` |
| integer numbers between -50 and 50 | `^-?([0-9]\|[1-4][0-9]\|50)$` |
| any integer or decimal number, may begin with `+` or `-` | `^[-+]?\d*\.?\d+$` |
| decimal numbers between 0 and 1, inclusive | `^\+?((0?\.\d+)\|(1(\.0+)?))$` |
| decimal numbers between -90 and 90, inclusive | `^[-+]?(90(\.0+)?\|[1-8]?\d?(\.\d+)?)$` |
| decimal numbers between -180 and 180, inclusive | `^[-+]?(180(\.0+)?\|((1[0-7]\d)\|([1-9]?\d?))(\.\d+)?)$` |
| latitude and longitude (combination of the two above, separated with a single comma and space) | `^[-+]?(90(\.0+)?\|[1-8]?\d?(\.\d+)?),\s*[-+]?(180(\.0+)?\|((1[0-7]\d)\|([1-9]?\d?))(\.\d+)?)$` |

### Testing Regex

A useful website for testing regular expressions is [Regular Expressions 101](https://regex101.com/). You could input any regex and type a series of test strings, then any matches found will be marked out. 

![regular expressions 101](/pictures/regex101_tester.PNG)

If this is not done by default, please remember to check the regex flags `g` and `m` for easier testing.

![regular expressions 101 flags](/pictures/regex101_flags.PNG)

## MIME Types

MIME tutorials and examples here

## ISO 8601

ISO 8601 DateTime tutorials and examples here

