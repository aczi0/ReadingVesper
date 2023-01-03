---
title: Learning to code
date: 2020-10-22T08:26:10.000-04:00
tags:
- learning, computer science, web development, coding, programming
categories:
- Learning
keywords:
- learning, computer science, web development, coding, programming

---
If you've done a few computer science tutorials or bootcamp, you've probably heard of (or lived) *tutorial hell*, where each course you take seem to add something new but does not fill the gap between theory and application. I was there, and had a hard time to get out. But I figured out a way to do it and thought i could share my thought processes and guides here.

My initial goal was to learn web development so I could build an application that uses operations research abstracted with a nice UI for people to use.

The following guide is an unnoficial syllabus that mimics the computer science syllabus from many great universities (MIT, Stanford, Harvard, Berkley...) and most courses are free or very inexpensive!

It is assumed that you the reader have sufficient knowledge of Linear Algebra, Calculus, statistics and basic programming (notion of loops, datatypes, conditionality, OOP).


## My syllabus

## Fundamentals
### [Harvard's CS50](https://online-learning.harvard.edu/course/cs50-introduction-computer-science?delta=0) Introduction to Computer Science
A very good introduction to computer science from the great (if not best) instructor David J. Malan. This course covers the surface of basic programming, python, SQL, web development. I was also exposed to the quality of education Harvard has to offer and was very excited that I could enjoy learning from the institution from the comfort of my home, for free.

### [Berkley CS61A](www.cs61a.org) Structure and Interpretation of Computer Programs 
This course is by far the best course to help you understand fundamental concepts in programming, regardless of the language. Topics range from Object-Oriented Programming, Functional Programming, Abstraction. Berkley also holds very high standards of quality regarding education, and it is clearly observable through all of the course notes and lectures they have published along with homeworks, exams and solutions for free, on the courses dedicated website. Since 2011.

### [Berkley CS61B](www.cs61b.com) Computer Architecture
A great introduction to the hardware that makes up a computer. Bootcamps and tutorials *always* skip this part, but it's fundamental to understand this.

### [Berkley CS61C](www.cs61c.com) Data & Algorithms
Having good fundations in data and algorithm is part of every CS degree out there, but this course is probably the best offered online, for free, available for anyone to take. It's a great course to develop your critical thinking and problem solving skills.

### [MIT's Discrete Mathematics](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-042j-mathematics-for-computer-science-fall-2010/video-lectures/)
I had a discrete mathematics course during my mathematics minor and I believe it's very useful for programming, so here is the best course available for free in that topic, which covers Logic, Proofs, Probabilities and other useful mathematical concepts for coding.

### [MIT's Distributed Systems](https://www.youtube.com/watch?v=cQP8WApzIQQ&list=PLrw6a1wE39_tb2fErI4-WkMbsvGQk9_UB)
Everything today relies on distributed computing, so if you want to build a website, you ought to learn about it because you will probably be using it.

## Web development
### [freeCodeCamp](www.freecodecamp.org)
Very good introductory course on web programming that covers HTML/CSS/JavaScript. The learning method is very hand-in-hand and code has been chewed up for you already, but it covers a lot of the basics and sets you up wanting more with different small projects.

### [FullStackOpen](www.fullstackopen.com)
A more advanced hands-on course on web development that uses JavaScript and covers the entire web stack.

## Machine Learning
### [Coursera Andrew Ng's Machine Learning I](https://www.coursera.org/learn/machine-learning)
Most AI courses give you an overview of ML algorithms and show you how to implement these in Python. This course is algorithm first, then has you implement it in Octave (to abstract Python syntax). It goes deep in the foundations of typical machine learning algorithms (logistic regressions, KNN, gradient boosting) and goes a bit deeper into how there functions work at their core (spoiler!: using a loss function that tries to minimize the gap between prediction and real data using testing and training data sets. This is operations research! woohoo!)

### [Machine Learning A-Z](https://www.udemy.com/course/machinelearning/)
This course can be summarized by this: how to implement popular ML algorithms using Python. Does not go deep in technical details, it's mostly a Python course on how to use the ML library. (I would recommend to wait for this course to be on special, it normally goes for 12-25$)

## Scripting
### [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)
One of the courses I did to try to find a more applicable approach to programming, hopeful that it would be project based and not exercices-only. I was not deceived! Most of the courses are based on small projects that are general enough for you to want to dig deeper, or to apply them in other settings (ex: you learn how to do web scraping with Python)

## Projects

A project that helped me dive in web programming was building this website. I would strongly suggest anyone that wishes to start coding to also have this as a side project.  
I would suggest you to finish the HTML/CSS part of freeCodeCamp.org before doing so. Using HUGO for your website will also teach you how to use vscode, git and netlify. I shared [here](./posts/aboutthiswebsite.com) how I managed to do it.  
It will also push you to read a lot of code and with only your ambition to customize the appereance of your website, you will learn how to navigate through files and figure out how things are interconnected, what works and what doesnt, and asking yourself 'what happens if I remove this?'.

## Missing semester - useful tools
Along all of those tutorials, something that might be missing would be the basics of most tools you will be using later on to develop your own projects, such as:

Code editors
Shell scripting
Version Control
etc...

A great ressource for this would be MIT's [missing semester](https://missing.csail.mit.edu/), which goes in dept on most of these.