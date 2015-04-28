---
layout: default
tags:
- javascript
---

Alright! I'm back to get down my thoughts on the remaining chapters of [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742). See my [previous post]({% post_url 2015-04-26-javascript-the-good-parts-pt1 %}) for the reason why I'm doing this, and the very brief recap of Chapters 1-2.

### Chapter 3: Objects

Most values in JS are objects (unless they are numbers, strings, booleans, null or undefined). Objects are simply containers of properties where each property has a name and a value. Objects look pretty much the same as JSON, although they aren't the same thing. (I didn't know this for sure until now when I looked it up.) In JSON the key has to be enclosed in double quotes whereas in JS objects the name does not need to be quoted unless it has a special character. JSON also cannot store functions, and dates are stored as strings. JSON is meant to be a kind of universal data exchange format that can be parsed and understood in the receiving language. 

**Object literals** are used to create new objects. They are just a pair of curly braces around name/value pairs. (Ok this is not new to me but I do need to remember the term "object literal" because it comes up a lot.) Retrieval of an object's value can either be done by using the name of the property in square brackets after the object (`object["name"]`) or using dot notation (`object.name`). That's nice.

**Prototypes** are a huge concept that I need to hammer into my skull. "Every object is linked to a prototype object from which it can inherit properties. All objects created from object literals are linked to `Object.prototype`." The way I've been thinking about them is as I think about classes in Ruby. It's just like how every object in Ruby is a descendant of the Object class. However, there is some confusing stuff about how when you create a new object you can select the object that should be its prototype. The book says the built in way is "messy and complex", and then goes on to define a whole new `create` method to the Object function so it can be done more easily as an example.

That's what's so frustrating about JS to me. It feels like a half-finished language and it's up to the programmer to define the basic functions that allow you to use it like any other fully fleshed out language. There are several other aspects of JS that are like this and I'll make a point of bringing them up when I come across them.

Another important point about prototypes is that if you add a new property to a prototype, that property will be immediately visible in all the objects based on that prototype. This also feels weird to me and will take some getting used to. To me it seems that if you create a new Object A based off Object X at time Y, then update Object X with a new property at time X + whatever, Object A should not be changed. But according to JS it would be.

**Reflection** - I hadn't heard this term used to refer to looking up what kind of an object something is. To do this you can either use `typeof` before the object value, or do `object.hasOwnProperty('number')` to ask an object whether it has a number (or any) property. The benefit of the latter is that it doesn't look along the prototype chain to all its ancestors if it doesn't have a particular property itself.

**Enumeration** - apparently you can loop over the properties of an object, which brings up the idea that you may want to skip over functions or other types of properties. You can also explicitly define a set of properties to loop over and just access them from the object one by one.

Lastly I just wanted to mention **Global Abatement**. I am reading over and over that one of the bad parts of JS is how easy it is to be lazy with global variables. One way to "abate" this badness is to create a single global variable for an application, which then becomes a container for all the other variables you may want to save globally. I do this myself at work so it's nice to see something familiar.

Chapter 4 is all about functions, and it's a big one (and the one I have the most trouble with) so I'll save it for next time.
