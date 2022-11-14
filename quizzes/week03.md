# Application Architecture, MVC Design Pattern

**1.** What are the Pillars of Object Oriented Programming (`OOP`)?
<!-- enter you answer in the space below -->
```
Encapsulation, inheritance, and polymorphism.
```
**2.** How would you access the `name` of the below object using the `property` variable?
```js
let staff = {
  name: "Tim",
  age: 26,
  job: "Code Monkey"
  }
let property = 'name'
```
staff.name

```

```
**3.** What is Encapsulation?
<!-- enter you answer in the space below -->
```
The bundling of data with the methods that operate on that data. Also, restricts direct access to some of an object's components.
It hides the values or state of a object in a class. It helps people/users not mess with important features of the app.

```
**4.** What does the S stand for in the `SOLID` principles?
<!-- enter you answer in the space below -->
```
Single-responsibility principle. 

```
**5.** What the difference between a `class` and an instance of a `class`?
<!-- enter you answer in the space below -->
```
Class describes a data type. 
An instance of a class is an object of the data type that exists in memory.

```
**6.** What is a `Proxy` object?
<!-- enter you answer in the space below -->
```
An object in javascript that wraps an object or a function and monitors it via something called target.

```

**7.** What is the purpose of the `MVC` pattern?
<!-- enter you answer in the space below -->
```
It implements user interfaces, data, and controlling logic while seperating the app or software's business logic and display.

```
**8.** What is the job of the `Controller` in the `MVC` Pattern?
<!-- enter you answer in the space below -->
```
The controller controls the way that a user interacts with an application. 

```

**9.** What is the job of the `Service` in `MVC`?
<!-- enter you answer in the space below -->
```
It is kind of where the actions happens in the software (that helps me understand it a bit, at least). It's protected from the user, and the controller talks to it between the user and the service.
It contains the logic.

```
**10.** What is the job of the `Model` in `MVC`?
<!-- enter you answer in the space below -->
```
The model stores the core information that the application uses to access and manipulate. 
Often templates go there, and arrays.

```
