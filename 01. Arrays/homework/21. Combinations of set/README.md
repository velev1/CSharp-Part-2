# Combinations of set\*
Write a program that reads two numbers `N` and `K` and generates all the combinations of `K` distinct elements from the set [`1..N`].

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

| N | K |                                          result                                           |
|:-:|:-:|:-----------------------------------------------------------------------------------------:|
| 5 | 2 | `{1, 2}` <br> `{1, 3}` <br> `{1, 4}` <br> `{1, 5}` <br> `{2, 3}` <br> `{2, 4}` <br> `{2, 5}` <br> `{3, 4}` <br> `{3, 5}` <br> `{4, 5}` |
