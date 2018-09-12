---
layout: post
title:      "Programming and fundamentals/farming app"
date:       2018-07-15 22:27:38 -0400
permalink:  programming_and_fundamentals
---

So, what is programming or coding? Programming is what you input to a machine. More precisely, it is the set of machine instructions that tell the machine what and how to do a task or a list of tasks. Computers and machines run programs that diligently and successfully do multiple tasks with ease, provided a solid set of commands in programming. Because machines are very good at repetitive task, they work well with us. 

In many ways, programming has been a very part of your life. Programming makes robots become alive, become available to speak and jump, or possibly, one day, interact with human activity(such as cleaning or cooking). In the medical field, programming helps doctor and patient maintain a seemingly fast interaction; it may help to discover new remedies or quickly diagnose patients. The activity of programming has developed the newly-generated self-driving cars; as such, challenges in programming present themselves as there are walkers and more natural conditions that programs must adhere to. Other programmers(people who code programs) develop games; gaming has been a huge industry that wraps probably millions of people every year. Programming helps to create and use websites that enable users  to search for information, view guides and principles, or be exposed to funny content. Ever since the development of programming, it has been vital to the human interaction.


To get started in programming, here are a few things to know:

I will use javascipt as the programming language.

**Variables** are instances that hold another piece of information (or in computer terms, a memory that contains a certain value).
```
var name = "Richard";
var number = 4;
var answer = true;
```
In the following code, name, number, and answer are variables. `var` tells the computer that it is a variable. name contains a primitive type of string,"Richard". number contains a primitive type of integer,4. answer is a primitive type of boolean (true/false),true. These are but a couple primitive types. You may read further here:
[http://developer.mozilla.org/en-US/docs/Glossary/Primitive](http://).

**Functions** are blocks of code that are good for repetition. They are used to cut repetitive tasks. They look like this in the following:
```

function doesSomething() {
	for(var i = 0; i < 10; i++) {
	  console.log(i);
	}
	return "Hello";
}
```

In the following code, I code a function with a named doesSomething.

(Bonus: To run the function, you have to call the function; in this particular case, 
`doesSomething();` )

In the function, I have a for loop (a useful tool to code something over and over again) that outputs, one at a time,  in the console the numbers 0-9. There is also a returned value of "Hello" at the end of the function, which may be used for a  variable, for example.

This is but a small sample of programming and what methods are available to use. Code is stored in libraries and APIs(application program interface). As someone goes beyond programming, the complexity of his code grows and a working program develops into a beautiful "work of art".  To develop these programs, there may be struggles and there may be satisification.


It is near September and this rails app with jquery is just about complete. I feel enlightened after the processs. The challenges that the program posed gave me great frustrations and the ability to work out perfect or somewhat near perfect solutions have been great also. My app is about creating an interface that allows ,users but more specifically farmers, to post their products and for users to generate comments about their product and develop a sense of where their food comes from as well as what farmers offer in the marketplace.


In order to fulfill a completed project, I will talk about the specifications of the project. First, I needed to create a way to serialize data and create a JSON object. To serialize data on ruby on rails, you can use the gem 'active_model_serializers' and *bundle install*. When serializing data and *rails g serializer user*, the building of the  class needs attributes to the object and creating the *hasmany/hasone* relationships(, which is like the models). Once data is called to be serialized, you can render the json of the object such render json: @item. You are also able to extract the data in JSON objects through methods and post in URLs. The ability to transform between data as JSON and data as raw data in html format was challenging throughout the creation of web pages and routes. The second part was to use jQuery to implement tasks in the web browser. In my app, I was able to create a form that adds a comment to the current page and stop the form from submitting and rendering/redirecting another page. It took me a long time to go over the jQuery docs and research before the adding comment and stopping form submission came true. I also added a nifty calculator function, implemented with Javascript.
This is most of the bulk of work to be added to the ruby on rails project(although I created a whole project). The learning process throughout the build has been very rewarding. I look forward to see other projects.

