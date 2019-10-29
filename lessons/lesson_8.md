# Advanced JavaScript Fundamentals

## 8. Strict mode

[Lesson 8](https://github.com/twclark0/advanced-javascript-fundamentals/blob/master/lesson-8/notes.md)

Strict mode intentionally has different semantics than normal code we're used to.

## Takeaways:

- `"use strict"` --the syntax for strict mode
- Catches silent errors and throws them
- Doesn't allow you to use certain syntax that could possibly be defined in future versions of ECMAScript. 
- es6 JS modules are automatically converted to strict mode
- If the 'this' keyword ever references the global object in browser, strict mode returns undefined.
- Doesn't allow global variables. For example:

```JavaScript 
name = ‘tyler’ // throws a reference error
```

