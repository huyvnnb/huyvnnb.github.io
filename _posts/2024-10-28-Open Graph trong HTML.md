---
title: "Open Graph trong HTML"
date: 2024-10-18 21:30:00
categories: [Design Pattern]    # TAG names should always be lowercase
---
### Open Graph có gì hay ?

Open Graph là một giao thức cho phép bạn kiểm soát cách nội dung của trang web hiển thị khi được chia sẻ trên các nền tảng mạng xã hội như Facebook, LinkedIn, Twitter, v.v. Nhờ Open Graph, bạn có thể tùy chỉnh tiêu đề, mô tả, hình ảnh đại diện, và nhiều thông tin khác để thu hút người xem tốt hơn.

### Cách Thêm Thẻ Open Graph

Để sử dụng Open Graph, bạn chỉ cần thêm các thẻ `<meta>` vào phần `<head>` trong HTML của trang web. Dưới đây là các thẻ Open Graph quan trọng thường dùng:

```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang Web của Tôi</title>
    
    <!-- Các thẻ Open Graph -->
    <meta property="og:title" content="Machine Learning Workshop" />
    <meta property="og:description" content="School for Machines Who Can't Learn Good and Want to Do Other Stuff Good Too" />
    <meta property="og:image" content="http://www.machinelearningworkshop.com/image/all.png" />
    <meta property="og:image:alt" content="Black and white line drawing of refrigerator, french door refrigerator, range, washer, fan, microwave, vaccuum, space heater and air conditioner" />
</head>
<body>
    <h1>Chào mừng đến với trang web của tôi!</h1>
</body>
</html>
```

![Nội dung hiển thị](https://web.dev/static/learn/html/metadata/image/facebook-card-machine-le-645e337e0cb1f_960.png)


`og:title`: Tiêu đề của trang khi được chia sẻ.

`og:description`: Mô tả ngắn về trang, giúp người xem hiểu nội dung khi chưa truy cập vào.

`og:image`: Đường dẫn đến hình ảnh đại diện của trang. Nên sử dụng ảnh có kích thước ít nhất 1200x630 pixel.

### Lưu Ý Khi Sử Dụng Open Graph
Ảnh chất lượng cao: Chọn ảnh có độ phân giải cao để đảm bảo hình ảnh hiển thị đẹp khi chia sẻ.

Cập nhật thông tin đúng: Đảm bảo nội dung trong các thẻ Open Graph chính xác và cập nhật nếu trang thay đổi.

Dùng thẻ `og:type` phù hợp: Chọn loại nội dung đúng với nội dung của trang.

Với Open Graph, bạn sẽ có toàn quyền kiểm soát cách nội dung của mình hiển thị trên các nền tảng mạng xã hội, giúp tăng cường trải nghiệm người dùng và thu hút lượt truy cập nhiều hơn!

Hy vọng hướng dẫn này sẽ giúp bạn dễ dàng triển khai Open Graph trên trang web của mình.

### Tài liệu tham khảo

https://web.dev/learn/html/metadata?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fhtml%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fhtml%2Fmetadata