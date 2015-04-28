---
layout: default
tags:
- javascript
---

As you may have gathered from other parts of my website, I am a software developer. I'm pretty junior at the moment and working hard on one day not being so junior. Although I have been programming off and on for nearly half my life, I never did web development professionally until about a year and a half ago. Most of my other programming experience was very data-oriented and mainly served to accomplish discrete tasks such as collect behavioral data, explore data, analyze data, visualize data... you get the picture. So far I love being a developer - it fits my preferred style of working quite well. It's challenging, there's always a puzzle to figure out, most work is done independently but collaboration underlies everything, and it requires a lot of creativity. Pretty much everything I work on involves learning something new. It can be quite slow, especially if I go about it the right way and do a ton of reading before committing any code. But it's worth it because I get bored easily if I'm not learning every day.

I much prefer doing back-end vs. front-end coding, but this year I've decided it's about damn time I become a true full-stack developer. What I mean is that I need to become fluent in the language of the web browser: JavaScript. I first touched JS during my first semester at college in some introduction to computers class. I didn't really get it but I did enough to make it seem like I got it. Fast-forward 15 years, and, although I use it almost every day (in the form of [Coffeescript](http://coffeescript.org/) and [jQuery](https://jquery.com/)), I actually still don't really get JS itself. This brings me to the topic of this post.

Two weeks ago I started reading [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742) by Douglas Crockford. (No, scratch that, I started reading this book about a year ago on my kindle. I don't know why I thought it would be a good idea, but I just can't grok programming books on a kindle.) I finished reading it today and, suffice it to say, I still don't really get JS. But! I know there is a ton of other reading I need to do, and the thing about real paper books is I can go back and read my notes in the margins and keep building on my knowledge. One day I will get it.

The purpose of this post (or should I say series of posts?) is to keep me accountable for what I just read. It's not necessarily going to be a summary, but rather, things that stuck out to me, or things that I don't understand, or things that I should probably try hard to remember. If anyone ever reads this and gets anything out of it, bonus.

### Chapter 1: Good Parts

Here we learn that JavaScript has some flaws. There are a lot of bad parts. This book, appropriately enough, focuses on the good parts and points out stuff to avoid. It drives home the fact that JS is THE language of the web and is one of the most popular languages in the world. (I've known JS is the language of the web browser for a long time, but I suppose I often thought of it as kind of, well, optional. Like, do we really need animations and goofy stuff on our static webpages? But I just wasn't thinking big enough, and my head was still stuck in the 90s.)

JS is built on some good ideas:

- **functions**
- [**loose typing**](http://en.wikipedia.org/wiki/Strong_and_weak_typing) - variables are declared without a type (as opposed to strong typing)
- **dynamic objects** - objects can change throughout the execution of the script (as opposed to static objects)
- expressive **object literal notation** - objects can be created simply by listing their components
- **prototypal inheritance** - objects inherit properties directly from other objects

JS is also built on some bad ideas:

- **global variables** - all top-level variables of all compilation units are tossed together in a common namespace called the global object. This is evil.

Here are some awesome quotes: 

"...it is one of the most despised programming languages in the world. The API of the browser, the Document Object Model (DOM) is quite awful..."

"If you want to learn more about the bad parts and how to use them badly, consult any other JavaScript book."

"'Why should I use JavaScript?' There are two answers. The first is that you don't have a choice...The other answer is that, despite its deficiencies, *JavaScript is really good*."

### Chapter 2: Grammar

This chapter introduces the amazing railroad diagram to visualize the grammar of the good parts of JS. Not much else to say here.

<img src="http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad41.png">

<hr>

Well I think that's it for today. I'm up past my bedtime and I still have to go watch Game of Thrones! I'll come back and fill in my notes for the 8 remaining chapters, although I will say the bulk of the book (and the most difficult for me to understand) is contained in Chapters 3, 4 and 5, which cover objects, functions and inheritance. Until then!
