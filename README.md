# ECE-2112 - Programming Assignment 1
**By: Macni, Julian Diether J. | 2ECE-B**
### Overview
This repository contains the Programming Assignment 1 for ECE 2112 - Advanced Computer Programming and Algorithms. The problems for this assignment covers Module 1 - Base Computing with Python, which covers basic Python functions and techniques such as indexing, slicing, and more.

## A. Word Rotation Problem
Create a function that accepts a non-empty string and moves the first character of the string to the end while keeping all remaining characters as well as their capitalization in their original order.

The following functions and methods were used in this problem:

• **Slicing** - used to get the indexes of specific characters

Example:
```python
text = "programming"
text[1:9:2] #[index of the first element: number of characters: increment]
```
which results to `rgam`

• **Concatenation** - joins characters together

Example:
```python
text = "programming"
text[1:9:1] + text[0]
```
which results to `rogrammingp`

These methods were combined in order to put the first character of the string to the end:
```python
def rotate_word(text):
    return text[1:] + text[0]

print(rotate_word("python"))
```
resulting to `ythonp`




## B. Username Builder Problem
Create a function that accepts two strings for the first name and the last name. Then it generates a username that has all of the characters lowercase as well as removing all spaces while separating both the first and last name with a period.

The following functions and methods were used in this problem:

• `.lower()` - a string method that converts all letters to lowercase
Example:
```python
name = "Macni"
name.lower()
```
which results to `macni`

• `.replace()` = a string method that replaces characters in the string. The first parameter is the character to be replaced, while the second parameter is the character that replaces the first parameter.
Example:
```python
name = "Julian Macni"
name.replace(" ","")
```
which results to `JulianMacni`

• **Concatenation** - joins characters together
Example:
```python
first_name = "Julian"
last_name = "Macni"
first_name + "." + last_name
```
which results to `Julian.Macni`

These methods were combined in order to convert the letters to lowercase, to remove the spaces, as well as to add a period to separate the first and last name:
```python
def make_username(first_name, last_name):
    return (first_name + "." + last_name).lower().replace(" ","")

print(make_username("Ada", "Lovelace"))
```
resulting to `ada.lovelace`




## C. Bookend Swap Problem
Create a function that accepts a list containing at least two elements, and only swaps the first and last element in the list.

The following functions and methods were used in this problem:

• **Sequency Unpacking** - a syntax that assigns elements into individual variables
Example"
```python
first, *middle, last = ["red", "green", "blue", "yellow"]
```
in which `first = "red"`,  `middle = ["green", "blue"]`, `last = "yellow*`

• **Concatenation** - joins characters together
Example:
```python
["red"] + ["green", "blue"] + ["yellow"]
```
which results to `["red", "green", "blue", "yellow"]`

These methods were combined in order to swap the first and last elements in the list:
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]

print(swap_bookends([1, 2, 3, 4, 5, 6]))```
```
resulting to `[6, 2, 3, 4, 5, 1]`

Thank you for reading!
