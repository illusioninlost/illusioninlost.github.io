---
layout: post
title:      "Back to basic Javascript"
date:       2018-11-23 14:17:27 -0500
permalink:  back_to_basic_javascript
---


After diving and learning to code, Javascript always presents its mysteries to me. The combination of using the keyword, this and the complex steps when combining string and array syntax.
As a step back, I thought it would be a good idea to revisit the basics as a refresher for the aging “noggin”. 


```
// this is a single comment
/* this 
is  a
multiline comment
//
*/
```


Comments are useful to tell users and programmers about something without the computer executing it. Comments are effectively not visible to the computer execution in the file.
JavaScript contain seven different data types: undefined, null, string, Boolean, symbol, number, and object. Variables (called var)  are used to store one of these data types; a programmer can later manipulate and store data types in a computer’s memory. One thing to note is that the variable name (what appears after the keyword var, or var name = “Bob”, name is the variable name) follows some guidelines according to its API(application programming interface). One of these such rules is that a variable must contain either letters, numbers, $, or _; a variable cannot start with a number or contain spaces, or use a reserved word in Javascript. This is the common rule when naming variables.

Here we have an example of variable usage:

```
var five = 4;
five = 5;
```

The variable five is initialize with the number(data type) of 4, called an initialization. In the following expression, this is an example of assignment: five is assigned to 5(number type), called an assignment.

All function and variable names are case-sensitive; five is not the same as Five. When coding in Javascript, camelcase is the best practice to use. Camelcase looks like this: camelCaseIsWhatIUse. Camelcase means you capitalize the first letter of each word after the first word; the capitalization may look like camel humps to people.
Part of the manipulation process is to change to the variables through some basic operations.
Adding in mathematics is easy when assigning a new value to a variable.

```
var twenty = 10 + 10;
i = I + 1; OR i++;
```

When adding 1 to the variable itself after initialization, the above is a shortcut to add 1 to the variable itself.

```
var twenty = 30 - 10;
twenty--;
```

Subtracting is another operator.

 ```
var twenty = 5 * 4;
 var twenty = 40 / 2;
```

Multiplication and division works in the same manner.
Numbers can be integers or floats
var remainder = 11 % 3;
The remainder value carries a value of 2. The modulus operator looks like a remainder.

```
a = a + 5;
a +=5;
```

These statements are equivalent; both add 5 to the variable a. the latter is a shortcut that works with subtraction(-), multiplication(*), and division(/). But be careful, when using subtraction and division, the left side(variable) becomes the minuend (or dividend) and the right side (number) is the subtrahend(or divisor). Order matters.

var myStr = "I am a \"double quoted\" string inside \"double quotes\".";
This is to show quoted strings inside of strings. The strings double quotes must be enclosed in escaped character, denoted by the backward slash(\) before the character” You may also use double quotes to wrap around single quoted strings such as “Hello, ‘Welcome to Javascript!’”.

TO BE CONTINUED

