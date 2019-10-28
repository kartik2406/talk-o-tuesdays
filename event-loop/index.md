---
title: Event Loop
date: "2015-05-28T22:40:32.169Z"
category: 'Talk-o-Tuesdays'
cover: "./cupcake-media-704554-unsplash.jpg"
tags: ['js']
---

> Today's talk

## What the heck is the event loop anyway?, by Philip Roberts. @JSConf

### What is the talk about?

Javascript handles async operations with the help of event loop, callbacks. As JS developers we use async code almost every day, but we might not know the internal working of the async operations. This talk will help you learn the meaning of all the async jargon. To make it easier to understand, the talk has lots of awesome animations, demos. We often understand what is async but dont really know what does what and how?

### What will you learn?

- How does JS handle async events?
- What is the call stack, callback queue, event loop
- Whor provides these features? How do they interact with each other?
- Why is browser blocked in case of sync events
- Whatt? setTimeout(0) is a thing? How does it work?

### Summary

- JS can only do one thing at a time, thing at the top of the queue is the one that is currently being executed
- Async capability in JS is due to web API's, and in Node due to C++ API's, event loop, callback queue
- Event loop is not part of the JS runtime
- When the callstack is empty, event loop will pick atask from callback queue and place it onto the callback stack...
- What is the need for async? Well if all the actions where sync, then the UI would have been blocked and that wouldn't be a good UX.
- Along with callback queu, there is a render queue that repaints the window.
- setTimeout() meanx min time to execution, setTimeout(0) works becuase the cb gets put onto the callback queue.
- JS Runtime = heap + Call stack
- Browser = JS Runtime + Web API's + Callback Queue + Event loop
