---
title : "Exit status"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---
When a program ends, a special exit code is provided to the computer.

When a program exits without error, a status code of `0` is provided to the computer. Often, when an error occurs that results in the program ending, a status of `1` is provided to the computer. 

For example: write a C program named `status.c` as follow:

```bash
#include <cs50.h>
#include <stdio.h>

int main(int argc, string argv[])
{
    if (argc != 2)
    {
        printf("Add one command-line argument\n");
        return 1;
    }
    printf("hello, %s\n", argv[1]);
    return 0;
}
```

Then run the program typing `./status mate`, we will get an exit status of `0` and the output will be `hello, mate`. If you fail to provide any argument, such as just `./status` , we will get an exit status of `1` with a warning “Add one command-line argument”.