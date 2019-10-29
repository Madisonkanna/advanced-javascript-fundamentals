# Advanced JavaScript Fundamentals

## 3. Coercion

[Exercises from lesson 3](https://github.com/twclark0/advanced-javascript-fundamentals/tree/master/lesson-3)

 Coercion is one type to another type. It is when you change types from primitive to primitive or when you change types from object to primitive.

You actually rely on coercion for so much of what you do every day. To understand your code, you have to interpret code like JS.

## Impliciic coercion.

Implicit coercion is a way to abstract those lower details to provide more focus for the developer. For example the double equals. Are the explicit coercions distracting to the reader? 

Example: 

```javascript
const someNumber = 2
const str = `Hello, I have ${someNumber} eyes`
```

**What will JS do here?**

First JS calls the ```.valueOffunction``` to determine the primitive value. Our JS engine would know someNumber is a number. Then it sees that const str = is a string and it converts someNumber into a string. The valueOf function gets called to determine values. It will coerce the type into a similar type to complete the operation.

Overload operators like '+' do implicit coercion.
Truthy and false checks do implicit coercion.

If you want to avoid coercion at any cost, then you’re missing one of the most powerful things about JS. 

## Explicit coercion

```Javascript
String(val) //explict coercion into a string
```

Some objects have a toString() and that coerces it into a string. Implicitly the ‘+’ asks it to coerce for us.

Example of both an implicit and explicit coercion:
```javascript
const num = (1).toString()
```

Here JS first coerces this primitive type into an object. Then we call the object’s toString prototype method to coerce it into a string. 


### to-boolean
With any of these 7, you will get Falsy:

```javascript
"", 0, -0, null, NaN, false, undefined
```

Keep in mind the rules and the situations where things behave differently than you'd think. - not as many gotchas that jump at you unless you’re trying to explicitly coerce.





