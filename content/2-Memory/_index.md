---
title : "Memory"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
Inside of our computer, we have a finite amount of memory available

Each data type requires a certain amount of system resources:

- `bool` 1 byte
- `int` 4 bytes
- `long` 8 bytes
- `float` 4 bytes
- `double` 8 bytes
- `char` 1 byte

Physically, we might imagine that a `char`, which requires 1 byte of memory, may look as follows:

![a byte](https://raw.githubusercontent.com/baobaoupcloud/cs-w2/main/static/images/2.memory/memory1.png)

Similarly, an int, which requires 4 bytes might look as follows:

![4 bytes](https://raw.githubusercontent.com/baobaoupcloud/cs-w2/main/static/images/2.memory/memory2.png)
