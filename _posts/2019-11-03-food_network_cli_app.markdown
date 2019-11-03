---
layout: post
title:      "Food Network CLI App"
date:       2019-11-03 11:13:23 +0000
permalink:  food_network_cli_app
---


The first project I completed is a command line interface (CLI) application that interfaces with the Food Network website. The application allows a user to search recipes featured on the Food Network website via key search terms. There were quite a few challenges, and lessons learned while building this application. In this blog post, I will discuss one challenge, thing I've learned, and the future work that can make the application more resilient, robust, and feature-rich.

## Chalenge

#### URL Creation

One of the first challenges I ran into when creating the project was figuring out a way to dynamically create URL's that lead to the page that is being scrapped. Instead of just scraping the same URL, the URL needed to be generated based on the user's search terms. Luckily, the Food Network's website has a predictable URL pattern that is also affected by search. If a user wanted to search recipes for 'chicken', the URL for that search would be "https://www.foodnetwork.com/search/chicken-". If the user wanted to use a search term with multiple words such as 'chicken taco', the generated URL will look like this "https://www.foodnetwork.com/search/chicken-taco-". A clear pattern emerges.

However, I discovered another problem quickly. The purpose of the CLI app is to find recipes. When searching based on the URL, the results will return not only recipes, but also ads, and articles about your search term. One of the ways I thought about solving this problem was to find the CSS tags relevant to only recipes and isolate them during the scrape. However, I found a much easier way by simply manipulating the URL being searched. Food Network's website has a built-in filter for searching only recipes. All I had to do was add the filter flag to the end of the URL that is generated. Let's say the user searched 'chicken', the generated URL will look like this "https://www.foodnetwork.com/search/chicken-/CUSTOM_FACET:RECIPE_FACET".

## One Thing I've Learned

#### The 'bundle gem name' Command

There were many things I've learned when putting this project together. From creating objects dynamically by calling a custom constructor in a loop from another class, to simple string manipulation techniques. My favorite thing has to be creating the scaffolding of a Ruby Gem with Bundler. There are certain patterns that most applications will follow in terms of the file structure. Bundler knows this and has a command that will auto-generate the structure of a Ruby Gem. 
The 'bundle gem name' command creates a basic structure for your gem project that includes a gemfile, and gemfile specs file. Note that the name part of the command is the name of your gem project and can be changed to anything.

## Future Work

The current state of the application is very basic and doesn't have much functionality. However, with more time, more features can be added. The following is a list of a few that I hope to add in the coming weeks.

#### Sort by Time

One of the biggest factors in determining what to cook is how long it will take to cook that item. I would like to add a method to the recipe class where users can sort the recipes based on the time it takes to cook.

#### Search With Pagination

At the moment, the app only searches the first page of recipes from the URL provided. This yields 10 results. However, I would like to add the ability to search through more pages.

#### More Details on Recipies

Currently, the app fetches the recipe name, time to cook, and the recipes URL. I would like the user to be able to lookup more details of a recipe, such as the ingredients, withing the CLI application.
