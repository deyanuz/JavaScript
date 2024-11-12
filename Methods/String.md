## String in JavaScript 📝

JavaScript `String` objects are used to store and manipulate text. They can contain letters, numbers, symbols, and even spaces. Strings are immutable, meaning their characters cannot be changed after creation, but you can create modified copies.

## Creating Strings

Strings can be created using single quotes (`'...'`), double quotes (`"..."`), or backticks (`\`...\`` for template literals).

```javascript
const singleQuoteString = 'Hello';
const doubleQuoteString = "World";
const templateLiteral = `Hello, ${singleQuoteString} ${doubleQuoteString}!`; // "Hello, Hello World!"
```

Template literals (backticks) allow for string interpolation using the `${}` syntax, making it easy to embed variables and expressions.

## Basic String Operations

- **<u>Accessing Characters</u> :** Use bracket notation or the `.charAt()` method to access characters in a string.

```javascript
const text = "Hello";
console.log(text[0]); // Output: H
console.log(text.charAt(1)); // Output: e
```

`text[0]` and `text.charAt(1)` retrieve specific characters from the string. Bracket notation is a modern, convenient way to access characters.

---

<br>

- **<u>Length Property</u> :** Use the `.length` property to get the number of characters in a string.

```javascript
console.log(text.length); // Output: 5
```

`text.length` returns the total count of characters, helpful for looping through or validating string content.

## String Methods

JavaScript provides a variety of methods for working with strings:

### _Finding and Extracting Substrings_

- **<u>indexOf</u> :** Returns the index of the first occurrence of a substring.
- **<u>slice</u> :** Extracts a section of the string from start to end (end not included).
- **<u>substring</u> :** Extracts characters between two indices. It's worth noting that `substring` does not accept negative indices, unlike slice.

```javascript
const text = "Hello, JavaScript!";
console.log(text.indexOf("JavaScript")); // Output: 7
console.log(text.slice(0, 5)); // Output: Hello
console.log(text.slice(-10)); // Output: "JavaScript!"
console.log(text.slice(-8, -1)); // Output: "Script"
console.log(text.substring(7, 17)); // Output: JavaScript
```

`indexOf` is used to find the position of a substring. `slice` and `substring` extract portions of the string; `slice` can take negative indices.

---

### _Modifying Strings_

- **<u>toUpperCase / toLowerCase</u> :** Converts the string to uppercase or lowercase.
- **<u>replace</u> :** Replaces part of a string with another string.
- **<u>trim</u> :** Removes whitespace from both ends of the string.

```javascript
const greeting = " Hello ";
console.log(greeting.trim()); // Output: "Hello"
console.log(greeting.replace("Hello", "Hi")); // Output: " Hi "
```

`trim` removes leading and trailing spaces, which is useful for cleaning input. `replace` swaps specified text with new text.

## Advanced String Manipulation

### _Template Literals_

Template literals allow for string interpolation and multiline strings, making it easier to embed expressions within strings.

```javascript
const name = "Alice";
const greeting = `Hello, ${name}! Welcome to JavaScript.`;
console.log(greeting); // Output: Hello, Alice! Welcome to JavaScript.
```

Template literals simplify embedding variables into strings and support multiline formatting, enhancing code readability.

## String Primitives vs String Objects

- **<u>String Primitive</u> :** Strings created using quotes (single or double) are primitives and have no methods until accessed.

- **<u>String Object</u> :** Created using the `String` constructor, it’s an object with built-in properties and methods.

```javascript
const primitive = "Hello"; // String primitive
const objectString = new String("Hello"); // String object

console.log(typeof primitive); // Output: string
console.log(typeof objectString); // Output: object
```

`typeof primitive` returns "string" because it's a basic data type. `objectString` is an object with additional features, but it's less commonly used.

## Resources

- [JavaScript String Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

<br>

---

---
