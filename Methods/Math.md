## Math in JavaScript 🔢

The `Math` object provides mathematical constants and functions. It has no constructor and is used directly. It works with the `Number` type. It doesn't work with `BigInt`.

### _Common Math Methods_

- **Math.round / Math.ceil / Math.floor :** Rounds a number to the nearest integer.

```javascript
console.log(Math.round(4.6)); // Output: 5
console.log(Math.ceil(4.2)); // Output: 5
console.log(Math.floor(4.8)); // Output: 4
```

`Math.round` rounds to the nearest integer, `Math.ceil` rounds up, and `Math.floor` rounds down.

### _Mathematical Constants_

- **Math.PI / Math.E :** Constants representing π and Euler's number.

```javascript
console.log(Math.PI); // Output: 3.141592653589793
console.log(Math.E); // Output: 2.718281828459045
```

Use `Math.PI` for calculations involving circles and `Math.E` for exponential calculations.

### _Other Math Methods_

- **Math.max / Math.min :** Returns the largest or smallest number from a set.
- **Math.random :** Generates a random number between 0 (inclusive) and 1 (exclusive).
- **Math.abs :** Returns the absolute value of a number..

```javascript
console.log(Math.max(1, 3, 2)); // Output: 3
console.log(Math.min(1, 3, 2)); // Output: 1
console.log(Math.abs(-20)); // Output: 20

let numbers = [10, 2, 30, 1];
console.log(Math.max(...numbers)); // Output: 30

console.log(Math.random()); // Output: Random number (e.g., 0.235)
```

In the third code snippet, the `...` is used to spread its elements as individual arguments.

### _Logarithmic Functions_

- **Math.log / Math.log10 / Math.log2 :** Compute the natural logarithm, base-10 logarithm, and base-2 logarithm of a number.

```javascript
console.log(Math.log(1)); // Output: 0 (natural logarithm of 1)
console.log(Math.log10(100)); // Output: 2 (log base 10 of 100)
console.log(Math.log2(8)); // Output: 3 (log base 2 of 8)
```

### _Trigonometric Functions_

- **Math.sin / Math.cos / Math.tan :** Compute the sine, cosine, and tangent of an angle (in radians).

```javascript
console.log(Math.sin(Math.PI / 2)); // Output: 1 (sine of 90 degrees)
console.log(Math.cos(0)); // Output: 1 (cosine of 0 degrees)
console.log(Math.tan(Math.PI / 4)); // Output: 1 (tangent of 45 degrees)
```

### _Hyperbolic Functions_

- **Math.sinh / Math.cosh / Math.tanh :** Compute the hyperbolic sine, cosine, and tangent of a number.

```javascript
console.log(Math.sinh(1)); // Output: 1.1752011936438014
console.log(Math.cosh(0)); // Output: 1
console.log(Math.tanh(1)); // Output: 0.7615941559557649
```

## Resources

- [JavaScript Math Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

---
