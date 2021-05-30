# JavaScript

Introduction to JavasScript and its ecosystem

## JavaScript Basics

[Introduction to JavaScript - Udacity](https://in.udacity.com/course/intro-to-javascript--ud803)


## ES6 Basics

[Introduction to ES6 - Udacity](https://www.udacity.com/course/es6-javascript-improved--ud356)

## freeCodeCamp [Optional] 

If do not feel confident with JS yet or you want more prectice go ahead with the freeCodeCamp JS certification.

[FreeCodeCamp Course](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/)

## Data Project - JS Version

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