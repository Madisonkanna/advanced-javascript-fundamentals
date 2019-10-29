# Advanced JavaScript Fundamentals

## 6. ES6 Classes

[Lesson 6 instructor notes](https://github.com/twclark0/advanced-javascript-fundamentals/tree/master/lesson-6))

- Sugar over functions and the prototype chain
- While ES6 Classes arae syntactic sugar, they also also have their own things that only exist with classes.
-Classes are not hoisted, unlike functions which are. 
-Has many keywords specific to ‘class’, but it is still just sugar.

### ‘extends’ 

- Subclasses custom classes and built-in objects.

- Equivalent of using ```Object.setPrototypeOf``` with two functions before new keyword. Example:

```javascript
class Square extends Rectangle {}

Object.getPrototypeOf(Square) // class Rectangle {}
```

### Constructor
 - Special method on a class. It is what is called when you new up a class. 
 - One ```constructor``` per class. 

### Static

- Used to set the property to the class itself. 
- Will not go onto the ```.prototype``` property
- Should not be called on instances of class

### Super keyword

Super is a way of accessing methods whether static or constructor.. super gives us access to anything on the parent class. Your child class has to call ‘super’ before it uses ‘this.`

The ```new``` keyword goes through classes on extends and looks at constructors. To complete the chain, ```super``` is required in children constructors. Must call super on child classes.

## Additional notes/resources:

- Things have been built around ES6 classes to make classes work like how they would in classical languages.

- When we create classes in react we are extending react.component. It was a child class of another class and it had a constructor, which means we need to use Super. 