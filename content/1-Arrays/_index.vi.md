---
title : "Mảng"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Mảng** là một danh sách các giá trị được lưu trữ liên tiếp trong bộ nhớ máy tính.

Để tạo một mảng trong ngôn ngữ C, đầu tiên xác định kiểu dữ liệu cho mảng và tạo một tên cho mảng đó. Sau đó thêm vào `[]` số lượng phần tử mà mảng có thể chứa. Cuối cùng thêm các phần tử vào mảng theo số chỉ mục. Chỉ số mảng bắt đầu từ 0: `[0]` sẽ là phần tử đầu tiên, `[1]` là phần tử thứ hai,...

Ví dụ tạo mảng `scores`: 

```bash
int scores[3];
scores[0] = get_int("Điểm: ");
scores[1] = get_int("Điểm: ");
scores[2] = get_int("Điểm: ")
```

`int scores[3]` thông báo trình biên dịch cung cấp ba vị trí liền kề trong bộ nhớ có kích thước `int` là số nguyên để lưu trữ ba phần tử `scores`.

Sau đó chúng ta dùng `get_int` để lấy `Điểm` gán cho các phần tử `scores`.

Chúng ta còn có thể cải thiện mã thành:

```bash
int scores[3];
    for (int i = 0; i < 3; i++)
    {
        scores[i] = get_int("Điểm: ");
    }
```

Số chỉ mục `i` sẽ lặp 0 → 2 để lấy ba phần tử của mảng `scores`