# Advanced JavaScript Fundamentals

## 5. Scope and hoisting

[Lesson 5 instructor notes](https://github.com/twclark0/advanced-javascript-fundamentals/tree/master/lesson-5)

### Lexical scope
- This is related to “author” time or “compile time” or “fixed." Not It decided on when or how the code is executed. 

## IIFE pattern
- Immediately invoked function
- Around scope it’s used to scope vars  and make private things private. Let and const will scope to all block but var doesn’t. Var scopes to functions.
- IIFFE does not put the function on the global space. The function lives only in that one expression and its gone once function is executed. 

## Block scoping 

- Defined with the open and closing: ```{}``` 
- It is not scoped until there is an assignment 
- Objects are not scoped 

## Var

- Before code is executed, var declarations are executed. Var scope = current execution context.
- Re-declaring var with no value will not lose initial value of that var
- Var delcaration = ```undefined``` and hoisted to the top of its execution context.
- With an assignment without a var statement, it goes on the global object
- Var will not respect block scope.
 
## Let

- Block scoped
- Will not create properties on the Window Object
- ```let``` is only utilized to value when the parser evaluates it. Let is not hoisted like vars are. It’s not hoisted to the top and its not given an undefined val at first

## Const

- Similar to ```let``` but val of a constant can't be changed. 
- Cannot do deep equals on object types. 

## Let and Const gotcha; Temporal dead zone 

- Const and let have no initial value hoisted to the top and depending on how you access them will give a reference error 

## Additional notes/ resources:

Many say make private which your scope cares about, make public what everyone cares about. 