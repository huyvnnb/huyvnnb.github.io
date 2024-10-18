---
title: "SOLID và đồng bọn của hắn"
date: 2024-10-18 21:30:00
categories: [Design Pattern]    # TAG names should always be lowercase
---

# SOLID là gì ? Có ăn được không
Tuy solid không ăn được nhưng nó sẽ giúp bạn trở thành một lập trình viên **"PREMIUM"** hơn rất nhiều. Cùng mình tìm hiểu nhé

Mỗi chữ cái đại diện cho một nguyên tắc
- **S**: Single Responsibility Principle (SRP)
- **O**: Open/Closed Principle (OCP)
- **L**: Liskov Substitution Principle (LSP)
- **I**: Interface Segregation Principle (ISP)
- **D**: Dependency Inversion Principle (DIP)

### 1. Single Responsibility Principle (SRP)
> A class should have one, and only one, reason to change.

Điều này có nghĩa là một class chỉ nên xử lý một chức năng nhất định.

Khi class chỉ xử lý một nhiệm vụ, thì sẽ có ít method, biến giúp việc bảo trì trở nên dễ dàng hơn. Ngược lại, nhiều nhiệm vụ thì việc quản lý thôi đã khó, rồi việc phụ thuộc vào nhau khiến bảo trì hay mở rộng trở nên vô cùng vất vả hơn.

#### Code

```java
public class User {
    private String name;
    private String email;

    public User(String name, String email) {
        this.name = name;
        this.email = email;
    }

    public void printUserDetails() {
        System.out.println("Name: " + name + ", Email: " + email);
    }
}
```
Như các bạn đã thấy ở trên thì method printUserDetails không nên nằm trong class User vì ngoài phạm vi xử lý của user. 

Chúng ta có thể loại bỏ method đó và sử dụng trong một class riêng biệt khác như sau

```java
public class UserPrinter {
    public void printUserDetails(User user) {
        System.out.println("Name: " + user.getName() + ", Email: " + user.getEmail());
    }
}
```

Điều này giúp kiểm tra code cũng như bảo trì code tốt hơn.

### 2. Open/Closed Principle (OCP)

> Open for extension, closed for modification

Phương pháp này giúp thêm chức năng mà không ảnh hưởng tới code ban đầu.

Chúng ta hãy xem ví dụ

#### Code

```java
public class DiscountService {
    public double getDiscount(String type) {
        if (type.equals("Regular")) {
            return 0.1;
        } else if (type.equals("Seasonal")) {
            return 0.2;
        } else {
            return 0;
        }
    }
}
```
Nếu ta muốn thêm nhiều loại discount khác thì phải làm thế nào ? Hay là thêm nhiều dòng else if khác ? Điều đó làm cho code trở nên phức tạp và khó mở rộng

Sau khi áp dụng Open/Closed, ta có thể viết như sau

```java
public interface Discount {
    double applyDiscount();
}

public class RegularDiscount implements Discount {
    @Override
    public double applyDiscount() {
        return 0.1;
    }
}

public class SeasonalDiscount implements Discount {
    @Override
    public double applyDiscount() {
        return 0.2;
    }
}

// DiscountService now can be extended without modifying existing code.
public class DiscountService {
    public double getDiscount(Discount discount) {
        return discount.applyDiscount();
    }
}
```
Chúng ta sử dụng một interface để quản lý các loại discount, do đó, khi thêm một loại khác ta chỉ cần implements Discount, còn chức năng bên trong không ảnh hưởng gì tới các class khác.


### 3. Liskov Substitution Principle (LSP)

Trong một chương trình, các object của class con có thể thay thế class cha mà không làm thay đổi tính đúng đắn của chương trình

Hơi khó hiểu? Không sao, mình cũng thấy vậy :D. Hãy tưởng tượng bạn có 1 class cha tên Vịt. Các class Vịt Bầu, Vịt Xiêm có thể kế thừa class này, chương trình chạy bình thường. Tuy nhiên nếu ta viết class Vịt Chạy Pin, cần pin mới chạy được. Khi class này kế thừa class Vịt, vì không có pin không chạy được, sẽ gây lỗi. Đó là 1 trường hợp vi phạm nguyên lý này.

Một ví dụ khác, hay xem đoạn code về xe cộ dưới đây
#### Code
```java
public class Vehicle {

    public int getNumberOfWheels(){
        return 2;
    }
    
    public Boolean hasEngine(){
        return true;
    }
}

public class Car extends Vehicle{
    @Override
    public int getNumberOfWheels(){
        return 4;
    }
}

public class MotorCycle extends Vehicle{
}

public class Main {
    public static void main(String[] args) {
        List<Vehicle> vehicles = new ArrayList<>();
        vehicles.add(new Car());
        vehicles.add(new MotorCycle());
        vehicles.add(new Bicycle());

        for(Vehicle vehicle : vehicles){
            System.out.println(vehicle.hasEngine().toString());
        }
    }
}
```

Chúng ta có 3 class Car, MotorCycle, Bicycle kế thứ class Vehicle, tuy nhiên thì class Bicycle lại vi phạm nguyên tắc LSP do trả về NullPointerException thay vì True/False. Để hiểu rõ hơn, bạn có thế xem video này nhé : https://www.youtube.com/watch?v=129QkkXUHeQ

### 4. Interface Segregation Principle (ISP)
Khi chúng ta thiết kế interface và có class thực thi, sẽ có một số method mà class đó không cần sử dụng đến nhưng bị ép thực thi, điều đó vi phạm ISP

#### Code
```java
public interface Worker {
    void work();
    void eat();  // Robots shouldn't need to implement this method
}

public class HumanWorker implements Worker {
    @Override
    public void work() {
        System.out.println("Human working...");
    }

    @Override
    public void eat() {
        System.out.println("Human eating...");
    }
}

public class RobotWorker implements Worker {
    @Override
    public void work() {
        System.out.println("Robot working...");
    }

    @Override
    public void eat() {
        // This is irrelevant for robots.
    }
}
```
Như bạn có thể thấy, robot không cần ăn do đó interface này chưa hợp lý. Hãy thiết kế lại, chia thành hai interface khác nhau là Workable và Eatable

```java
public interface Workable {
    void work();
}

public interface Eatable {
    void eat();
}

public class HumanWorker implements Workable, Eatable {
    @Override
    public void work() {
        System.out.println("Human working...");
    }

    @Override
    public void eat() {
        System.out.println("Human eating...");
    }
}

public class RobotWorker implements Workable {
    @Override
    public void work() {
        System.out.println("Robot working...");
    }
}
```
Trông có vẻ hiệu quả hơn nhiều đúng không ? 
Bằng việc tách các interfaces nhỏ hơn, cụ thể hơn, mỗi class chỉ phụ thuộc vào các methods mà chúng thực sự cần giúp việc tổ chức code trở tốt hơn.

### 5. Dependency Inversion Principle (DIP)
> High-level modules should not depend on low-level modules; both should depend on abstractions.

Nguyên tắc "Dependency Inversion Principle" khuyến nghị chúng ta nên phụ thuộc vào các abstraction (interfaces), không phụ thuộc vào concretions (các class cụ thể). Điều này giúp giảm sự phụ thuộc trực tiếp giữa các module, giúp code linh hoạt hơn.

```java
public class Keyboard {
    public String getInput() {
        return "User input";
    }
}

public class Printer {
    public void print(String input) {
        System.out.println(input);
    }
}

public class CopyMachine {
    private final Keyboard keyboard;
    private final Printer printer;

    public CopyMachine() {
        this.keyboard = new Keyboard();
        this.printer = new Printer();
    }

    public void copy() {
        String input = keyboard.getInput();
        printer.print(input);
    }
}
```
Như bạn đã thấy thì CopyMachine đã phụ thuộc vào KeyBoard và Printer. Chúng ta có thể sửa code như sau
```java
public interface InputDevice {
    String getInput();
}

public interface OutputDevice {
    void print(String input);
}

public class Keyboard implements InputDevice {
    @Override
    public String getInput() {
        return "User input";
    }
}

public class Printer implements OutputDevice {
    @Override
    public void print(String input) {
        System.out.println(input);
    }
}

public class CopyMachine {
    private final InputDevice inputDevice;
    private final OutputDevice outputDevice;

    public CopyMachine(InputDevice inputDevice, OutputDevice outputDevice) {
        this.inputDevice = inputDevice;
        this.outputDevice = outputDevice;
    }

    public void copy() {
        String input = inputDevice.getInput();
        outputDevice.print(input);
    }
}
```

### Kết luận
Những ví dụ trên minh họa một cách cơ bản về nguyên lý SOLID. Việc áp dụng SOLID có thể yêu cầu chúng ta code dài hơn nhưng giúp logic trở nên dễ hiểu hơn và tính mở rộng, bảo trì code cũng tốt hơn. 

Điều quan trọng nhất khi áp dụng SOLID là không cần phải nguyên tắc áp dụng mọi lúc mọi nơi. Đôi khi, việc đơn giản hóa mã nguồn có thể mang lại lợi ích hơn so với việc tuân thủ một cách mù quáng tất cả các nguyên tắc. Nhưng nếu bạn muốn xây dựng một ứng dụng lớn, phức tạp, thì việc hiểu và áp dụng đúng SOLID sẽ là cần thiết.

---

Dưới đây chỉ là những phần notes của mình khi học được kiến thức mới nào đó, không tránh khỏi việc hiểu sai vấn đề, sai kiến thức nghiêm trọng, do đó mong nhận được sự góp ý từ mọi người để mình có thể hiểu sâu hơn về những kiến thức này. Xin chân thành cảm ơn mọi người.

### Tài liệu tham khảo

- https://blog.algomaster.io/p/solid-principles-explained-with-code
- https://viblo.asia/p/solid-la-gi-nguyen-tac-lap-trinh-solid-va-cach-ap-dung-chung-3kY4gEG9LAe
