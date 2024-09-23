---
title : "Bộ nhớ"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
Bên trong máy tính, chúng ta có một lượng **bộ nhớ** hữu hạn. Mỗi kiểu dữ liệu yêu cầu một lượng tài nguyên hệ thống nhất định:
- `bool` 1 byte
- `int` 4 bytes
- `long` 8 bytes
- `float` 4 bytes
- `double` 8 bytes
- `char` 1 byte

Ta có thể tưởng tượng một `char` (kiểu dữ liệu ký tự) sẽ cần 1 byte trong bộ nhớ, giống như trong ảnh:

![a byte](https://raw.githubusercontent.com/baobaoupcloud/cs-w1/main/static/images/2.memory/memory1.png)

Tương tự, một `int` (kiểu dữ liệu số nguyên) sẽ cần 4 byte:

![4 bytes](https://raw.githubusercontent.com/baobaoupcloud/cs-w1/main/static/images/2.memory/memory2.png)
