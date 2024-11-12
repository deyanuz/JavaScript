## Date in JavaScript 🗓️

JavaScript `Date` objects represent a specific moment in time as milliseconds since January 1, 1970, UTC. They provide a platform-independent way to handle date and time.

### Creating a Date

- **Syntax**: You can create a `Date` object using different constructors.

```javascript
const now = new Date(); // Current date and time
const specificDate = new Date(2024, 0, 1); // January 1, 2024 (month is 0-indexed)
const fromString = new Date("2024-11-03T12:00:00"); // Date from string
```

The `Date` object can represent the current time or specific dates. The month parameter is zero-based, so January is `0`.

### Getting Date Information

- **getFullYear / getMonth / getDate**: Methods to get specific parts of a date.

```javascript
const date = new Date(2024, 10, 3); // November 3, 2024
console.log(date.getFullYear()); // Output: 2024
console.log(date.getMonth()); // Output: 10 (November)
console.log(date.getDate()); // Output: 3
```

`getFullYear` returns the year, `getMonth` returns the zero-based month, and `getDate` returns the day of the month.

### Setting Date Information

- **setFullYear / setMonth / setDate**: Methods to set parts of a date.

```javascript
const date = new Date();
date.setFullYear(2025);
date.setMonth(5); // June (0-indexed)
date.setDate(15);
console.log(date); // Updated date: June 15, 2025
```

Use `setFullYear`, `setMonth`, and `setDate` to modify date values. These methods change the `Date` object in place.

## Date Methods: Local & UTC

| Component           | Get (Local)      | Set (Local)      | Get (UTC)        | Set (UTC)        |
|---------------------|------------------|------------------|------------------|------------------|
| Year                | getFullYear()    | setFullYear()    | getUTCFullYear() | setUTCFullYear() |
| Month               | getMonth()       | setMonth()       | getUTCMonth()    | setUTCMonth()    |
| Date (of month)     | getDate()        | setDate()        | getUTCDate()     | setUTCDate()     |
| Hours               | getHours()       | setHours()       | getUTCHours()    | setUTCHours()    |
| Minutes             | getMinutes()     | setMinutes()     | getUTCMinutes()  | setUTCMinutes()  |
| Seconds             | getSeconds()     | setSeconds()     | getUTCSeconds()  | setUTCSeconds()  |
| Milliseconds        | getMilliseconds()| setMilliseconds()| getUTCMilliseconds()| setUTCMilliseconds() |
| Day (of week)       | getDay()         | N/A              | getUTCDay()      | N/A              |

## Resources

- [JavaScript Date Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)

---
