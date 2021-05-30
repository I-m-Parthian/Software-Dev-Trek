# IPL data set analytics

## Aim
To convert raw open data (run by run records in this case) into charts that tell some kind of story.

## Preparation
**raw data**\
The data for this exercise is sourced from [kaggle](https://www.kaggle.com/manasgarg/ipl/version/5).  
**NOTE:** you might have to find data sources on your own. For example the country of origin for the Umpires  

## Instructions

1. Download all the data needed. Consult your mentor if you have any problems accessing the raw data.
2. Initialize ```rbenv``` for this project. Hint: create ```.ruby-version``` file.
3. Enable ruby linting via. ```RuboCop``` for this project.
4. All projects should have ```README.md``` with instructions on how to run this project.

## What your program should do

From the CSV and other source files specified above, write ruby code to ...
1. Read in the data.
2. Write logic to slice / dice / accumulate / transform the data.
3. Using [gruff](https://github.com/topfunky/gruff) plot the plots specified in the problems section.

## Problems

**1. Total runs scored by team**  
Plot a chart of the total runs scored by each teams over the history of IPL. Hint: use the total_runs field.

**2. Top batsman for Royal Challengers Bangalore**  
Consider only games played by Royal Challengers Bangalore. Now plot the total runs scored by every batsman playing for Royal Challengers Bangalore over the history of IPL.

**3. Foreign umpire analysis**  
Obtain a source for country of origin of umpires. Plot a chart of number of umpires by in IPL by country. Indian umpires should be ignored as this would dominate the graph.

**4. Stacked/Grouped chart of matches played by team by season**  
Plot a stacked/grouped bar chart of ...
* number of games played
    * by team
    * by season