---
title : "Đối số dòng lệnh"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
**Đối số dòng lệnh** là các giá trị được nhập vào sau tên của chương trình trong cửa sổ shell của hệ điều hành. Chúng có thể được sử dụng làm đầu vào để điều khiển chương trình một cách dễ dàng và linh hoạt hơn.

Cú pháp:

```bash
int main(argc, string argv[])
{}
```

`argc` (arguments count) đếm số lượng đối số được nhập vào trong câu lệnh. Giá trị của `argc` phải là số dương.

`argv` (arguments vector) là mảng chứa các đầu vào từ dòng lệnh.

Ví dụ:

- Tạo tệp `argument.c` và viết code như sau:

    ```bash
    #include <cs50.h>
    #include <stdio.h>
    
    int main(int argc, char* argv[])
    {
        printf("Bạn đã nhập %d đối số:\n", argc);
    
        for (int i = 0; i < argc; i++) 
        {
            printf("%s\n", argv[i]);
        }
    }
    ```

- Nhập `make argument` trong cửa sổ terminal để biên dịch tệp
- Thử chạy chương trình bằng cách thêm đối số sau tên chương trình:

    `./argument chào bạn`

- The output will be

    ```bash
    Bạn đã nhập 3 đối số:
    ./argument
    chào
    bạn
    ```