---
title : "Arrays"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Array** is a linear data structure where all elements are arranged sequentially in the computer’s memory. 

To create an array in C, define the data type and specify the name of the array, followed by square brackets `[]` with the number of elements of the array. Then add the elements to the array by index number. Array indexes start with 0: `[0]` is the first element. `[1]` is the second element,…

For example: 

```bash
int scores[3];
scores[0] = get_int("Score: ");
scores[1] = get_int("Score: ");
scores[2] = get_int("Score: ")
```

`int scores[3]` tells the compiler to provide us three back-to-back places in memory of size `int` to store three `scores`.

Then we use `get_int` to get the Score and assign to the elements

Or we can improve the code into this:

```bash
int scores[3];
    for (int i = 0; i < 3; i++)
    {
        scores[i] = get_int("Score: ");
    }
```

The index number `i` will loop from 0 → 2 to get the three elements of the array `scores`