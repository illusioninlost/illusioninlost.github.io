---
layout: post
title:      "Basics of Javascript-2"
date:       2018-11-26 14:28:23 +0000
permalink:  basics_of_javascript-2
---


A continuation of part 2 of the javascript segment. Basics are good for review.

```
var first = “Coding” + “ “ + “is”; 
//or “Coding” + “ is “
var adjective = “fun.”;
first += adjective;
```

String concatenation is simple and combines any number of characters into a longer string. The variable first now contains the data of string value of “Coding is “ which includes a space character. One of the biggest caveat in programming is that you must provide an empty space when you do string concatenation to express in English sentences. The comment (right under the assignment of first variable) provides a similar way to achieve the same assignment in the variable first. The second variable just contains another string for later purposes. We can concatenate it with the += operator, much the same as adding numerical values in mathematical expression. We get first variable with the entire string, “Coding is fun.”

```
var myStr = “Hello, my name is Richard”;
var myStrlength = myStr.length;
```

The String class in Javascript has a built-in method and when using the .length property on a string, the property counts the number of characters in the string variable.

```
var myStr = “Hello, my name is Richard”;
myStr[0]
//returns “H”
```

What if you just want a particular character given a non-empty string? Well, in programming, you can call the nth place character in the index by putting [n], n denoting the index, after the string variable. Programming uses zero based indexing, so the first character in the string has the index of 0, NOT 1. You can test this in the browser console.

```
var myStr = “Sun”;
myStr[0] = “R”;
//myStr is still “Sun”
```
Given what I said and coded above, what if you wanted to change the string “Sun” to “Run”. The above approach will not work because strings are immutable. A lesson hard learned until still later. You may change the variable assignment to run with a statement, “myStr = “Run”;”. Now the myStr contains the string variable “Run”. It is kind of peculiar. The variable myStr will not have any reference to the string “Sun” too. You may test this in a browser console.

```
var word = “brown”
var lastCharacterInWord = word[word.length -1];
//returns “n”
var secondtoLastCharacterInWord = word[word.length – 2];
//returns “w”
```

So you want to access any character with a given string in bracket notation. You can use the .length property to help retrieve that specific letter. 

On to the next topic which is array.

`var myArray = [“what”, “is”, 4, 3, true];`

An example of what an array looks like is shown above. It merely lists a bunch of Javascript data types that inherently gets an index of the array. The above array carries a total of 5 elements.

`[[“Bob”, 42], [“Co”, 3]]`

The above array carries 2 elements, which are also arrays. The inside array carries two elements. the lengths can be lengthy as you can imagine and as little as no elements. This is called a nested array.

```
var myArray = [“what”, “is”, 4, 3, true];
var myArrayLength = myArray.length;
//5
var myFirstElement = myArray[0];
// “what”
```

Like strings, arrays have the built-in .length method that counts the number of elements in the array. The variable myArrayLength has the value of 5. The variable myFirstElement references “what”, because it is referenced at 0th index position in the array. Remember the index starts at 0 not 1. As I should have mentioned before, if you use bracket notation to find element, there is no space between the variable word and opening bracket. It will compile nevertheless but it is bad coding practice.

The array class has several built-in methods that are commonly taught: push, pop, shift, unshift. The .push() method adds an element to the end of the array. The .pop() method removes the last element. The .unshift() method adds a specified element to the beginning of the array. The .shift() method removes the first element. 
The .length method works similarly in strings and arrays. Well that covers most of strings and arrays.

To be continued



