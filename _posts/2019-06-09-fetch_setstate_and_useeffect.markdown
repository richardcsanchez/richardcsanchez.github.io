---
layout: post
title:      "Fetch, setState, and useEffect"
date:       2019-06-09 16:20:44 +0000
permalink:  fetch_setstate_and_useeffect
---

In developing my React/Redux app, I kept running into the issue of how to capture an object's ID from an URL to use within a specific component. In Javascript/JQuery, this was something that seemed much more straightforward to me.

As I attempt various methods to debug, I delved into isomorphic-fetch to help me capture the object for a component from the URL. Isomorphic fetch is polyfill in the instance that a user uses the site with an older browser. Most modern browsers have fetch as native code, but isomorphic fetch will allow the older browsers to use ES6 syntax to utilize fetch.

The cycle for untilizing fetch remains the same. Fetch exports a default function that takes an URL and gets back a promise, which has a response. This data returned in the response is converted into JSON by calling .json on it, and then the promise is dispatched to the front end.

In the context of my project, when the DragQueenCard component, a function component, is rendered, it takes in an argument of  `match`. A match object contains information about how a `<Route path>` matched the URL. Within the object, several properties can be accessed. By isolating the `params` property, I was also able to retrieve the `id` that was used to retrieve the component within the route URL.

This isolation, `match.params.id` could then be interpolated into my fetch call, directing the location within the backend that I am retrieving data from.

In the component, I am running `useState`, which is a special function known as a  hook, that allows me to add React state to a functional component. Because in a functional component I don't have a `this` property, I can't assign or read `this.state`. Instead, I call the `useState` hook to declare a "state variable", which allows me to use the same capabilities that `this.state` provides in a class. 

`useState` returns a pair of values, the "state variable", as well as a function which updates it. The `useState` function allows me to create a variable `dragQueen`, that points to a set of `key:value`. The second value, `setDragQueen`, is called at the end of the fetch cycle to populate the `dragQueen` with the data from the backend. In a simplified form, `dragQueen` can be used as a "getter", and `setDragQueen` is used as the setter.

 I'm calling `fetch` within `useEffect`, which is a side effect that acts like it compresses `componentDidMount`,  `componentDidUpdate`, and `componentWillUnmount`. This hook indicates that after rendering, my component needs to do something. In this case, `useEffect` takes two arguments, the first of which calls `fetch`, which dispatches the retireved date using the `setDragQueen` function defined in the `useState` hook. The second argument, and empty array `[ ]`, tells the component to run this block of code whenever the first argument changes. Because this is a static component, this will run one time when the component loads and will not run again.   


