---
layout: post
author: "Natalie"
title:  "Tech Interviews - OOP and Android Development"
date:   2018-10-16 18:37:01 -0500
categories: notes
---

# Object Oriented Programming

- What's the difference between **Interface** and **Abstract class** or (Java) What's the difference between **extend** and **implement**
  - `extends` is for *extending* a class.
    - extending a class's functionality
    - significance of an abstract class:
      - Provide a common type of its subclasses
      - Encapsulation subclasses of duplicate content
      - To define abstract methods
  - `implements` is for *implementing* an interface
    - interface you can not implement any of the declared methods
    - significance of an interface:
      - Specification
      - Extension
      - Callback
  - related concepts: **polymorphism and inheritance**

# Android Development

1. Activity Lifecycle
   1. `onCreate()`
      - activity enters the *Created* state
      - fires when the system first creates the activity
      - happen only once for the entire life of the activity
      - must implement this callback
   2. `onStart()` 
      - makes the activity visible to the user, as the app prepares for the activity to enter the foreground and become interactive
      - where the app initializes the code that maintains the UI
   3. `onResume()`
      - activity comes to the foreground
      - app stays in this state until something happens to take focus away from the app
   4. `onPause()`
      - the user is leaving your activity (not necessarily destroyed)
      - indicates that the activity is no longer in the foreground (though it may still be visible if the user is in multi-window mode)
   5. `onStop()`
      - activity is no longer visible to the user, it has entered the *Stopped* state, and the system invokes the`onStop()` callback
      - if need to come back, use `onRestart()`
   6. `onDestroy()`
      - called before the activity is destroyed
      - two reasons:
        1. the activity is finishing (due to the user completely dismissing the activity or due to `finish()` being called on the activity), or
        2. the system is temporarily destroying the activity due to a configuration change (such as **device rotation** or **multi-window mode**)
2. Advantage of Kotlin
   1. **Concise** - Drastically reduce the amount of boilerplate code.
   2. **Safe** - Avoid entire classes of errors such as null pointer exception.
   3. **Interoperable** - Leverage existing libraries of JVM, android and the browser.
   4. **Tool friendly** - Choose any java IDE or build from command line.
3. Difference between Activity and Fragment
   - Why use a fragment
     - Reusability
4. Where to use thread and what is synchronization