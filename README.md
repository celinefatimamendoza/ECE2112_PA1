<kbd>ECE2112<kbd>
# ECE 2112 - Programming Assignment #01

**Celine Fatima C. Mendoza | 2ECE-C**

# EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING
  
This repository contains programming assignment 1 for the **ADVANCED COMPUTER PROGRAMMING AND ALGORITHMS** ```[ECE2112]``` course. It consists of three programming problems covering **Module 1 - Base Computing with Python**.


  ## I. Intended Learning Outcomes
  At the end of this laboratory activity, the student should be able to:

  1. use basic Python functions, operators, and string operations;
  2. manipulate strings using indexing, slicing, and built-in string methods;
  3. apply sequence unpacking to manipulate the elements of a list; and
  4. construct simple Python functions that return a specified result.

  ## II. Programming Problems
  
### A. WORD ROTATION PROBLEM 
Create a function named `rotate_word()` that accepts a non-empty string. Move the **first character** of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character.

### Function:
  ~ **String Slicing** ```text[1:]``` - This isolates the second character through the end.
  
  ~ **String Indexing** ```text[0]``` - This extracts the first character of the string.

```python
def rotate_word(text):
    return text[1:] + text[0]

#Examples
rotate_word("python")
rotate_word("logic")
rotate_word("Code")
rotate_word("A")
```


### B. USERNAME BUILDER PROBLEM
Create a function named `make_username()` that accepts two strings: `first_name` and `last_name`. The
function must:  
1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.)

### Function:
  ~ **Lowercase Function** ```first_name.lower()```, ```last_name.lower()``` - This function converts all characters in the string to lowercase.

  ~ **Replacing Characters** ```lower_firstname.replace(" ", "")```, ```lower_lastname.replace(" ", "")``` - The first portion inside the parentheses indicates what character/symbol is selected for replacement. Whereas the value in the second half is the one that replaces the targeted substring.

```python
def make_username(first_name, last_name): 
    lower_firstname = first_name.lower()
    lower_lastname = last_name.lower()

    nospace_firstname = lower_firstname.replace(" ", "")
    nospace_lastname = lower_lastname.replace(" ", "")

    return nospace_firstname + "." + nospace_lastname

#Examples
make_username("Ada", "Lovelace")
make_username("Alan", "Turing")
make_username("Ana Maria", "De Leon")
```


### C. BOOKEND SWAP PROBLEM
Create a function named `swap_bookends()` that accepts a list containing at least two elements. Unpack
the list into three variables:  
  • first – the first element;  
  • middle – a list containing everything between the first and last elements; and  
  • last – the last element.  
Using these variables, return a **new list** in which the first and last elements have exchanged positions.
The elements in middle must remain in their original order. Do not modify the input list.

### Function:
  ~ **`swap_bookends()`** ```swap_bookends(items)``` - This user-defined function takes in an input list, then processes the rearrangement of the first and last *items*, and returns a new list.

```python
def swap_bookends(items):
    first, *middle, last = items

    swapped_first = last
    swapped_last = first

    new_list = [swapped_first] + middle + [swapped_last]
    return new_list

#Examples
swap_bookends([1, 2, 3, 4, 5, 6])
swap_bookends(["red", "green", "blue"])
swap_bookends([8, 3])
```

## *END*

**Version History**   
*August 27, 2026* - Publishing of the whole output for experiment 01.






  
