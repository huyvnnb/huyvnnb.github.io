---
title: "Giới thiệu về cấu trúc dữ liệu"
date: 2024-06-05 09:05:00
categories: [DSA, Data Structure]    # TAG names should always be lowercase
---

### **Giới thiệu**

Cấu trúc dữ liệu và Giải thuật **(DSA - Data Structure and Algorithms)** là cách chúng ta thực hiện lưu trữ, tổ chức dữ liệu và thiết kế thuật toán để giải quyết một vấn đề nào đó. Tùy vào từng vấn đề mà ta chọn cách lưu trữ và sử dụng giải thuật phù hợp.

Để học được CTDL&GT, bạn cần:
- *Nắm chắc cú pháp một ngôn ngữ lập trình*: C, C++, Java, Python (mình sử dụng C++ vì có nhiều thư viện hỗ trợ, giúp học tập tốt hơn).
- *Học theo trình tự hợp lý*: Học các cấu trúc dữ liệu và cách thực thi nó, sau đó sẽ học sang các thuật toán.
- Cần đam mê, chăm chỉ, luyện tập nhiều.

---

### **Các cấu trúc dữ liệu phổ biến**

<!-- ![Data Structure](/_site/assets/img/img-ds/ds.jpg) -->

#### Array
- Mảng là một cấu trúc dữ liệu tuyến tính **(linear data structure)**, lưu trữ một tập hợp các giá trị cùng kiểu dữ liệu, liên tiếp nhau trên bộ nhớ, điều này cho phép truy cập dữ liệu với thời gian hằng số **(constant-time)**.
- Phổ biến nhất là mảng 1 chiều và mảng 2 chiều (Matrix)

#### String
- Chuỗi có bản chất là một mảng gồm các kí tự kiểu char. Kiểu dữ liệu string cho phép thao tác và xử lí các chuỗi văn bản

#### Linked List
- Là cấu trúc tuyến tính, lưu trữ giá trị dưới các Node, và được liên kết với nhau bởi con trỏ ( C, C++) hoặc sử dụng đối tượng (class) và tham chiếu (references) trong Java. 
- Khác với mảng, DSLK không lưu các giá trị liên tiếp nhau, mà được cấp phát ngẫu nhiên trong bộ nhớ.

#### Stack
- Kiểu dữ liệu hoạt động theo cơ chế Last In First Out (LIFO), giống như kiểu chồng sách vậy. VD: Muốn lấy giá trị cuối cùng, ta cần loại bỏ hết giá trị ở phía trên.
- Có thể dùng Mảng hoặc DSLK để thực thi.

#### Queue
- Hoạt động giống cách chúng ta xếp hàng. Ai đến trước thì được thực hiện trước.
- Thực thi bằng Mảng hoặc Danh sách liên kết.

#### Tree
- Nghe tree là chúng ta biết nó sẽ như thế nào rồi đúng không. Tree sẽ gồm các Node gọi là Node cha, và từ đó sẽ ra các Node con, và cứ thế.
- Ví dụ: Tổ chức file trong máy tính, phân cấp quyền,..

#### Heap
- Dữ liệu sẽ được lưu trữ theo quy tắc nhất định. Với Max Heap, Node cha luôn lớn hơn các Node con, còn Min Heap thì Node cha luôn nhỏ hơn Node con.
- Dùng để thực thi Priority Queue.

#### Set
- Lưu trữ các giá trị phân biệt.
- VD: [1,2,3,4] , không tồn tại [**1**,2,3,4,**1**] trong *set*, nhưng trong *multiset* thì có

### Map
- Lưu giá trị theo kiểu **{KEY : VALUE}**

### Graph
- Cấu trúc phi tuyến tính, đồ thị bao gồm hữu hạn các **Đỉnh (Vertices)** và **Cạnh (Edge)** liên kết với nhau
- Ví dụ: Mạng xã hội, mạng máy tính, hay **Google Maps**.

Mình đã liệt kê cho các bạn một số cấu trúc dữ liệu phổ biến. Ở [bài sau](https://huyvnnb.github.io), mình sẽ liệt kê các thuật toán liên quan đến các cấu trúc dữ liệu. Cảm ơn mọi người đã đọc bài viết của mình.