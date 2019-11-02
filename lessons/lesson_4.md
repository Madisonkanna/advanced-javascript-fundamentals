# Advanced JavaScript Fundamentals

## 4. This

[Lesson 4 instructor notes](https://github.com/twclark0/advanced-javascript-fundamentals/blob/master/lesson-4/notes.md)

```This``` references the execution context of a function call. which is determined how the function was called and in non-strict mode, is always a reference to an object.

In interview questions, this has got to be the number one most asked question. Easy to get tripped up on. It’s not the same thing every time a function is called. It all depends on how it was written and more importantly it
s all about how a function was actually called.

## 3 main ways to invoke a function:

1) Opening clothsing parentheses ```()```
2) Individually (implicit binding)
3) Methods like ```call``` or the ```new``` keyword

### Implicit binding - ‘this keyword’

Option 1) Context object: when you write a function on an object, you probably intend ‘this’ to reference the object that that function lives on.

```const person = {
  firstName: 'tyler',
  getName() {
    return `${this.firstName} is my first name`
  }
}

person.getName() // 'tyler is my first name'
```

What would happen if we called getName() with nothing to the left of it?

- Default binding, where ‘this’ defaults to the global. Behaves differs depending on if you’re in strict mode or non strict mode. Whenever you define functions they get automatically added to the global object. So this function now lives on the window and window is the context. 

### Explicit binding 

-  ```apply, call and bind``` take parameter which assigns the ```this``` context explcitly.

```new``` keyword does 3 main things: 
1) Creates a new object
2) points ‘this’ to new object, links ‘prototype’ to new object ‘_proto_’
3) returns ‘this’ which is that new object

### Arrow functions 
- Arrow functions have no concept of ‘this’. Arrow functions treats ```this``` like a normal variable. It will try to look up its scope to figure out what this is. It will lexically resolve to the enclosing scope for a ```this.```
- Big difference with arrow functions is that its the only time we need to know how the function was written. 
- Contrary to what we often think, arrow functions don't solve everything

### Arrow function gotchas: 
-Cannot self reference with recursion. 
-Anonymous unless assigned to a var
-Cannot be used with the ```new``` keyword
- ```call``` or ```apply``` first param for ```this``` is ignored.


