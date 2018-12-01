# Regular expression
1. [Special characters](#1-special-characters)
2. [Character Escapes](#2-character-escapes)
3. [Character Classes](#3-character-classes)
4. [Sets](#4-sets)

## 1. Special characters
| Mchar | Definition |
| --- | --- |
| `^` |	Start of a string |
| `$` |	End of a string |
| `.`   | Matches any character except `\n` newline |
| &#x7c; | Alternation |
| `*` | 0 or more of previous expression |
| `+` | 1 or more of previous expression |
| `?` | 0 or 1 of previous expression; also forces minimal matching when an expression might match several strings within a search string |
| `\` | Preceding one of the above, it makes it a literal instead of a special character |
| `{m,n}` | Matches the expression to its left `m` to `n` times, and not less |
| `{m,n}?` | Matches the expression to its left `m` times, and ignores `n` |

## 2. Character Escapes
| Escaped Char | Description |
| --- | --- |
| ordinary characters | Characters other than `.$^{[(\|)]}*+?\` match themselves |
| `\t` | Matches a tab |
| `\r` | Matches a carriage return |
| `\v` | Matches a vertical tab |
| `\f` | Matches a form feed |
| `\n` | Matches a new line |
| `\e` | Matches an escape |
| `\*` | When followed by a character that is not recognized as an escaped character, matches that character |

## 3. Character Classes
| Char class | Description |
| --- | --- |
| `\p{name}` | Matches any character in the named character class specified by {name} |
| `\P{name}` | Matches text not included in groups and block ranges specified in {name} |
| `\w` | Matches any word character. `\w` is equivalent to `[a-zA-Z_0-9]` |
| `\W` | Matches any nonword character. `\W` is equivalent to `[^a-zA-Z_0-9]` |
| `\s` | Matches any white-space character |
| `\S` | Matches any non-white-space character |
| `\d` | Matches any decimal digit |
| `\D` | Matches any nondigit |
| `\b` | Matches the boundary (or empty string) at the start and end of a word, that is between `\w` and `\W` |
| `\B` | Matches where `\b` doesn't, the boundary of `\w` characters |
| `\A` | Matches the expression to its right at the absolute start of a string |
| `\Z` | Matches the expression to its left at the absolute end of a string |

## 4. Sets
| Char class | Description |
| --- | --- |
| `.`   | Matches any character except `\n` |
| `[aeiou]` | Matches any single character included in the specified set of characters |
| `[^aeiou]` | Matches any single character not in the specified set of characters
| `[0-9a-fA-F]` | Use of a `-` allows specification of contiguous character ranges |
| `[-a]` |  Matches a or `-` |
| `[(+*)]` |  Matches `(`, `+`, `*` and `)` |

## 5. Groups
| Char class | Description |
| --- | --- |
| `(...)` | Logical grouping of part of an expression |
