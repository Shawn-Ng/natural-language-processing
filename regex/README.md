# Regular expression
1. [Metacharacter](#)
2. [Character Escapes](#)
3. [Character Classes](#)

## 1. Metacharacter
| Mchar | Definition |
| --- | --- |
| `^` |	Start of a string. |
| `$` |	End of a string. |
| `.` |	Any character (except \n newline) |
| &#x7c; | Alternation. |
| `{...}` |	Explicit quantifier notation. |
| `[...]` |	Explicit set of characters to match. |
| `(...)` |	Logical grouping of part of an expression. |
| `*`	| 0 or more of previous expression.
| `+`	| 1 or more of previous expression.
| `?` |	0 or 1 of previous expression; also forces minimal matching when an expression might match several strings within a search string. |
| `\` |	Preceding one of the above, it makes it a literal instead of a special character. Preceding a special matching character, see below. |

## 2. Character Escapes
| Escaped Char | Description |
| --- | --- |
| `ordinary characters` | Characters other than .$^{[(\|)]}*+?\ match themselves. |
| `\a`	| Matches a bell (alarm) \u0007. |
| `\b`	| Matches a backspace \u0008 if in a []; otherwise matches a word boundary  (between \w and \W characters). |
| `\t`	| Matches a tab \u0009. |
| `\r`	| Matches a carriage return \u000D. |
| `\v`	| Matches a vertical tab \u000B. |
| `\f`	| Matches a form feed \u000C. |
| `\n`	| Matches a new line \u000A. |
| `\e`	| Matches an escape \u001B. |
| `\040`	| Matches an ASCII character as octal (up to three digits); numbers with  no leading zero are back references if they have only one digit or if they correspond to a capturing group number. (For more information, see Backreferences.) For example, the character \040 represents a space. |
| `\x20`	| Matches an ASCII character using hexadecimal representation (exactly two digits). |
| `\cC`	| Matches an ASCII control character; for example \cC is control-C. |
| `\u0020`	| Matches a Unicode character using a hexadecimal representation  (exactly four digits). |
| `\*` | When followed by a character that is not recognized as an escaped character, matches that character. For example, \* is the same as \x2A. |

## 3. Character Classes
| Char class | Description |
| --- | --- |
| `.`	| Matches any character except \n. If modified by the single line option, a period character matches any character. For more information, see Regular Expression Options. |
| `[aeiou]`	| Matches any single character included in the specified set of characters. |
| `[^aeiou]`	| Matches any single character not in the specified set of characters.
| `[0-9a-fA-F]` |	Use of a hyphen (–) allows specification of contiguous character ranges. |
| `\p{name}`	| Matches any character in the named character class specified by {name}. Supported names are Unicode groups and block ranges. For example, Ll, Nd, Z, IsGreek, IsBoxDrawing. |
| `\P{name}`	| Matches text not included in groups and block ranges specified in {name}. |
| `\w`	| Matches any word character. Equivalent to the Unicode character categories [\p{Ll}\p{Lu}\p{Lt}\p{Lo}\p{Nd}\p{Pc}]. If ECMAScript-compliant behavior is specified with the ECMAScript option, \w is equivalent to [a-zA-Z_0-9]. |
| `\W`	| Matches any nonword character. Equivalent to the Unicode categories [^\p{Ll}\p{Lu}\p{Lt}\p{Lo}\p{Nd}\p{Pc}]. If ECMAScript-compliant behavior is specified with the ECMAScript option, \W is equivalent to [^a-zA-Z_0-9]. |
| `\s`	| Matches any white-space character. Equivalent to the Unicode character categories [\f\n\r\t\v\x85\p{Z}]. If ECMAScript-compliant behavior is specified with the ECMAScript option, \s is equivalent to [ \f\n\r\t\v]. |
| `\S`	| Matches any non-white-space character. Equivalent to the Unicode character categories [^\f\n\r\t\v\x85\p{Z}]. If ECMAScript-compliant behavior is specified with the ECMAScript option, \S is equivalent to [^ \f\n\r\t\v]. |
| `\d`	| Matches any decimal digit. Equivalent to \p{Nd} for Unicode and [0-9] for non-Unicode, ECMAScript behavior. |
| `\D`	| Matches any nondigit. Equivalent to \P{Nd} for Unicode and [^0-9] for non-Unicode, ECMAScript behavior. |
