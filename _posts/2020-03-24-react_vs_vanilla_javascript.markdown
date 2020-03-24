---
layout: post
title:      "React vs Vanilla JavaScript"
date:       2020-03-24 23:12:38 +0000
permalink:  react_vs_vanilla_javascript
---


## Overview
React is a very popular frontend JavaScript framework for creating robust, dynamic, and interactive user interfaces. However, with having to learn JSX, and some of the quirks of React, one might wonder if it is worth it over plain old vanilla JavaScript. In this post I will discuss why I think learning React is worth it, and why it is a better tool than plain old vanilla JavaScript.

### Reason 1 - DOM Manipulation
When a web page is loaded, a virtual copy of the page is created in the browsers that represents how the source HTML is organized. This is called the Document Object Model (DOM). In vanilla JavaScript, to make an application dynamic, one would have to target and manipulate specific DOM elements manually. This can be expensive in terms of compute resources, and be error prone. In React, the UI is built using components. Components are separate units of the UI with their own state, data, layout, styling, and markup. This allows a React app to be more tightly controlled, and for the components to separate logic. By doing this, it is easier to maintain the UI, and DOM elements do not have to be directly manipulated. This leads to performance improvements, and less errors.

### Reason 2 - Plugins and Extensions
When programming in vanilla JavaScript, you may find that handling things such as routing, and data can become a hassle as an application grows. Luckily with React, you can take advantage of the power of npm and its million packages. React has very good support for npm and package management via webpack. This allows an application to grow painlessly without having to reinvent the wheel with common tasks such as routing by simply installing and importing a npm package to handle the task.

### Reason 3 - Documentation and Community
There is a plethora of recourses online to learn vanilla JavaScript. From stackoverflow to a million courses. However, I would argue that the documentation and support available for React is on par, or even better than that of vanilla JavaScript. This makes learning React, and JSX easier and more accessible.
