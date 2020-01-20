---
layout: post
title:      "Job Application Tracker"
date:       2020-01-20 23:44:42 +0000
permalink:  job_application_tracker
---

## Project 3 - Rails Application


### Overview
Since me and my peers are headed in the direct of applying to jobs, I thought it would be a cool idea to create a job application tracker website as my Ruby on Rails project. The website is simple at the moment, with limited fields. I would like to expand upon in in the future. In this blog post i will discuss one of the challenges I faced in creating this project and how I overcame it.

### The Challenge - Nesting in Rails
It took me a while to understand how nesting worked in Rails. This included nested forms, and resources. I didn't understand the use for it, nor how to do it for a while. Nested forms and resources are used when multiple models are associated with eachother. Nested forms allows the associations between models to be displayed to the user when inputing data. For example, in my project, the job_applications model, and the companies model are associated. A job_application has a company in it. This is called a belongs_to relationship (company belongs_to job_application). As a result, in one of my forms to create a job application, I had to nest a company form in it to allow users to list a company they would like to apply to.

Nested resources were a whole other can of worms. Nested resources allowed for routes to be nested, to create a more restful routing system. 

### Future Work - Things I Want to Add to the Project
1. More fields
2. Company contact info
3. Ability to filter by company, or status
