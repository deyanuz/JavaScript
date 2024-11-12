
# Regular Expressions in JavaScript 🔍

Regular expressions (RegEx) are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. Regex enables tasks such as validation, replacement, and parsing in a streamlined way. 

## Basics of Regex Syntax

In JavaScript, regular expressions are created using either **regex literals** or the **RegExp constructor**.

### *Regex Literals*

```javascript
const regex = /pattern/flags;
```

### *RegExp Constructor*

```javascript
const regex = new RegExp("pattern", "flags");
```

## Common Flags in Regex

Flags modify the behavior of the regular expression:
- **g** — Global search (find all matches).
- **i** — Case-insensitive search.
- **m** — Multi-line search.
- **s** — Dot (`.`) matches newlines.
- **u** — Unicode support.
- **y** — Sticky search (matches from the current position).

```javascript
const regex = /hello/gi; // Case-insensitive and global search
```

## Pattern Syntax

| Syntax  | Description                                    | Example                  |
|---------|------------------------------------------------|--------------------------|
| `.`     | Any character except newline                   | `/h.t/` matches `hat`, `hit` |
| `\d`    | Digit (0-9)                                    | `/\d+/` matches `123`     |
| `\w`    | Word character (alphanumeric + underscore)     | `/\w+/` matches `hello`   |
| `\s`    | Whitespace                                     | `/\s+/` matches spaces    |
| ``    | Word boundary                                  | `/word/` matches `word` |
| `^`     | Start of input                                 | `/^hello/` matches `hello` at the start |
| `$`     | End of input                                   | `/world$/` matches `world` at the end   |

Use **quantifiers** to specify how many times a pattern should match:
- `*` — Zero or more times
- `+` — One or more times
- `?` — Zero or one time
- `{n}` — Exactly n times
- `{n,}` — At least n times
- `{n,m}` — Between n and m times

## Basic Regex Operations

### *Testing a Pattern*


Use `.test()` to check if a pattern is found in a string:
```javascript
const pattern = /\d+/;
console.log(pattern.test("123")); // Output: true
console.log(pattern.test("abc")); // Output: false
```

### *Extracting Matches*


Use `.match()` to retrieve matches:
```javascript
const text = "I have 2 cats and 3 dogs";
const matches = text.match(/\d+/g); // Output: ["2", "3"]
```

### *Replacing Text*


Use `.replace()` to replace text matching a pattern:
```javascript
const text = "Hello world";
const result = text.replace(/world/, "JavaScript"); // "Hello JavaScript"
```

## Resources

- [JavaScript Regular Expressions Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

---
