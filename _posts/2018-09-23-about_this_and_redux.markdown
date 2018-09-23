---
layout: post
title:      "About this"
date:       2018-09-23 01:28:33 -0400
permalink:  about_this_and_redux
---

The use of *this* in javascript is often a confusing subject in programming. In the light of recent events, this is a somewhat of a collection of resources built to explain the use of *this*. One thing to note is beginnning in ES5 bind methods(apply(),bind(),call()) were created to allow *this* to refer to the object. When created, arrow functions are said "to don't provide their own binding"(thus *this* refers to the  enclosing lexical context)".
 
**Global Context**

![](https://i.imgur.com/6NDfuYu.png)

In global context, *this* refers to the global object. Using the web browser's console, we can see that *this* refers to the window.

**Calling this and using apply, bind, call**
![](https://i.imgur.com/TJkaRsN.png)

In the above code, var obj is set as an object with *key a*, which has a value of string "object". I then set another variable a to the string "global". I simply made a test function that return this.a, not knowing what this refers to. When running test() as is, string "global" is returned because *this* refers to the window. When running with apply and call methods(these two, as well as the bind method, refers *this* in enclosing context), string "object", NOT "global", is returned because the method apply or call, referred *this* to var obj,NOT the window.
		 
**Arrow Function and Object Function**
![](https://i.imgur.com/FHIKckE.png)

Arrow functions, as discussed, do not have their own binding. In this demonstration, an object is created with properties: i that points to a number, b that points to an arrow function, and c that points to object function. The returned value of both functions is console.log(this.i, this). As we can see, using the arrow function, this.i refers to undefined and this refers to the window. Using the object function, this.i refers to number 10 and this refers to the object itself, var obj. Arrow functions do not provide their own binding. Arrow functions may be created faster with simpler syntax but lacks in the binding of this when called. Object function bind *this* to the object or in the example case, var obj. 
		
   

