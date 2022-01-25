# NodeJS

##### Table of Contents
* [Getting Started](#Getting-Started)
* [Node.js Basics](#Node-Basics)
* [JavaScript Summary](javascript.md)
<!-- * [Express](#Express)
* [Templating Engines](#Templating-Engines)
* [Model-View-Controller](#MVC)
* [Advanced Routes and Models](#Advanced-Routes-and-Models)
* [SQL](#MySQL)
* [sequilize](#sequilize)
* [NoSQL](#NoSQL)
* [MongoDB](#MongoDB)
* [Sessions and Cookies](#Session-and-Cookies)
* [Authentication](#Authentication)
* [Sending E-mails](#E-mails) -->

<a name="Getting-Started"/>

## Getting-Started
---
### What is Node.JS?

![nodejs logo](img/nodejs.png)

> [Official Website](https://nodejs.org/en/)

* Node.js is a JavaScript Runtime.
* Node.js is a server-side platform built on Google Chrome's JavaScript Engine (V8 Engine).

* Node.js was developed by Ryan Dahl in 2009

> Node.js is an open source, cross-platform runtime environment for developing server-side and networking applications. Node.js applications are written in JavaScript.

``` 
Node.js = Runtime Environment + JavaScript Library
```

### Download Node.JS

* [windows](https://nodejs.org/dist/v16.13.2/node-v16.13.2-x64.msi)
* [macOS](https://nodejs.org/dist/v16.13.2/node-v16.13.2.pkg)



Once installed check current version or installed Version of node

``` 
    node -v
```

<a name="Node-Basics" />

## Node-Basics
---
### Role

* Run Server
    
    * Create Server
    * listen to incoming Requests

* Business Logic

    * Handle Requests
    * Validate Input
    * Connect to Database

* Responses
    * Return Responses(Render HTML, JSON..)

Basic program to print **Hello from Node, This is my first program** using nodejs

```javascript
    // first-app.js
    console.log("Hello from Node,\n This is my first program");
```
To run or execute nodejs file

    // syntax: node _filename_
    // here

```
    node first-app.js
```
