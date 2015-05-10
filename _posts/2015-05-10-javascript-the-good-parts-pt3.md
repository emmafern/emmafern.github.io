---
layout: default
tags:
- javascript
---

I had a bit of a hiatus due to being sick and binge-reading [Elfquest](http://elfquest.com/gallery/OnlineComics/digitalEQ.html) comics online last weekend. But I'm feeling more motivated today. Back to getting thoughts down on [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742). See my [first post]({% post_url 2015-04-26-javascript-the-good-parts-pt1 %}) in the series for the reason why I'm doing this.

### Chapter 4: Functions
Most of what I write here will be lifted verbatim from the book, just as a way for me to take notes/repeat what I've read several weeks ago at this point. Functions in JS are confusing to me because it seems like they appear everywhere and are used in so many different ways.

**Function objects** are linked to `Function.prototype`, which is linked to `Object.prototype`. Every function is created with two hidden properties: its context and the code that implements the function's behavior. Every function object is also created with a `prototype` property whose value is an object with a `constructor` propery whose value is the function.

(That last sentence doesn't make a whole lot of sense to me.)

Functions can be stored in variables, objects and arrays. They can be passed as arguments to functions, and functions can be returned from functions.

**Function Literals** have 4 parts: 1) reserved word `function`, 2) function's name, 3) a set of parameteters wrapped in parantheses, and 4) a set of statements wrapped in curly braces.

A function object created by a function literal contains a link to that outer context - this is **closure**.

**Invocation**. When invoked, functions also get two additional parameters. `this` and `arguments`. The value of `this` is determined by the invocation pattern. There are 4 types of invocation patterns: 1) method, 2) function, 3) constructor, and 4) apply.

>**Method Invocation** - when a function is stored as a property of an object. `this` is bound to that object.

>**Function Invocation** - when a funciton is not the property of an object. `this` is bound to the global object. This was a mistake because a method cannot employ an inner function to help it do is work because the inner funciton does not share the method's access to the object as its `this` is bound to the wrong value. The work around is `var that = this;`.

>**Constructor Invocation** - the function is invoked with the `new` prefix, and has a hidden link to the value of the function's `prototype` member, which is bound to `this`. Constructor names are always capitalized.

>**Apply Invocation** - `apply` lets us construct an array of arguments to use to invoke a function, and lets us choose the value of `this`.

**Arguments** gives the function access to all of its arguments that were supplied with the invokation. This means that you can write functions without specifying the number of parameters.

There are a whole bunch of other sections in this chapter, including discussions of **exceptions**, **augmenting types**, **recursion** (which will probably always confound me to some degree), **scope**, **closure**, **callbacks**, **modules**, **cascades**, **currying** (baffling! curry should only be something I eat) and **memoization**. However, for now I'm just focusing on the main topic, functions, and the other topics are good to come back to when needed.

A great resource I've been using a lot lately is [Code School](https://www.codeschool.com/). I did their **JavaScript Roadtrip** series. It's for beginners and it focuses on just a few aspects of JS. Although not comprehensive, doing the exercises after reading this chapter and then coming back to this chapter helped a lot.

Hopefully I can finish up a selection of the next several chapters in one fell swoop next time: Inheritance (Chapter 5), Methods (Chapter 8) and Style (Chapter 9).
