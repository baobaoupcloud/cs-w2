---
title : "Trạng thái kết thúc"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---
Khi một chương trình kết thúc, một mã thoát đặc biệt được cung cấp cho máy tính.

Khi một chương trình kết thúc mà không có lỗi, mã trạng thái `0` được cung cấp cho máy tính. Thông thường, khi xảy ra lỗi dẫn đến kết thúc chương trình, mã trạng thái `1` được cung cấp cho máy tính.

Ví dụ: viết một chương trình C có tên `status.c` như sau:

```bash
#include <cs50.h>
#include <stdio.h>

int main(int argc, string argv[])
{
    if (argc != 2)
    {
        printf("Thêm một đối số dòng lệnh\n");
        return 1;
    }
    printf("chào %s\n", argv[1]);
    return 0;
}
```

Sau đó, chạy chương trình bằng cách nhập `./status bạn`, chúng ta sẽ nhận được mã trạng thái `0` với kết quả trả ra là `chào bạn`. Nếu bạn không cung cấp bất kỳ đối số nào, chẳng hạn như chỉ nhập `./status`, chúng ta sẽ nhận được mã trạng thái `1` với cảnh báo `Thêm một đối số dòng lệnh`.