# L4: OOPS and SOLID Architecture

## OOPS drills

#### Countdown

- Create a class called ```Counter```
- Create a instance variable called ```value```. Initialize it to 0
- Implement a ```incr``` method which increments value by 1
- Implement a ```decr``` method which decrements value by 1
- Implement a ```incrby``` method which accepts a integer, n and increments value by n
- Implement a ```decrby``` method which accepts a integer, n and decrements value by n


#### Triangle and points

Create a Triangle class.

Initially this class will have an empty list of points. Add a ```add_point``` method which adds the point to the list of points. Add a ```perimeter``` method which calculates the perimeter of a triangle. Add a ```is_equal``` method which accepts another triangle object as an argument and checks whether the two triangles have the same list of points.

Create a triangle object, ```t1``` and add the following points:
```
0, 0 0, 3 4, 0
```

Find its perimeter

Create another triangle object, ```t2``` with the following points:
```
1, 2 2, 1 1, 5
```

Find its perimeter

Check whether ```t1``` and ```t2``` are equal

Create another triangle object, ```t3```, with the following points:
```
1, 2
2, 1
1, 5
```
Do the following operations:
```
t1 == t3
t1.is_equal(t3)
t3.is_equal(t1)
```

Rename ```is_equal``` to ```__eq__```:

Do the following operations
```
t1 == t3
```

## Solid Resources

- [Bob Martin SOLID Principles of Object Oriented and Agile Design - Watch from 16:00](https://www.youtube.com/watch?v=TMuno5RZNeE )

- [Software Design - Introduction to SOLID Principles in 8 Minutes](https://youtu.be/yxf2spbpTSw)

- [Playlist on Solid principles](https://www.youtube.com/playlist?list=PL6n9fhu94yhXjG1w2blMXUzyDrZ_eyOme)

- [Importance of code quality](https://www.multidots.com/importance-of-code-quality-and-coding-standard-in-software-development/)

- [How to Minimise nesting](https://en.wikibooks.org/wiki/Computer_Programming/Coding_Style/Minimize_nesting)  


## Data Munging Problem

[Practice Data Munging problem](http://codekata.com/kata/kata04-data-munging)

Spike out the first version just make it work.

In the second version:

Create proper classes. Try to apply OOPs concepts and do it using minimum amount of code.

Check your work - total 5 files

- Create a DataExtractor class - which only extracts data. Pass arguments to customize
- Create a DataAnalyzer class - which only calculates the min diff. Pass arguments to customize.
- Create a Calculator class - which initializes the two classes above and executes.
- Soccer and Weather files - Create objects of Calculator class and pass arguments. Make sure you use named variables for column names. Do not pass 6 directly.
