# L5: Web basics

## HTML and CSS
Start with [Learn to Code HTML and CSS by Shay Howe](https://learn.shayhowe.com)

In particular read the following sections and complete the exercises.

#### HTMl & CSS
* Lesson 1: Building your first web page
* Lesson 2: Getting to know HTML
* Lesson 3: Getting to know CSS
* Lesson 4: Opening the Box Model
* Lesson 5: Positioning content

#### Advanced HTML & CSS
* Lesson 3: Complex Selectors
* Lesson 4: Responsive Web Design

#### Resources for Flex and Grid Layouts:
* [CSS Flex Video](https://www.youtube.com/watch?v=JJSoEo8JSnc)
* [CSS Grid Video](https://www.youtube.com/watch?v=jV8B24rSN5o)

#### Resources for Web Development for any Topic:
* [Mozilla Web Docs](https://developer.mozilla.org/en-US/)



## Project II: Portfolio project

#### Goal
Build your portfolio website using your knowledge of HTML and CSS. The display should work in all resolutions.

Use your knowledge of responsive media queries, CSS flex, and CSS grid for handling multi-column layouts.

#### Hosting
Host your website on [Heroku](https://www.geeksforgeeks.org/how-to-deploy-a-basic-static-html-website-to-heroku/). The specifics will be discussed in class.


## Project II: Themed E-Commerce Website

#### Goal
Recreate the following [website](https://shop.polymer-project.org/), but with a theme of your own. Example: a shoe store, clothing store, electronics store, etc.

*NOTE*: This project is on HTML/CSS only, do not attempt to add functionality with JS. That part will come later. You should only use JS if it needed for widgets of frameworks like bootstrap.

#### Project Description
The website should have 5 pages:
1. Home Page
2. Item listing page
3. Single Item Page
4. Cart Page (hard code the items in the cart)
5. Checkout Page

#### Some pointers:
* Please work mobile-first.
* Use of a CSS framework like Bootstrap is encouraged but not required.
* Add README.md and .gitignore files to your repository.
* Make a common styles.css. Include it on each HTML page. Put the style classes here.They can be gradually reused.
* Work page by page, section by section, element by element. Break things down to the smallest step. Ask yourself what you don't know and figure it out.
* Try to work with high energy and complete things.

#### Hosting
Host your website on [Heroku](https://www.geeksforgeeks.org/how-to-deploy-a-basic-static-html-website-to-heroku/). The specifics will be discussed in class.

## Introduction to JavasScript and its ecosystem

#### JavaScript Basics

[Introduction to JavaScript - Udacity](https://in.udacity.com/course/intro-to-javascript--ud803)


#### ES6 Basics

[Introduction to ES6 - Udacity](https://www.udacity.com/course/es6-javascript-improved--ud356)

#### freeCodeCamp [Optional] 

If do not feel confident with JS yet or you want more prectice go ahead with the freeCodeCamp JS certification.

[FreeCodeCamp Course](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/)

#### Data Project - JS Version

**Java Script Data Project 1**

In this project, you will use the same raw data from the previous data project (IPL). There are 2 parts to the problem ...

**Part 1: JSON generation [RUBY]**

- Write a ruby program that takes the CSV file(s) as input, computes the data required for plots, and writes a JSON file as output.

- **IMPORTANT** The output JSON file should not contain all the data from the CSV file, it should only contain data for plots.

- **IMPORTANT** the data structure of the json should be based on the data needed to plot, described in Part 2.


**Part 2: Plotting [JavaScript]**

- Write HTML/CSS/JS code to plot the data on the browser
- Use the HighCharts JavaScript Lib for plotting [HighCharts Demos](https://www.highcharts.com/demo).
- Serve the html, js and json files with ruby

```sh
ruby -run -ehttpd . -p8000
```

- Use Fetch API on the Browser to get JSON data generated in Part 1 from the webserver [Browser Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

**Hosting**

Host the HTML / JS / JSON along with your other HTML projects on Heroku.


## Node.js

## What is node.js ?

[Official Docs](https://nodejs.org/en/docs/)

Well in 1-line, Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.

Huh?

Historically, JavaScript could be executed only in a web browser. Things changed in 2009 when node.js came into being. Using node.js we can execute JavaScript outside the browser environment.

Go through the videos below to understand more about how it works.
[Part 1](https://www.youtube.com/watch?v=uVwtVBpw7RQ&feature=emb_imp_woyt)
[Part 2](https://www.youtube.com/watch?v=XUSHH0E-7zk&feature=emb_imp_woyt)
[Part 2](https://www.youtube.com/watch?v=jOupHNvDIq8&feature=emb_imp_woyt)


#### Node Version Manager (NVM)

It is a tool used to manage multiple active Node.js versions.

The Node.js platform, Node.js ​community of tools, and Node.js libraries are fast-moving targets – what might work under one Node.js version is not guaranteed to work for another version of Node.js. Hence, users need ways to switch between multiple versions of Node.js

**Why use NVM?**

NVM allows users to:

- Locally download any of the remote Long Term Support (LTS) versions of Node.js with a simple command.
- Easily switch between multiple versions of Node.js, right from the command line.
- Set up aliases to switch between different downloaded versions of Node.js with ease.

[Learn more about nvm](https://github.com/nvm-sh/nvm)

#### npm - the node package manager

***npm***, short for Node Package Manager (well, not really), is two things:

- it is an online repository for the publishing of open-source Node.js projects
- and, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

A majority of Node.js libraries and applications are published on npm, and many more are added every day. These applications can be searched for on [npmjs](http://npmjs.org/). Once you have a package you want to install, it can be installed with a single CLI command.

Let's say you're hard at work one day, developing the Next Great Application. You come across a problem, and you decide that it's time to use that cool library you keep hearing about - let's use Caolan McMahon's **async** as an example. Thankfully, **npm** is very simple to use: you only have to run **npm install async**, and the specified module will be installed in the current directory under **./node_modules/**. Once installed to your node_modules folder, you'll be able to use **require()** on them just like they were built-ins.

Let's look at an example of a global install - let's say coffee-script. The npm command is simple: **npm install coffee-script -g**. This will typically install the program and put a symlink to it in **/usr/local/bin/**. This will then allow you to run the program from the console just like any other CLI tool. In this case, running coffee will now allow you to use the coffee-script REPL.

Another important use of npm is dependency management. When you have a node project with a package.json file, you can run npm install from the project root and npm will install all the dependencies listed in the package.json. This makes installing a Node.js project from a git repo much easier! For example, **vows**, a Node.js testing framework, can be installed from git, and its single dependency, **eyes**, can be automatically handled:

Example:
```sh
git clone https://github.com/cloudhead/vows.git

cd vows

npm install
```

After running those commands, you will see a node_modules folder containing all of the project dependencies specified in the package.json.

[NPM crash course](https://www.youtube.com/watch?v=jHDhaSSKmB0&feature=emb_imp_woyt)
