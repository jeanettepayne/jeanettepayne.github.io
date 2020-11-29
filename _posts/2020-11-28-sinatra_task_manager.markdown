---
layout: post
title:      "Sinatra Task Manager"
date:       2020-11-29 01:03:27 +0000
permalink:  sinatra_task_manager
---


While I was nervous to build my first full-on web app using Sinatra, I was about 10x less nervous than I was going into the CLI project. This time I was more confident that I can figure things out and take an idea from a blip on the radar to full-blown, functioning program.

I currently work in admin and absolutely live and die by my trusty task manager app, so I thought it could be fun to try to create something along those same lines, but a little more simplified and with a twist.

I decided that for my Task Manager app there would be two types of users - Managers and Employees. The breakdown/relationships between models are as follows:
* A Task belongs to an Employee
* An Employee has many Tasks, belongs to a Manager
* A Manager has many employees

There are no join tables, as I didn't think it made sense for a Manager to have many tasks through Employees. I did, however, want it to resemble the real world in the sense that Managers can assign tasks to their Employees. Rather than complicating relationships I just passed that off to logic and permissions.

Some of the labs I'd seen up to this point had helper methods of "current_user" and "logged_in?" - since I had two models that were two separate "user" classes, I created "current_employee", "current_manager", "employee_logged_in?", and "manager_logged_in?" This allowed me to really specify permissions like I had envisioned.

Some examples of those permissions are:
* Any employee or manager can view the managers list, employees list, individual manager/employee pages, and task lists and pages
* An employee can only create/edit/delete their own tasks or employee information
* A manager can only create/edit/delete an employee's tasks or delete an employee if that employee belongs to them
* A manager can only create/edit/delete their own manager information

I had the most fun with these permissions when I got into the erb files and was able to make it so only the users with permissions to edit/delete were even shown the edit and delete buttons when visiting pages. This gives double protection against a user attempting to do something they don't have permissions for, and is just generally more visually appealing (don't show me a button if I'm not supposed to click it). I also specified permissions using the helper methods within controllers so that if someone were to directly type in an edit or delete route they will be rerouted and shown a flash error, and unable to access the page.

Overall this project was incredibly fun and challenging. It was exciting to see a full web app with dynamic routes come to fruition. It was my first time using (basic) CSS, which I had probably too much fun with despite only using simple design elements. 

Building out this project not only gave me confidence in myself that I am capable, but showed me how much fun coding truly is. I found myself in a time vortex multiple times, not realizing how in the zone I was and how much work I was cranking out without taking a break. Here's to learning new things and proving to yourself that you can do it even when you think you can't!


