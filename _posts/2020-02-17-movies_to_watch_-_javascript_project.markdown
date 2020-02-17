---
layout: post
title:      "Movies To Watch - Javascript Project"
date:       2020-02-17 11:36:52 +0000
permalink:  movies_to_watch_-_javascript_project
---


## Overview
The 4th project in the Flatiron curriculum involves creating a Rails API that will be consumed by a vanilla JavaScript frontend. The project I build is a simple movie tracker. It keeps track of movies watched. The data is organized with a movies model, that belongs to a genre. Of course, genres have many movies. Although the project is simple, it encompasses a lot of concepts that build upon modern websites. This includes making API requests, and dynamically creating content on a webpage without reloading the page. This allows a website to be faster, more robust, and have a better user experience. In this post, I will discuss one of the most interesting things I've learned in this module, DOM manipulation.

## DOM Manipulation
Web browsers are amazing applications that sit in the background of a lot of the tasks we do on a computer. When a web page is loaded, a request is made to a server for a source HTML file. This file is then loaded into the browser, parsed, and any associated styles and JavaScript is applied. The browser creates a version of the source HTML file that is parsed into the DOM. The DOM consists of different nodes, and their values. This can lead to some amazing behavior and ultimately, the DOM enables modern web applications. Whenever a change is made to the web page, instead of reloading the page, the DOM can be updated with the changes instead. This allows the website load content dynamically, which is great for the user experience.

In the context of my project, the user can submit a form to add a new genre. If the page didn't take advantage of DOM manipulation, when the user submits the form, the page would have to reload to add the genre or let the user know there was an error. This can get annoying, and can also be slow. Instead, the website makes an API request, gets a response, and displays the result to the user (error or success) in realtime. 

## Future Work - Things I Want To Add
1. The ability to delete movies, and genres.
2. A search input to lookup movies
3. Better styling

