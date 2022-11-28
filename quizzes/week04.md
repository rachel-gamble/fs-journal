# UnderStanding Asynchronous Code, and API's

**1.** What is the difference between `asynchronous` code and `synchronous` code?
<!-- enter you answer in the space below -->
```
Synchronous code must occur in a linear manner, like function A goes before function B before function C. It is dependent on the block of code it's connected to.
Asynchronous code allows an application to continue running without pausing. Functions can occur before, during, or after other functions. Processes can run simultaneously and do not need to wait until other processes finish to run.
```


**2.** What is an event listener?
<!-- enter you answer in the space below -->
```
An event lister lives in the Controller constructor (which runs on page load) and "listens" to its assignment, waiting for an event to occur. Any time something changes in the DOM or the event occurs that the listener is waiting for, the event listener fires off a function.

A common example is a user clicking the mouse on a button.
```


**3.** What does the `O` represent in the `SOLID` principles?
<!-- enter you answer in the space below -->
```
Open-closed Principle
```


**4.** What is a callback / higher order function?
<!-- enter you answer in the space below -->
```
Callbacks are functions passed as parameters to be called at a later time. They typically run after another function is finished. They make sure that one section of code doesn't execute until another code has finished; but they can lead to callback hell.

```


**5.** What is a `promise`? How do you capture an error from a `promise`?
<!-- enter you answer in the space below -->
```
A promise allows asynchronous methods to return values like synchronous methods; it keeps the program running (rather than pausing and waiting for a return) and promises, "when this is done, I want you to perform this action on success or this action on failure."
The three states are:
pending - promise started, not finished
fulfilled - promised completed successfully
rejected - promise has failed
The  class constructor takes in a callback, and either runs a resolve or reject. It is fulfilled with a value,  and rejected with an error.
A '.catch' method is used to "catch" errors if the promise is rejected. You run that with a '.then' and '.catch' code.


```
**6.** Name three processes used to make requests over `HTTP`?
<!-- enter you answer in the space below -->
```
Get, Post, Put
```


**7.** What does the `API` acronym stand for?
<!-- enter you answer in the space below -->
```
Application Programming Interface 

```


**8.** In the `MVC` design pattern, who is responsible for making calls to `APIs`?
<!-- enter you answer in the space below -->
```
The Service!
```


**9.** What is the purpose of encapsulation in programming?
<!-- enter you answer in the space below -->
```
To restrict direct access to some components of an object, usually from a user.
```


**10.** What is `HTTP` response code for a successful request?
<!-- enter you answer in the space below -->
```
Successful responses are between 200-299 :)
```


**11.** What is a 500 error?
<!-- enter you answer in the space below -->
```
Internal Server Error. Bummer, man!

Other 500 errors are also some type of server or network error; and the code doesn't know how to handle it.

```