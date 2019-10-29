# Advanced JavaScript Fundamentals

## 1. Primitive types

[Lesson 1 instructor notes](https://github.com/twclark0/advanced-javascript-fundamentals/tree/master/lesson-1)

Before we talk about primitive types, first what is a type?

Types are ways of organizing data that has similar values. When you give something a type, it is easier to know how to handle what you are working with. For example, it’s easier to know what to do with an array once you know it **is** an array.

Primitive types are data that is 1) not an object and 2) has no methods and 3) cannot be mutated. 

We hear people say “Everything in JS is an object!” and you can see where that comes from as we go through this workshop, but this isn’t actually true. Objects are not primitive types. 

With Ecmascript there are 7 primitive types: 

**string, number, bigint, boolean, null, undefined, and symbol**

Data types are different. These are collections of data such as objects. 

Primitive types, when they’re passed as params to functions, are passed by value and not by memory.

So if we were to pass by string, we pass its primitive type value to the function. We are not mutating this top level variable. 

## Wrapper objects

Auto-boxing is when you try to replicate object behavior. JS behind the scenes boxes that primitive type into an object so you can then dot into it. 

Primitive wrapper objects in JavaScript	 (Natives, Constructors, Fundamental Object) 

So here we have:

```javascript 
const str = ‘foo’
console.log(typeof str)
console.log(str.length)

const wrapperString = new String(‘foo’);
console.log(typeof wrapperString) //object

//this is now an object
console.log(wrapperString) // String ‘foo’ {  [Iterator] 0: ‘f’ 1: ‘0’ 2: ‘0’}
```

Why does this happen? It happens because of auto-boxing in JS. So if we create a var of new String(‘foo’) like we did, and we just do that, auto boxing will happen. 

## Additional resources/notes:

In your browser if you run

```Javascript
typeof null
```

This returns an object. 

 This is a bug in JS dating to when JS was first written. Null was initially written to be an object to represent nothing or zero, and it’s kind of just stuck with the language. It’s not actually an object, it is its own primitive type. 
 
 An article I found on more about typeof null and confusing types:

 [Article: "What's the typeof null?", and other confusing JavaScript Types](https://bitsofco.de/javascript-typeof/) 