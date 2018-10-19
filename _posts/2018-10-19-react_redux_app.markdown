---
layout: post
title:      "React/Redux App"
date:       2018-10-19 16:12:40 +0000
permalink:  react_redux_app
---


**H**ello. It’s been a while. Time seems to pass quickly.

> The code should be written in ES6 as much as possible
> 
> Use the create-react-app generator to start your project
> 
> Follow the instructions on this repo to setup the generator: create-react-app
> 
> Your app should have one HTML page to render react-redux application
> 
> There should be 2 container components
> 
> There should be 5 stateless components
> 
> There should be 3 routes
> 
> The Application must make use of react-router and proper RESTful routing (should you choose to use react-router v3 please refer to the appropriate docs; docs for v4 can be found here)
> 
> Use Redux middleware to respond to and modify state change
> 
> Make use of async actions to send data to and receive data from a server
> 
> Your Rails API should handle the data persistence. You should be using fetch() within your actions to GET and POST data from your API - do not use jQuery methods.
> 
> Your client-side application should handle the display of data with minimal data manipulation
> 
> Your application should have some minimal styling: feel free to stick to a framework (like react-bootstrap), but if you want to write (additional) CSS yourself, go for it!

**T**hose are the specs for the React and Redux portfolio project. It is quite daunting especially for someone who just trying to understand JavaScript and now to quickly learn React and Redux. I had completed a book about JavaScript after the jQuery app. The book cemented some logic and principles of JavaScript which in doing so taught the basics well. I recommend A Smarter Way to Learn JavaScript, by Mark Myers. I had a grasp for it and used as most as I could on the React and Redux section.

**A**nyway, back to React and Redux “land”, I guess I should start by explaining the overall process of how a react app works. To get started, the command “create-react-app” automatically lays out the groundwork for building such an application. You get dependencies, react-scripts, an index.html, index.js, app.js, and a cool React logo with some CSS (which you can easily alter or delete to your desire effect). You can create a store which holds most of the current state or modified state given with a reducer which takes in and uses actions and the current state. The “Store” is wrapped around a Provider which essentially calls for a re-render of the components. In the components, you have props (short for properties) and state (which are like props but are mutable). In addition to passing data from the “Store” to the components, the components may pass data from its state to next components’ props. For the application, components render the data, and any, welcoming possible function that you want to enact. Components may have forms or buttons and when the user chooses to enact these actions, specific actions are sent to an actions.js page. These actions dispatch that returns a type and payload sent to the reducer function. In the reducer function, you have an initial state and an action. The reducer function is most-like a switch function that returns the modified state that later updates the store. There you have it, in a small “nutshell”.
	As for my React and Redux app, I made a tool rental app that uses and implements the CRUD (create, read, update, and destroy) actions with a front end of React and Redux and a backend with Ruby on Rails. The process for React and Redux doesn’t really start anywhere but I would recommend creating a “Store” and applying “thunk” (part of redux) for the app. This is probably what I should have started with, but I started writing code for the layout and trying to start implementing code for components, actions, reducers, and then the store. Then I questioned how to connect this to a Ruby on Rails backend. I essentially wrote code that completes fetching data from a Ruby on Rails backend, takes that data back to the reducer and then the store and then the component, then render onto the component. I think it took more than four days just trying this. I read the React docs over and covered some more JavaScript. Then I spent another probable week to do the add, update, and delete tool into my application with React. The add and delete action are mostly similar and only had problems trying to make sure the redux worked. The action to update tools was the big challenge. Initially, I thought there was two ways of trying to get data from the back-end to the front-end: fetching all the tools or fetching for just that one tool, and then after to render into the component’s prop. I choose the latter. In effect, my code kept producing bugs such as not able to render the correct tool with its properties or on the form, not able to put this.state.name into the value of the form. Sometimes, it rendered correctly but I could not modify the form on Mozilla Firefox. It froze, as I could describe it. Issues on correctly tabulating data in the backend came and go. I fixed most of code through reading the React docs, looking up examples in some lessons, and a study group session.

**T**here were A LOT of errors in the making of this light-appearing app. Well, cheers on the React and Redux app with a Ruby on Rails backend. 

