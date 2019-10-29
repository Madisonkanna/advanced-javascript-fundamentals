# Advanced JavaScript Fundamentals

## 2. Prototypes

[Lesson 2 instructor notes](https://github.com/twclark0/advanced-javascript-fundamentals/tree/master/lesson-2)

**What are prototypes?**

- Fundamentally how inheritance works in JS.
- Prototypes are the linkeage between objects through properties, called the prototype chain.
- Prototypes are objects and link objects. You can think of it like the nesting of objects. The way they’re all connected to each other is through this linkeage.

If you type {} in your console, you can see we have nothing in our object. However, we do have ``` _proto_ : Object``` 

Any time we create a new data type, they’re automatically given this proto. This is referred to as “_proto.” If we open this up in our console, we can see we have all of these methods. 

An object can be automatically connected to another object. This key has the value of an object with many methods. There is no limit of chaining. We can have one object or six. This is how data types are able to inherit from each other. It’s automatically added to any syntax we use. 


## Connections between ‘.prototype’ and ‘__proto__’

Any time we create a function, every single function is created with a dot prototype that is an object.  
- Functions have a `.prototype` property that points to an object with a constructor property, and a `__proto__` property.


## Understanding the ‘new’ keyword
The 'new' keyword has 3 main things it is doing, and a fourth one not used often:

1. Creates a brand new object instance. 
2. It connects the brand new object's _proto to function's .prototype.
3. The ```this``` keyword within called function points to the new object created.
4. It returns ‘this’, the new object.

### Loops with prototypes

- Loop behavior changes if objects have chained prototype objects.
- The for in statement iterates over all non-symbol, enumerable properties of an object. 

setPrototpye of and the 'new' keyword are ways we can change what the _proto_ is. The 'new' keyword changes it to whatever function it was called on. There’s also setPrototypeOf where we say the next in line _proto_ object is the second arg. 

### Object.create

Object.create creates an object and gives the ability to point another object to the new object’s prototype. Object.create is a third way we can connect prototypes between objects. 

When using prototypes, favor Object.create as opposed to the new keyword.
If you do want to mess around with prototypes, favor Object.create.


## Additional notes/resources:

- Whenever you see a new Ecmascript release that says “added to the prototype” that means you don’t have to reference the global constructor function to utilize this. That means that you can just dot onto it from the instance if its a prototype method.

- You can ad methods to the global object prototype, for example:

```javascript
Object.prototype.findName = function()
```

You could do this, and every new object literal that you create inside of your code would have access to this function. Throughout your code, all your objects would have access to this function. But it’s not good to do this because you could be causing a big performance problem. Secondly, with a new release of JS, they could add a new prototype method that has the same name and yours would be overridden. 