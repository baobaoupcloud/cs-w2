---
title : "Strings"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
#### Strings
A `string` is simply an array of variables of type `char`: an array of characters.

For example in this image, we can see how a string is an array of characters that begins with the first character and ends with a special character called a `NUL character` `\0`:

![string](https://raw.githubusercontent.com/baobaoupcloud/cs-w2/main/static/images/3.strings/strings1.png)

An example of string defined in code:

```bash
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string s = "HI!";
    printf("%c%c%c\n", s[0], s[1], s[2]);
}
```

The string `s` is an array consists of 3 characters `H` `I` `!`

We can interact with strings like finding the length or converting into lowercase and uppercase, using pre-built code by other programmers in header files libraries.


#### String length

Use `strlen()` function in the `string.h` library to find the length of a string. For example:

```bash
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    // Prompt for user's name
    string name = get_string("Name: ");
    int length = strlen(name);
    printf("%i\n", length);
}
```

Function `strlen()` calculates the length of the string passed to it.


#### Lower and upper case

Use `toupper()` function in the `ctype.h` library to convert string into upper case. For example:

```bash
#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Before: ");
    printf("After:  ");
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        printf("%c", toupper(s[i]));
    }
    printf("\n");
}
```

It will get the string and convert every character in it into upper case. Similarly, can use `tolower()` to convert the string into lower case.
