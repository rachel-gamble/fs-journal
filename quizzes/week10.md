# C# Fundamentals


**1.** What is the purpose of a `namespace`?
<!-- enter you answer in the space below -->
```
a namespace declares region that provides a scope to the project's identifiers (the names of types, functions, variables, ect) inside it. They're used to organize code into logical groups, and as I learned this week, avoid name collisions - I'm guessing especially when your code base gets bigger and has multiple libraries.

```
**2.** What is the difference between a `class` and a `struct`?
<!-- enter you answer in the space below -->
```
The main difference between a class and a struct in C#, is that a struct is a value type and a class is a reference type.
```

**3.** What is the method that returns an instance of a class, yet it has no return type?
<!-- enter you answer in the space below -->
```
A constructor
```
## Example 1
```c#
abstract class Car
{
  ...
  public virtual string Start()
  {
    return "Vroooom";
  }
}
```
**5.** In the example what is the access modifier of the `Start()` method?
<!-- enter you answer in the space below -->
```
Public; it says right there. 
```
**6.** In the example what is `string` an indication of?
<!-- enter you answer in the space below -->
```
'String' is the return type of the method Start(). It indicates that when the method is called, it will return a value of type string.
```
**7.** In the example what is `abstract` preventing?
<!-- enter you answer in the space below -->
```
The abstract keyword is indicating that the method is incomplete and must be implemented by a derived class; it cannot creat ean object of the class, it can only be inherited by a derived class.
So in this case, the 'abstract' is preventing the creation of an instance of the class 'Car'. It's just a blueprint for other classes.

```
**8.** In the example what is the purpose of `virtual`?
<!-- enter you answer in the space below -->
```
It's being used to indicate that the method can be overridden by derived classes.

```
**9.** Name four access modifiers:
<!-- enter you answer in the space below -->
```
Public
Private
Protected
Internal

```
**10.** If you set a class or method to private, what can access it?
<!-- enter you answer in the space below -->
```
A private method can only be accessed from within the same class or struct in which it is declared. A "private member" is not accessible from outside. Not even from the same namespace; only by code within the same class or struct.

Note: it's useful for access restriction for hiding information ect.

Though I did read that in C#, if a class or method is private, it can be accessed by other classes, structs or methods within the same assembly, but not by other assemblies or by external code.

```