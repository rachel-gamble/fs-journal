# Intro to JavaScript

**1.** Which keywords are used to declare a variable in JavaScript?
<!-- enter you answer in the space below -->
```
var
let
const

```
**2.** What is the definition of a function?
<!-- enter you answer in the space below -->
```
function name(parameters){
  //statements
}

A Function is a declaration, of sorts. I kind of think of them as actions. Var/let/const define the objects and information that I manipulate with a function. (That's how it works in my brain, anyways; it's working for me so far). You evoke functions you write to "do" various things, or manipulate things in a declared fashion. This isn't technically right, but it's how I've made sense of it this week.

The real definition:
A function is a subprogram designed to perform a particular task.
Functions are executed when they are called. This is known as invoking a function.
Values can be passed into functions and used within the function.
Functions always return a value. In JavaScript, if no return value is specified, the function will return undefined.
Functions are objects.

```
**3.** What are the `SOLID` principles?
<!-- enter you answer in the space below -->
```

I had to google this, I couldn't find it in our notes, but according to multiple google searches: 

S: Single Responsibility Principle.
O: Open-Closed Principle.
L: Liskov-Substitution Principle.
I: Interface Segregation Principle.
D: Dependency Inversion Principle.

```
**4.** Given this array: 
```js
let fruit = ['apple', 'banana', 'pineapple',  'orange', 'strawberry']
``` 
What index is the pineapple's current position? How do you know?
<!-- enter you answer in the space below -->
```
I think it's 2... I believe it goes 0. apple 1. banana 3. pineapple

I guess I'm not solid on the answer to this question. I plan to do a lot more studying this week so hopefully I will figure it out for sure.

```
**5.** With these two objects: 
```js
let you = { name:"You", hair: true, friends: [] }
let them = { name:"Them", hair: false, friends: [] }
```
how would you .push the `them` object into the `you` object's array of friends?
<!-- enter you answer in the space below -->
```
let (you.friends += them)

Idk I'm probably wrong. I need tutoring with arrays, and so far my method of figuring out JavaScript is to try different code phrasing until something finally works. I have little idea what I'm doing! But to be honest, this last homework challenge did teach me a lot.
```

**6.** Give an example of a JavaScript `Conditional`:
<!-- enter you answer in the space below -->
```
if (gold >= flower.cost) {
  flowers.quantity++
  gold -= flowers.cost
} else {
  console.log("not enough gold")
}

```
**7.** In the `for loop` below, what is the name of the piece belongs inside the empty "______" space? What would you put here to increase `i` by one on every iteration?
```js
for ( let i = 0; i < arr.length; _______ ) {
  //...
```
expression 3
you would put i++ to increase i by one. or, 
for ( let i = 0; i < arr.length; i++ ) {
```

```
**8.** What does the `DOM` acronym stand for? Which file is first accessed to render the `DOM`?
<!-- enter you answer in the space below -->
```
Document
Object
Model

I think it first accesses the HTML index, and then makes a family tree to follow. That's why we have to link our javascript and css to the html.

```

**9.** What are the `9` ECMAScript types as defined by MDN?
<!-- enter you answer in the space below -->
```
My brain might be fried, but I cannot find this answer literally anywhere. I don't know if '9' is wrong and meant to be 6, because I found nothing. I searched MDN's site, all our notes, using ctl+f search, nothing. 
```
**10.** When it comes to functions or methods, what is the difference between a `parameter` and an `argument`?
<!-- enter you answer in the space below -->
```
Parameters are names listed in a function's definition, while arguments are the real values passed to the function.

So parameters are values that are defined when a function is declared, while arguments are values declared within a function when it is called.

Names vs values, kind of.
```
**11.** What is the difference between a `primitive` value and a `reference` value?
<!-- enter you answer in the space below -->
```
Primitive values are numbers, strings, boolean, undefined, null, or a symbol.

Reference values are anything else; or a reference value that refers to objects.

```