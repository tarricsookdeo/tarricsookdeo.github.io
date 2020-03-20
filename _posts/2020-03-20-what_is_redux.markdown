---
layout: post
title:      "What is Redux?"
date:       2020-03-20 02:26:24 -0400
permalink:  what_is_redux
---


## Overview:
The last section of the Flatiron School curriculum is about Redux. It is also required to use Redux as a state manager in the final project. In this blog post, I will discuss what Redux is, and why you would want to use it, as well as a simple explanation of all the parts such as reducers, and actions.

### What is Redux?
Redux is a global state manager. At Flatiron School, we use Redux in combination with React. Note that even though Redux and React mingle well with each other, Redux can be used in almost any project, not only ones that use React. Redux allows you to create a central, global state called a store. Any part of your app can tap into this store, use, and change the data in it so long as it has permission to do so. Data within a store can only be change in a pre defined, specific manner using actions.

### Why Use Redux?
Redux can take a lot of boilerplate, and repeated code to setup. So it can be recommend that in small projects, Redux isn't needed. However, as a project becomes more and more complex, it can become a hassle to do the prop drilling that will be used in a React project. This is where Redux shines. In a large project, having a separate global central store can help keep components simple, and stateless.

### The Parts of Redux
Redux can be thought about in 3 parts:
1. The Reducer
2. Actions
3. Dispatch Methods

#### Reducers
Reducers are pure JavaScript functions. A reducer takes 2 arguments: an initial state, and an action. Based on the action selected, and the actions payload, a reducer decides how to update the data in the central store.

#### Actions
Actions are simply a name designated to a specific thing the reducer can do. Actions are called, and usually have a payload which represents the data that you want to pass to a reducer.

#### Dispatch Methods
Dispatch methods are called when you want to make an action happen. A dispatch method is imported as a prop to the React component that you wish to use it. When an event happens, such as a click, a dispatch method can be set to fire off. A dispatch method invokes an action to occur, potentially changing state.
