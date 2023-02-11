---
layout: single
title:  "Stolp of Varinye [EN]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---

# Let's start with an overview

What is Stolp of Varinye?

This is the draft of a project carried out in collaboration with 2 friends to validate our year of L2. Although this one was not finished and the implementation of Android compatibility was never fully realized, it nevertheless has some interesting technical features.

To sum up the initial objective, the idea was to create a mobile game inspired by the work of the **"Penrose Staircase"** produced by Mr. Escher. It goes without saying that the first difficulty was to revisit this concept in an idea that had not yet been explored: that of the repetition in an instantiating way of the stairs.

To explain more clearly, the objective of the game was to offer a puzzle game in a world formed by instances of the same terrain, everything that happens to a terrain, happens to the other instances.

***

# Programming work

This project was a new challenge for me, partly through the use of Shader and scriptable objects. Work that I will detail in more detail below:

## Shader and Stencil Buffer

The use of Stencil Buffer and more particularly Stencil Buffer was very practical within the framework of this project. Indeed, my goal was to create a "magnifying glass" that allowed looking through to see invisible objects the rest of the time. To put it simply, rays are emitted by a "master" object (Buffer Read) which will bounce off the objects marked "client" (Buffer Write). This bounce then makes it possible to send back the image of the object and consequently to see it through the master which is equipped with a transparent material. The final effect may therefore look like the one below:

![shaderDemo](/assets/images/shaderDemo.gif)

And below is the code for BufferR and BufferW (for Read and Write)

BufferR:

![ShaderBufferR](https://user-images.githubusercontent.com/114059469/200172035-054633b6-d313-40d1-98f3-964a59501c57.png)

BufferW:
 
![ShaderBufferW](https://user-images.githubusercontent.com/114059469/200172040-dd774511-b883-4a2e-a02e-d3a4ab67b6ce.png)

## Scriptable Object

The second problem, which was also related to the functioning of the game, was the use of scriptable Object in order to obtain a synchronized movement of the puzzle bricks, as shown in the image below:

![scriptableDemo](/assets/images/scriptableDemo.gif)

The method of operation of this mechanism is also quite simple since it consists of two types of block, a "Master" block and a "Slave" block. The Master block is determined by the player. He can indeed choose to move any block attached to the base instance of the world. The Master block then sends every local move it makes as data within the scriptable object. When data is updated in this same scriptable object, the "slave" blocks will then read the data and apply this movement to themselves locally.

# Continuation of the project

This project will have no continuation and will remain closed. It was also decided to make its code open source, so I would be happy to help you if any part of it interests you.