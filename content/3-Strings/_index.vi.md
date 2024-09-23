---
title : "Chuỗi"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
#### Chuỗi
`Chuỗi` có thể hiểu đơn giản là một mảng các ký tự.

Có thể hình dung chuỗi là một mảng bắt đầu bằng một ký tự và kết thúc bằng ký tự kết thúc đặc biệt `NUL character` `\0`

![string](https://raw.githubusercontent.com/baobaoupcloud/cs-w1/main/static/images/3.strings/strings1.png)

Ví dụ về chuỗi trong đoạn mã sau:

```bash
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string s = "HI!";
    printf("%c%c%c\n", s[0], s[1], s[2]);
}
```

Chuỗi `s` là một mảng gồm 3 ký tự: `H` `I` `!`

Chúng ta có thể thao tác với **chuỗi** như đo độ dài chuỗi, chuyển đổi giữa chữ viết hoa và viết thường bằng cách dùng các mã được viết sẵn trong các thư viện tiêu đề.


#### Đo độ dài chuỗi

Chúng ta sẽ dùng hàm `strlen()` trong thư viện tiêu đề `string.h` để đo độ dài chuỗi. Ví dụ:

```bash
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    // Yêu cầu người dùng nhập tên
    string name = get_string("Tên: ");
    int length = strlen(name);
    printf("%i\n", length);
}
```

Hàm `strlen()` sẽ tính toán độ dài của chuỗi được truyền vào.


#### Chữ hoa và chữ thường

Dùng hàm `toupper()` function in the `ctype.h` library to convert string into upper case. For example:

```bash
#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Viết thường: ");
    printf("Viết hoa:  ");
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        printf("%c", toupper(s[i]));
    }
    printf("\n");
}
```

Hàm này sẽ lấy chuỗi và chuyển đổi các ký tự trong đó thành chữ hoa. Tương tự, chúng ta có thể sử dụng hàm `tolower()` để chuyển đổi chuỗi thành chữ thường.