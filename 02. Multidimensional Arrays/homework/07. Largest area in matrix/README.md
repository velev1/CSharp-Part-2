# Largest area in matrix\*

## Description
Write a program that finds the largest area of equal neighbour elements in a rectangular matrix and prints its size.

## Input
- On the first line you will receive the numbers **N** and **M** seperated by a single space
- On the next **N** lines there will be **M** numbers seperated with spaces - the elements of the matrix

## Output
- Print the size of the lasrgest area of equal neighbour elements

## Constraints
- 3 <= **N**, **M** <= 1024
- Time limit: **0.1s**
- Memory limit: **8MB**

## Sample tests

| Input | Output |
|:-----:|:------:|
| <table><tbody><tr><td>1</td><td><b>3</b></td><td>2</td><td>2</td><td>2</td><td>4</td></tr><tr><td><b>3</b></td><td><b>3</b></td><td><b>3</b></td><td>2</td><td>4</td><td>4</td></tr><tr><td>4</td><td><b>3</b></td><td>1</td><td>2</td><td><b>3</b></td><td><b>3</b></td></tr><tr><td>4</td><td><b>3</b></td><td>1</td><td><b>3</b></td><td><b>3</b></td><td>1</td></tr><tr><td>4</td><td><b>3</b></td><td><b>3</b></td><td><b>3</b></td><td>1</td><td>1</td></tr></tbody></table> | 13 |

_Hint: you can use the algorithm [Depth-first search](http://en.wikipedia.org/wiki/Depth-first_search) or [Breadth-first search](http://en.wikipedia.org/wiki/Breadth-first_search)._
