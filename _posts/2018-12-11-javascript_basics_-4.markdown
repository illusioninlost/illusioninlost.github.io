---
layout: post
title:      "JavaScript basics -4"
date:       2018-12-11 12:58:46 +0000
permalink:  javascript_basics_-4
---



Here we look at switch statements and objects. 

```
switch(num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  case valueN:
    statementN;
    break;
}
```

The idea behind a switch statement is to overcome a huge multiline if statement (explained in the JavaScript basics-3) then. In switch statement, you need a variable to be evaluated-num is our variable- and each case represents a unique output depending on the input of num. Switch statements increase the readability and remove some statements

```
function caseInSwitch(val) {
  var answer = "";
  switch(val){
    case 1:
    answer = "alpha";
    break;
    case 2:
    answer = "beta";
    break;
    case 3:
    answer = "gamma";
    break;
    case 4:
    answer = "delta";
    break;
  }
   return answer;  
}
caseInSwitch(3)// return “gamma”
```


The above example presents a function with a switch statement that reevaluates the assignment of the variable answer based on the input val.

```
switch(val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```

If the same input gives out the same output in a switch statement, you can merge the cases together like the above shown. When val is 1,2, or 3, the result variable changes string. This simplifies and cuts away unnecessary code.

```
function test(a, b){
return a > b;
}
```

Depending how you called the function, the return value of the function is a Boolean, either true or false. test(1, 2) returns false and test(2,1) returns true. The function might look funny, but this is all right and returns the Boolean with no problem. It is very practical to write code in this concise way.

```
var count = 0;

function cc(card) {
  switch(card){
    case 2:
    case 3:
    case 4:
    case 5:
    case 6:
    count++;
    break;
    case 7:
    case 8:
    case 9:
    break;
    case 10:
    case 'J':
    case 'Q':
    case 'K':
    case 'A':
    count--;
    break;
    default:
    break;
  }
 
  
  return count > 0 ? `${count} Bet` : `${count} Hold`
}
cc(2); cc(3); cc(7); cc('K'); cc('A');
```

Card counting is a known technique to evaluate a count in blackjack based on given cards. a high count means you should place a big bet and a low count means you should place a lower bet or hold. Card counting increases your rate of rewards. Above, the function has a global variable of count with a count of 0. As we get more cards like cc(2), the count adds or subtracts, mimicked by the switch statement inside the function.  Once the count is complete, you are given the count and a decision to “Bet” or “Hold”.

```
var human = {
  name: "Richard",
  age: 20,
};
```

Moving onto objects, you can create these with named properties, which are assigned to different data types. Inside objects, it may appear to look like a dictionary. 

```
var firstName = human.name
var firstAge = human.age
var secondName = human[“name”]
var secondAge = human[“age”]
```

These are couple ways to access your object. Note if the property has a space, you would use the bracket notation with the quotation marks added.

```
var carObject = {
make: “Toyota”,
year: 2001,
miles: 145600,
name: [“Richard”, “Ken”, “Liz”]
}
```

Above shown is an example of object, as a data type; this is the start of what is called as object orientated programming in which you can create and manipulate objects to your will or store them in a data set. 

```
carObject.year = 2000; // update year property of carObject
carObject.tires = 4; //add new property of carObject
delete carObject.name;// delete name property of carObject
carObject.hasOwnProperty(make)//returns true or false if object contains specified object property.
```

Using the carObject above, we can access, update, add, delete, and find whether the property exists or not. A RESTful application is an application in which objects are changed based on HTTP request to get, put/patch, and delete. See you in JavaScript basics-5.



