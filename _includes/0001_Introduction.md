## 1.1. What is this?

This document attempts to provide guidelines (or coding standards if you like) that are both valuable and pragmatic. 

## 1.2. Why would you use this document?

Although some might see coding guidelines as undesired overhead or something that limits creativity, this approach has already proven its value for many years. This is because not every developer:

- is aware that code is generally read 10 times more than it is changed;
- is aware of the potential pitfalls of certain constructs in C#;
- is up to speed on certain conventions when using the .NET Framework such as `IDisposable`, `async`/`await`, or the deferred execution nature of LINQ;
- is aware of the impact of using (or neglecting to use) particular solutions on aspects like security, performance, multi-language support, etc;
- realizes that not every developer is as capable, skilled or experienced to understand elegant, but potentially very abstract solutions;

## 1.3. Basic principles

- The Principle of Least Surprise (or Astonishment): you should choose a solution that everyone can understand, and that keeps them on the right track.
- Keep It Simple Stupid (a.k.a. KISS): the simplest solution is more than sufficient.
- You Ain't Gonna Need It (a.k.a. YAGNI): create a solution for the problem at hand, not for the ones you think may happen later on. Can you predict the future?
- Don't Repeat Yourself (a.k.a. DRY): avoid duplication within a component or a source control repository without forgetting the [Rule of Three](http://lostechies.com/derickbailey/2012/10/31/abstraction-the-rule-of-three/) heuristic.
- The [four principles of object-oriented programming](https://github.com/TelerikAcademy/Object-Oriented-Programming/tree/master/Topics/04.%20OOP-Principles-Part-1): encapsulation, abstraction, inheritance and polymorphism.
- In general, generated code should not need to comply with coding guidelines. However, if it is possible to modify the templates used for generation, try to make them generate code that complies as much as possible.

Regardless of the elegance of someone's solution, if it's too complex for the ordinary developer, exposes unusual behavior, or tries to solve many possible future issues, it is very likely the wrong solution and needs redesign. 

## 1.4 Original Version
The author of the original repository can be found here: https://github.com/dennisdoomen/CSharpGuidelines/
