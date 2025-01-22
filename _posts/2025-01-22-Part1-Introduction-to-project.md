---
title: "Tutorial #1: Giới thiệu tổng quan về project Blognest"
date: 2024-06-05 09:05:00
categories: [SpringBoot]    
---

# #1 Giới thiệu tổng quan về project Blognest

Chào mọi người,

Sau một thời gian học Spring, mình quyết định thực hiện một dự án nhỏ để củng cố và áp dụng các kỹ năng đã học. Series này sẽ ghi chép lại toàn bộ quá trình xây dựng một trang blog cơ bản với Spring Framework, giúp mình cũng như các bạn học hỏi và thực hành nhiều kiến thức bổ ích.

Mặc dù đây chỉ là một **Pet Project**, mình vẫn rất mong muốn nhận được những đóng góp và phản hồi từ mọi người để cùng nhau hoàn thiện và cải thiện hơn nữa. 

## I. Khởi Tạo Project

Để bắt đầu, chúng ta sẽ sử dụng [Spring Initializr](https://start.spring.io/) để tạo ra cấu trúc dự án ban đầu. Đây là một công cụ cực kỳ hữu ích, giúp bạn khởi tạo nhanh chóng một dự án Spring với các thông tin cơ bản.

![](https://huongdanjava.com/wp-content/uploads/2016/10/tao-moi-spring-boot-project-su-dung-spring-initializr-web-1.png)

### Các bước khởi tạo:

1. **Chọn Project**: Mình chọn **Maven** vì đây là công cụ build phổ biến trong cộng đồng Java, giúp quản lý các phụ thuộc (dependencies) dễ dàng.
2. **Chọn Language**: Chọn **Java** vì dự án này sử dụng Java làm ngôn ngữ chính.
3. **Chọn Spring Version**: Phiên bản Spring mình sử dụng là **3.4.1** (tính đến thời điểm này).
4. **Điền thông tin metadata**:
   - **Group**: Đây là tên tổ chức hoặc tên miền (thường viết ngược lại, ví dụ: com.example).
   - **Artifact**: Tên của dự án (mình có thể gọi là `spring-blog` chẳng hạn).
   - **Packaging**: Chọn **Jar** vì đây là ứng dụng Java thông thường, không phải ứng dụng web phân tán.
   - **Java**: Chọn **21** để sử dụng phiên bản mới gần nhất của Java.
5. **Chọn Dependencies**: Lúc này, mình chỉ cần chọn **Spring Web** vì đây là yêu cầu cơ bản để xây dựng một ứng dụng web. Các dependencies khác có thể thêm vào sau khi cần.

Sau khi điền xong các thông tin trên, nhấn **Generate** để tạo ra project. Bạn sẽ tải về một file nén, giải nén nó và mở bằng **IntelliJ IDEA Community Edition** (hoặc bất kỳ IDE nào bạn thích).

### Các bước tiếp theo:

Sau khi mở project trong IntelliJ, bạn sẽ thấy cấu trúc thư mục mặc định của một ứng dụng Spring, bao gồm:
- `src/main/java`: Chứa mã nguồn của dự án.
- `src/main/resources`: Chứa các tài nguyên như file cấu hình (application.properties).
- `pom.xml`: File cấu hình Maven chứa thông tin về các dependencies và plugin.

### Các phần tiếp theo:

Bài tiếp theo trong series này sẽ đi sâu vào việc cấu hình Spring và xây dựng các lớp cơ bản cho dự án blog này. Mình sẽ hướng dẫn cách tạo các class như Controllers, Services, và Repositories để xây dựng tính năng cho blog, cũng như các kiến thức cơ bản về Spring Boot như Dependency Injection, Routing, và Configuration.

Mong các bạn sẽ theo dõi series và đừng ngần ngại để lại ý kiến đóng góp giúp mình hoàn thiện hơn nhé!

---

Hẹn gặp lại ở bài tiếp theo!
