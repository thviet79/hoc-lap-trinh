---
title: "Thao tác với chuối trong C"
description: "Thao tác với chuối trong C"
keywords:
  ["học lập trình c", "khoá học lập trình c", "Khoá học lập trình c căn bản"]
chapter:
  name: "Strings"
  slug: "chuong-08-strings"
category:
  name: "C"
  slug: "c"
image: https://user-images.githubusercontent.com/29374426/127596066-fa46df01-982f-4a72-b6d1-f7d8f5c5a9b3.png
position: 2
---

Trong bài học này, ta sẽ học cách thao tác với các chuỗi trong C bằng cách sử dụng các hàm thư viện như `gets()`, `puts()`, `strlen()` v.v. Ta cũng sẽ học cách lấy chuỗi từ người dùng và thực hiện các thao tác trên chuỗi.

## Các hàm tương tác với chuỗi trong C

Chúng ta cần phải thường xuyên thao tác các chuỗi tùy theo nhu cầu của đề bài. Hầu hết, việc ta thao tác chuỗi có thể được thực hiện thủ công nhưng điều này làm cho việc lập trình trở nên phức tạp.

Để giải quyết vấn đề này, C hỗ trợ một số lượng lớn các hàm xử lý chuỗi trong thư viện `string.h`.

Một số hàm xử lí chuỗi thường được sử dụng

|    Hàm     | Mục đích                           |
| :--------: | ---------------------------------- |
| `strlen()` | tính độ dài chuỗi                  |
| `strcpy()` | sao chép một chuỗi sang chuỗi khác |
| `strcmp()` | so sánh hai chuỗi                  |
| `strcat()` | nối hai chuỗi                      |
| `strlwr()` | chuyển đổi chuỗi thành chữ thường  |
| `strupr()` | chuyển đổi chuỗi thành chữ hoa     |

> Lưu ý: trước khi dùng các hàm xử lí chuỗi trên thì hãy khai báo thư viện chuỗi bằng syntax:

```c
#include <string.h>
```

### gets(), puts()

Các hàm `gets()` và `puts()` là hai hàm chuỗi để lấy đầu vào chuỗi từ người dùng và hiển thị chuỗi đó

Ví dụ:

```c
#include<stdio.h>

int main()
{
    char name[30];
    printf("Enter name: ");
    gets(name);
    printf("Name: ");
    puts(name);
    return 0;
}
```

Kết quả:

```c
Enter name: Hello Anest
Name: Hello Anest
```

> Mặc dù hai hàm `gets()` và `puts()` là các hàm xử lí chuỗi nhưng chúng đều được khai báo trong thư viện `<stdio.h>`
