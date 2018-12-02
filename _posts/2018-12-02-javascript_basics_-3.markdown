---
layout: post
title:      "JavaScript basics -3"
date:       2018-12-02 19:35:15 +0000
permalink:  javascript_basics_-3
---


Functions are an integral part of the JavaScript language. A function is a block of code designed to perform a set task. Functions are reusable and hence become handy when you must perform one operation numerous times. They just make life easier.

```
function test (param1, param2) {
  console.log (param1, param2);
}
```


The above function is a simple function that is called test. It takes in two parameters; parameters can be strings, numbers, or any data type. You can have a return in a function but not required. In this function there is not a return. This function just outputs the parameters in the console.

```
var myGlobal = 10;

function test(){
var myLocal = 5;
}
myGlobal //10
myLocal//undefined
```

Scope is an important lesson and takes a while to understand. You can declare variables but where you put it matters. Outside the function, declaring variable obtains a global scope. Inside a function, declaring a variable obtains a local scope. When looking at the references in the variable, you notice myGlobal still assigned to 10 and shockingly, you notice myLocal assigned to undefined even though you declared the variable. This is the difference between local and global scope. You may test this out in a browser console.

```
var switchOn = true;
var switchOff = false;
```

Another data type is the Boolean; Booleans are either true or false. Careful when you use Booleans, Booleans cannot contain quotation marks. “true” and true, in coding, are not the same thing.

```
function test (myCondition) {
  if (myCondition) {
     return "It was true";
  }
  return "It was false";
}
```

We can use a simple condition to make a function more complex and apply some logic into a function. Here we pass in a Boolean into the parameter in myCondition. “It was true” is returned when myCondition is set to true; “It was false” is returned when myCondition is set to false.

```
== //comparison operator, performs type conversion and then compares in both type and value
===//comparison operator, performs comparison as is, in both type and value
3 == '3' // returns true because JavaScript performs type conversion from string to number
3 === '3' // returns false because the types are different and type conversion is not performed
```

Comparison operator, == or ===, are used to compare data types and thus perform logical conclusions. Explanations are provided in the comments above and give a basis what to use comparison operators for.

```
!= //negative comparison operator, performs type conversion and then compares in both type and value
!==//negative comparison operator, performs comparison as is, in both type and value
```

These comparison operators work the same way as positives (== or ===) but != or !== are negatives. It is equivalent in doing the same comparison value == or === and then returning the opposite Boolean type (if return true, now is return false and vice versa). This is just adding another set of comparison. Sometimes it is more helpful to use the negatives rather than the positives comparison operators.

```
> // greater than
<// less than
>= // greater than or equal to
<= // less than or equal to
```

The above set of comparison operators perform exactly like in mathematics. They are often use numbers but in coding, string containing numbers can be used (be wary of the type when comparing). 

```
&& // and
|| // or
```

You can combine several comparisons into one long condition with either the above operators. When using “&&” in code, all the condition is required. When using “||” in code, only one of the conditions is required. 

This ends JavaScript part 3. I’m excited that I revisited such topics, as this was a good refresher. Hope to clarify some things in JavaScript. See you in a part 4.

