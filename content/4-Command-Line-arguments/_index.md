---
title : "Command-Line Arguments"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
**Command-line arguments** are the values given after the name of the program in the command-line shell of Operating Systems. They can be used as input to easily control the program with flexible value.

Syntax:

```bash
int main(argc, string argv[])
{}
```

`argc` (arguments count) counts how many arguments are typed at the prompt, including the name of the program. The value of `argc` should be non-negative

`argv` (arguments vector) is the array of inputs in the command-line

For example:

- Create file `argument.c` and write code as below:

    ```bash
    #include <cs50.h>
    #include <stdio.h>
    
    int main(int argc, char* argv[])
    {
        printf("You have entered %d arguments:\n", argc);
    
        for (int i = 0; i < argc; i++) 
        {
            printf("%s\n", argv[i]);
        }
    }
    ```

- Type `make argument` in the terminal window to compile the file
- Try running the program by adding argument after the program name

    `./argument hello world`

- The output will be

    ```bash
    You have entered 3 arguments:
    ./argument
    hello
    world
    ```