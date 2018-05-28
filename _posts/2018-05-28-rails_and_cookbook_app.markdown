---
layout: post
title:      "Rails and cookbook app"
date:       2018-05-28 21:46:54 +0000
permalink:  rails_and_cookbook_app
---


Rails is a web-application framework that essentially, with some code, builds a dynamic web application with ease. Combined with MVC(models-views-controllers) and a database manager, someone can create a fanstatic website with CRUD(create,read,update,destroy) application and RESTFUL routes. 


As so , it is important to understand MVC. M is for Models. Models are workable classes that hold most of the relationaship between objects code and coordinate with ActiveRecord, which creates the object relationships that are stored in the database. For example, a User model can have a string(a datatype) username, a string password, and string tasks. V is for Views. Views are the presentable files that an user would see once the web application is downloaded. It may contain pictures, buttons, designs, forms, and all the other what-nots. As such, an user experiences breath-taking web application.Templates can be used to ease the work of individual views. C is for controllers. Controllers handle the web routes between models and views. Controllers maintain most of the logic code that keep your app fully functional and hopefully user-friendly. With ruby on rails, a route is more what you see after the https://www.example.com, in most websites. There is a lot of work for the controller to work with both the models and views. As one can imagine, stacking more than one model and one view adds more complexity to a more dynamic web application. For a functional web application, all three provide a strong foundation for website.


In my rails project, I create a shared recipe app or as it is called an online cookbook. The app demonstates the use of MVC. I use 3 models: users, recipes, and comments. For views, I create dynamic routes that contain urls such as "https://........./recipes" and "https://........./recipes/2/comments/1". As such the controller contains the logic and flow in the routes between the models and views. The app was much more difficult than I anticipated even though I did most of the routes correctly and first. I had a set schema for the models which I eventually had to modify in order to incorporate the omniauth gem and tweak my "model" forms. I am overall satisfied with the amount of CSS(cascading style sheet) put into this app. There is room for improvement but I can proudly say that I built my very first ruby on rails app. 

