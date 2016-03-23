# Variations of set\*

## Description
Write a program that reads two numbers `N` and `K` and generates all the variations of `K` elements from the set [`1..N`].

## Input
- On the first line you will receive the number **N**
- On the next **N** lines the numbers of the array will be given

## Output
- Print the length of the **maximal sequence**

## Constraints
- 1 <= **N** <= 1024
- Time limit: **0.1s**
- Memory limit: **8MB**

## Sample tests

| Input                                                    | Output |
|:--------------------------------------------------------:|:------:|
| 10<br>2<br>1<br>1<br>2<br>3<br>3<br>**2<br>2<br>2**<br>1 | 3      |

_Example:_

| N | K |                                      result                                      |
|:-:|:-:|:--------------------------------------------------------------------------------:|
| 3 | 2 | `{1, 1}` <br> `{1, 2}` <br> `{1, 3}` <br> `{2, 1}` <br> `{2, 2}` <br> `{2, 3}` <br> `{3, 1}` <br> `{3, 2}` <br> `{3, 3}` |

