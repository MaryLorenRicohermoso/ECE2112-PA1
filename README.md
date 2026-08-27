# ECE2112-PA1

Ricohermoso, Mary Loren P. | 2ECE-B

This repository contains the Programming Assignment 1 for "Advance Computer Programming" this A.Y. 2026-2027. This covers three python problems referring to Module 1- Base Computing with Python.

# A. World Rotation Problems
Create a function named `rotate_word()` that accepts aa non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character.   

The following string indexing and slicing techniques were used in this problem:

• `text[0]` - accesses the first character of the string. Since Python uses zero-based indexing, index "0" represents the first character. 

Example: 
    
      `text = "python" 
       text[0] --> "p"`


• `text[1: ]` - utilzing slicing to obtain all characters starting from the second character and continuing to the end of the string.

Example:
     
      `text = "python" 
       text[1 : ] --> "ython"` 


The first character can then be transferred to the end of the string by connecting `text[1 : ]` with `text[0]`. Theese operations were combined to construct the function:

   ```python
    def rotate_word(text):
      return text[1 : ] + text[0]

    print(rotate_word("python"))
```

# B. Username Builder Problem

Create aa function named `make_username()` that accepts two strings: `first_name` and `last_name`. The function converts all letters to lowercase, removes all spaces from both names, and combines the processed names using one period (.). 

The following string methods and string connecting them weree uutilized in this problem:

•`.lower()` - A string method that converts aall uppercase letters in a string to lowercase.

Example:
      
        `first_name = "Ana Maria"
        first_name.lower() ---> "ana maria"`

        `last_name = "De Leon"
        last_name.lower() ---> "de leon"`


•`.replace(" ", "")` - A string method that replaces every space with an empty string. This effectively removes all spaces from the string.

Example:
       
        `first_name = "Ana Maria"
        first_name.replace(" ", "") ---> "AnaMaria"`

        `last_name = "De Leon"
        last_name.replace(" ", "") ---> "DeLeon"`

•`String Connecting using "+" ` - Combines the processed first name, a period, and last name into a single username.

These methods and operations were combined to construct the function:

```python
def make_username(first_name, last_name): 
   first_name = first_name.lower()      
   last_name = last_name.lower()

   first_name = first_name.replace(" ", "")
   last_name = last_name.replace (" ", "")

   return first_name + "." + last_name          
              
print(make_username("Ana Maria", "De Leon"))      
```

# C. Bookend Swap Problem

Create a function named `swap_bookends()` that accepts a list containing at least two elements. The function exchanges the positions of the first and last elements  while preserving the original order of all elements while preserving the original order of all elements between them. The original input list must not be modified. 

There is a required form of extended sequence unpacking that is:

`first, *middle, last = item`

With this Statement 

•`first` - receives the first elment of the list.

•`*middle` - collects all elements between the first and last elements into a list.

•`last` - receives the last element of the list.

Example: 

```python
items = [1, 2, 3, 4, 5, 6]
first, *middle, last = items --->

first = 1
middle = [2, 3, 4, 5]
last = 6
```
The first and last elements can later be exchanged by constructing a new list using list sequence.

Example:

            `[last] + middle + [first] --> [6, 2, 3, 4, 5, 1]`


Combining them, the final function for this problem is as follows: 
     
  ```python
      def swap_bookends(items):
            first, *middle, last = items
            return [last] + middle + [first]
      print(swap_bookend([1, 2, 3, 4, 5, 6]))
   ```

Thank you for reading!

To see the main python program for Programming Assignment 1, click this link 
https://github.com/MaryLorenRicohermoso/ECE2112-PA1/blob/main/Ricohermoso_Maryloren_2ECEB.ipynb and download. Open on Jupyter Notebook, then run all cells. 

# README file Version History:
August 27, 2026 - Initial README output uploaded















