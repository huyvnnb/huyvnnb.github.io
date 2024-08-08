---
title: "Các thiết bị mạng phổ biến và công dụng của chúng"
<<<<<<< HEAD
date: 2024-08-08 13:08:00
=======
date: 2024-08-08 07:14:00
>>>>>>> 6d8b4cf71f9983e41e2fc3e8cbe9a93b6885c267
categories: [CCNA]
---

## Thiết bị mạng là gì ?

Thiết bị mạng, hay còn gọi là network devices, theo cách hiểu đơn giản nhất thì đó là những thiết bị vật lý được kết nối với nhau, dùng để kết nối, truyền đi những gói tin từ thiết bị nguồn (source) đến thiết bị đích (destination). Ngoài việc truyền tin, chúng có thể dùng để phân giải (đổi tên miền [example.com](https://example.com) sang địa chỉ IP), ngăn chặn traffic đáng ngờ (firewall,…) và còn rất nhiều chức năng khác nữa.

![Thiết bị mạng](https://cdn.educba.com/academy/wp-content/uploads/2019/08/Networking-Devices.jpg)

## Các thiết bị mạng phổ biến và chức năng của chúng

### I. Hub

![Hub](https://static.javatpoint.com/computer/images/what-is-star-topology1.png)

Hub là một thiết bị mạng cơ bản được sử dụng để kết nối nhiều thiết bị (như máy tính, máy in,...) lại với nhau trong cùng một mạng **LAN (Local Area Network)**. Bạn có thể hiểu nếu bạn gửi một gói tin đi đến ngã tư, thì Hub sẽ chuyển gói tin đó ra cả 3 hướng còn lại. Tuy nhiên, vì nó “HẤP” cho nên ngày nay người ta thường không sử dụng vì hiệu suất truyền dữ liêu thấp, bảo mật không cao. Bởi bạn muốn nói chuyện với người A, những vì bạn nói quá to nên cả người B, C cũng nghe thấy được. Thay vào đó, họ dùng Switch bởi vì nó thông minh hơn.

### 2. Switch (Bộ chuyển mạch)

![Switch](https://juniper-prod.scene7.com/is/image/junipernetworks/4100-mg-48p-front-top-switches-banner?fmt=png8-alpha&wid=1280&dpr=off)

Switch là một thiết bị mạng thông minh, đóng vai trò trung tâm trong việc kết nối các thiết bị trong một mạng LAN (Local Area Network). Khác với hub, vì switch cần phải học hỏi nên nó thông mình hơn, bằng công nghệ nào đó giúp nó học địa chỉ MAC (địa chỉ riêng biệt của mỗi thiết bị), qua đó giúp nó biết mình cần truyền dữ liệu chính xác đến đâu dựa vào thông tin có trong gói tin mà nó nhận được.

### 3. Router

Router, hay bộ định tuyến, đóng vai trò quan trọng trong việc kết nối các mạng máy tính khác nhau.

- **Kết nối đa mạng**: Router nối liền các mạng con thành một mạng lớn hơn. Ví dụ, router giúp kết nối mạng LAN trong nhà bạn với mạng Internet toàn cầu.
- **Chuyển tiếp thông tin**: Khi bạn truy cập một trang web, router sẽ nhận các gói dữ liệu từ máy tính của bạn và tìm đường đi ngắn nhất để gửi đến máy chủ chứa trang web đó.
- **NAT (Network Address Translation)**: tiết kiệm địa chỉ IP và bảo vệ mạng nội bộ, router sử dụng NAT. NAT dịch các địa chỉ IP riêng tư trong mạng LAN (ví dụ: 192.168.1.100) thành địa chỉ IP công cộng khi giao tiếp với Internet.

Tóm lại, router là một thiết bị mạng không thể thiếu, giúp cho các thiết bị trong mạng có thể giao tiếp với nhau và truy cập Internet một cách hiệu quả

![Router]([https://www.researchgate.net/publication/298834060/figure/fig1/AS:669014497972231@1536516894585/Network-topology-used-for-testing-XP-router-in-home-small-corporate-network-environment.png](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSG4TcYBt6VHf55L6SINh9y64AdbeUe0dVHew&s))

### 4.Firewall

Tường lửa (Firewall) là một hệ thống bảo mật mạng có chức năng giám sát và kiểm soát lưu lượng dữ liệu đi vào và đi ra khỏi một mạng hoặc một thiết bị. Nó hoạt động như một bức tường lửa ngăn chặn các cuộc tấn công từ bên ngoài, bảo vệ dữ liệu và hệ thống của bạn khỏi những mối đe dọa an ninh mạng.

Ở trường mình, mỗi khi đến kì thi, nhà trường sẽ bật tường lửa, ngăn chạn việc kết nối giữa laptop với internet.

![Firewall](https://www.simplilearn.com/ice9/free_resources_article_thumb/Firewall_1.png)

### 5. Cáp mạng

Đây là thiết bị không thể thiếu được trong việc kết nối mạng máy tính với nhau. Cáp ở đây có thể là đồng hoặc có thể là ánh sáng phục vụ nhiều mục đích khác nhau.

Có ba loại cáp chính:

#### Cáp đồng trục (Coaxial cable)

![Coaxial cable](https://www.telnetww.com/wp-content/uploads/2020/05/coaxial-cable-diagram-1-1024x686.png)

- **Cấu tạo**: 
    - **Lõi dẫn điện trung tâm**: Đây là dây dẫn chính truyền tải tín hiệu.
    - **Chất cách điện**: Một lớp vật liệu cách điện bao quanh lõi dẫn để ngăn chặn tín hiệu rò rỉ.
    - **Lớp chắn bảo vệ**: Một lớp kim loại dạng lưới hoặc ống bao quanh lớp cách điện, giúp ngăn chặn nhiễu điện từ xâm nhập vào cáp.
    - **Vỏ nhựa bên ngoài**: Lớp vỏ bảo vệ các thành phần bên trong khỏi tác động môi trường.
- Ứng dụng: Truyền tín hiệu truyền hình


#### Cáp xoắn đôi (Twisted pair)

![Twisted pair](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRH4DZfIbdOwGaduL8oBJAPnWx2dqhV2SY6qQ&s)

Đây cũng là một trong những phương tiện phổ biến và lâu đời nhất, được sử dụng trong công nghệ Ethernet. 
- **Cấu tạo**: Gồm 2 - 4 cặp xoắn đôi vào nhau. Khi các dây dẫn song song chạy gần nhau, chúng sẽ tạo ra một từ trường tương tác, gây ra nhiễu. Bằng cách xoắn các dây dẫn, từ trường được tạo ra sẽ triệt tiêu lẫn nhau, giảm thiểu nhiễu.

- **Phân loại**: 
    - Cáp UTP (Unshielded Twisted Pair): Là loại cáp xoắn đôi không có lớp chắn bên ngoài. Đây là loại cáp phổ biến nhất, giá thành rẻ và dễ lắp đặt.
    - Cáp STP (Shielded Twisted Pair): Là loại cáp xoắn đôi có lớp chắn bên ngoài, thường là một lớp foil hoặc lưới kim loại. Lớp chắn này giúp tăng cường khả năng chống nhiễu, phù hợp với môi trường có nhiều nhiễu điện từ.

Cáp xoắn đôi được chia thành nhiều mục khác nhau trải dài từ CAT 1 – 7 (CAT trong Categories).
Ngoài ra có hai tiêu chuẩn mạng phổ biến được sử trong mạng LAN, đó là:
- 100BASE-TX / Fast Ethernet (speed 100 Mbps)
- 1000BASE-T / Gigabit Ethernet (1 Gbps)


**Ứng dụng**: Truyền tải trong mạng LAN

#### Cáp quang (Fiber optic cable)

![Fiber optic cable](https://zmscable.es/wp-content/uploads/2022/12/fibra-optica-cable.jpg)

**Cấu tạo**: Cấu thành từ nhiều sợi thủy tỉnh giúp chuyển tín hiệu một khoảng cách rất xa, có ba thành phần chính
- Lõi
- Lớp phản xạ ánh sáng
- Lớp vỏ bảo vệ chính

Cáp quang có nhiều ưu điểm so với các loại khác như tốc độ cao, khoảng cách xa, ổn định, không bị nhiễu điện từ tuy nhiên giá thành lại cao. Để hiểu được cách nó truyền tín hiệu, bạn hãy nhớ lại kiến thức quang học trong chương trình lớp 11 cũ, đó là nhờ tính chất phản xạ toàn phần, các bạn có thể tìm hiểu thêm.

Có hai loại chính đó là **Single-mode** và **Multi-mode**: 
- **Single-mode** chỉ cho phép truyền 1 kênh duy nhất thường để truyền tín hiệu ở rất xa (hàng trăm km)
- **Multi-mode** có thể truyền nhiều kênh, truyền tín hiệu <5km

Trên đây chỉ là những nội dung cơ bản về những thiết bị mạng phổ biến và chức năng phổ biến nhất. Nếu có gì chưa rõ, mọi người có thể tìm hiểu thêm ở những tài liệu sau:

[Fiber optic cable](https://www.ofsoptics.com/faq-guide-to-fiber-optic-cable/)

[Cáp quang](https://netsystem.vn/cap-quang-la-gi-doi-net-ve-cac-thanh-phan-dau-noi-45/)

[Network devices overview](https://www.lepide.com/blog/the-most-common-types-of-network-devices/)

[Firewall](https://us.norton.com/blog/privacy/firewall)

[Twisted pair](https://stl.tech/blog/network-connectivity-with-twisted-pair-cables/)

---

Hy vọng mọi người sẽ tiếp tục ủng hộ các bài viết tiếp theo của mình. Các bạn có thể liên hệ mình qua:

- [Gmail](mailto:huyqktk@gmail.com) 
- [Linkedin](https://www.linkedin.com/in/huy-nguyen-38910020b/)
- [Github](https://github.com/huyvnnb)

Xin cảm ơn mọi người !




