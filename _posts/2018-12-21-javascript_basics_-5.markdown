---
layout: post
title:      "JavaScript basics -5"
date:       2018-12-21 15:23:08 +0000
permalink:  javascript_basics_-5
---



Welcome back, in this blog we shall discuss while loops, for loops, return statements as a ternary operation and multi-ternary operation, Math.random(), and accessing objects inside a function. When coding repetitively, sometimes it is better to set with a while or for loop to iterate over a data type, such as arrays or objects. 

```
var i = 4;
var total = 0
while(i > 0) {
total += I;
}// total has a value of 10
```

Above we see set variables, total has an initialization of 0 and i has an initialization of 4.  Then with a while loop, you can run see a block of code or a single statement runs until the condition (i > 0) is false.
> The while loop tells the computer to do something if the condition is met. Its construct consists of a block of code and a condition. The condition is evaluated, and if the condition is true, the code within the block is executed. This repeats until the condition becomes false.

```
var total = 0;
for (var i = 0; i < 5; i++) {
total += I;
}//total has a value of 10
```

Here is a for loop that operates similarly to the discussed while loop. Inside the parenthesis of the for loop, there is an order: initialization, condition, statement that hits condition. for loops are usually used for iteration but it is up to programmer’s preference. for and while loops achieve the same purpose.

```
var arr = [
  [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
  for (var j=0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

Above, we have a set nested array, an iteration with a for loop; it will print in the console the order of the numbers individually.

```
//Setup
var contacts = [
    {
        "firstName": "Akira",
        "lastName": "Laine",
        "number": "0543236543",
        "likes": ["Pizza", "Coding", "Brownie Points"]
    },
    {
        "firstName": "Harry",
        "lastName": "Potter",
        "number": "0994372684",
        "likes": ["Hogwarts", "Magic", "Hagrid"]
    },
    {
        "firstName": "Sherlock",
        "lastName": "Holmes",
        "number": "0487345643",
        "likes": ["Intriguing Cases", "Violin"]
    },
    {
        "firstName": "Kristian",
        "lastName": "Vos",
        "number": "unknown",
        "likes": ["JavaScript", "Gaming", "Foxes"]
    }
];

function lookUpProfile(name, prop){
// Only change code below this line
for (var x = 0; x < contacts.length; x++){
    if (contacts[x].firstName === name) {
        if (contacts[x].hasOwnProperty(prop)) {
            return contacts[x][prop];	
        } else {
            return "No such property";
        }
    }
}
return "No such contact";
// Only change code above this line
}

// Change these values to test your function
lookUpProfile("Akira", "likes");
```

This is a good problem and way to test your understanding of objects (how to create and access). In this above function, we iterate through the number of contacts. We check if any of the contact’s firstName property is the name(parameter) and then if the property that we are looking for exists as prop(parameter), we return the result of the contact’s properties. We return “No such property” if we have a contact but not the right property we are looking for. And if there is no contact’s firstName, we return “No such contact”.

`Math.floor(Math.random() * (max - min + 1)) + min`

Above is a neat expression to randomly get a number within a range. It is quite amazing and magical.

`var a = parseInt("11", 2);`

We can convert strings into numbers with parseInt. The second parameter, which is optional, tells the computer to return a binary number(1’s and 0’s).

```
function findGreater(a, b) {
  return a > b ? "a is greater" : "b is greater";
}
```

We can simplify in coding by returning a ternary operation instead of an if/else statement.

```
function findGreaterOrEqual(a, b) {
  return (a === b) ? "a and b are equal" : (a > b) ? "a is greater" : "b is greater";
}
```

This is a new one for me but like the ternary operation, this is the return for a multiline ternary operation, or an if/else if/else statement.

While and for loops are great way of doing a small task over and over again-like a function. Functions are usually set bigger though. As an analogy, a person can count the number of attendees of a club, but a function incorporates this and the VIP guests, or change in security guards. Other important aspects were discussed in JavaScript and as JavaScript is an object-orientated programming it is important to review and practice basics. Thanks for tuning in and let’s get going with JavaScript basics-6.

