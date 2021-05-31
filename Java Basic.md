# Java Basic
## 1. Khởi đầu
- Khai báo class và main
- print: System.out.println("Hello world")
![](https://i.imgur.com/x1MyNp5.png)

## 2. Khai báo biến
Primitive data types:
- String: String MyName = "Thanh";
- int: int Speed = 120;
- char: char Key = 'T';
- boolean: B = true;
- float: float T = 3.14f;
- Convert Double to int: int Myint = (int)myDouble;

## 3. String
- in độ dài: System.out.println(text.length())
- In Hoa: System.out.println(text.toUpperCase())
- Ghép hai chuỗi: "+" hoặc
```java=
    - String firstName = "John ";
    - String lastName = "Doe";
    - System.out.println(firstName.concat(lastName))
```
- Trả về index chữ "e" trong chuỗi:
```java=
    - String txt = "Hello Everybody";
    - System.out.println(txt.indexOf("e"))
```
## 4. Toán
- Max: Math.max(x,y); 
- Căn: Math.sqrt(x); -> căn(x)
- random [0,1]: Math.random()

## 5. If...else
```java=
- if(x>y){}
- if(x==y){} else {}
- if(x==y){} 
    else if(x>y){}
    else{}
    
- (a<b)?a:b
    - int time = 20;
    - String resul = (time<18)?"Good day":"bad day";
    - System.out.println(result)
```
## 6. Switch case
```java=
- int day = 2;
- switch(day){
case 1:
    ....
    break;
case 2:
    ....
    break;
default:
    ....

}
```
## 7. Vòng lặp
### 1. While
```java=
- int i = 1;
- while(i<6){
    ....
    i++;
}
```
### 2. Do - While
```java=
- int i = 1;
do{
  System.out.println(i);
  i++;
}
while (i < 6);
```
### 3. For
```java=
for(int i = 0; i < 5; i++) {
  System.out.println("Yes");
}
```
### 4. Lặp qua các mục trong mảng
```java=
String[] cars = {"xe dap","xe may","xe honda"};
for (String i: cars){
    System.out.println(i);
}
```
## 8. Array
- String[] cars = {"xe may","xe honda"}
- Tìm độ dài: System.out.println(cars.length)
- 2 chiều: int[][];

## 9. Phương thức trong Java
```java=
static void Mymethod(){
    System.out.println("I'm Thanh and handsome");
}

public static void main(String[] args){
    Mymethod();
}
```
- Ví dụ: cho phép trùng tên những khác **data type**
```java=
static int plusMethod(int x, int y) {
  return x + y;
}

static double plusMethod(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethod(8, 5);
  double myNum2 = plusMethod(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```
- Ví dụ đệ quy:
```java=
public class Main {
  public static void main(String[] args) {
    int result = sum(10);
    System.out.println(result);
  }
  public static int sum(int k) {
    if (k > 0) {
      return k + sum(k - 1);
    } else {
      return 0;
    }
  }
}
```
## 10. Class/object
- Tạo Class tên MyClass: public class MyClass
- Tạo đối tượng Obj thuộc MyClass:
    - MyClass Obj = new MyClass();

- Use myObj to access and print the value of the x attribute of MyClass: 
```java=
    - public class MyClass {
          int x = 5;
    - public static void main(String[] args) {
        MyClass myObj = new MyClass();
        System.out.println(myObj.x);
            }
        }
```
- Tạo class constructor (lớp con)
```java=
// Create a MyClass class
public class MyClass{
  int x;  // Create a class attribute x

  // Create a class constructor for the MyClass class
  public MyClass() {
    x = 5;  // Set the initial value for the class attribute x to 5
  }

  public static void main(String[] args) {
    // Create an myObj object of class MyClass (This will call the constructor)
    MyClass myObj = new MyClass(); 
    // Print the value of x
    System.out.println(myObj.x);
  }
}
```
- Không cho phép thừa hưởng bởi class khác: final class Myclass
- import thư viện: import java.util.Scanner
- **Car** class thừa hưởng từ **Vehical** Class: class Car extends Vehicle

## 11. Xử lý ngoại lệ (try - catch)
- Ngoại lệ 1:
```java=
try
 {
  int[] myNumbers = {1, 2, 3};
  System.out.println(myNumbers[10]);
} 
catch
 (Exception e) {
  System.out.println("Something went wrong.");
}
```
- Ngoại lệ 2: sau khi hoàn thành try-catch sẽ trả về:
```java=
try {
  int[] myNumbers = {1, 2, 3};
  System.out.println(myNumbers[10]);
} catch (Exception e) {
  System.out.println("Something went wrong.");
} 
finally{
  System.out.println("The 'try catch' is finished.");
}
```
- Ném ngoại lệ: **throw**
```java=
public class Main {
  static void checkAge(int age) { 
    if (age < 18) {
      throw new ArithmeticException("Access denied - You must be at least 18 years old."); 
    } else {
      System.out.println("Access granted - You are old enough!"); 
    }
 } 
 
 public static void main(String[] args) { 
   checkAge(15); 
 } 
}
```
![](https://i.imgur.com/S8GOzpY.png)
![](https://i.imgur.com/SCzTFMU.png)

## 12. Thuộc tính trong Class
- Gọi một class trong một class khác
```java=
public class Main {
  int x = 5;
}

class Second {
  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```
- Thuộc tính trong class: x, y là 2 thuộc tính của class Main
```java=
public class Main {
  int x = 5;
  int y = 3;
}
```
- Truy xuất thuộc tính: "." và làm thay đổi nó
```java=
public class Main {
  int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // x is now 25
    System.out.println(myObj.x);
  }
}
```
- Truy xuất thuộc tính nhưng k thay đổi được: "final"
```java=
public class Main {
  final int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // will generate an error: cannot assign a value to a final variable
    System.out.println(myObj.x);
  }
}
```
- Như là **copy bề mặt**
```java=
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    myObj2.x = 25;
    System.out.println(myObj1.x);  // Outputs 5
    System.out.println(myObj2.x);  // Outputs 25
  }
}
```
## 13. Phương thức trong Class
- myMethod() là phương thức trong class Main
```java=
public class Main {
  static void myMethod() {
    System.out.println("Hello World!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}

// Outputs "Hello World!"
```
### 1. Static và Non-Static
- Sự khác nhau giữa Static và Public: 
    - Static: có thể được truy xuất mà k cần tạo đối tương
    - Public phải cần tạo đối tượng mới truy xuất được 
```java=
public class Main {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }

  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // Call the static method
    // myPublicMethod(); This would compile an error

    Main myObj = new Main(); // Create an object of Main
    myObj.myPublicMethod(); // Call the public method on the object
  }
}
```
![](https://i.imgur.com/yVcgA1q.png)
### 2. Multiple Classes
```java=
public class Main {
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }
}

class Second {
  public static void main(String[] args) {
    Main myCar = new Main();     // Create a myCar object
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.speed(200);          // Call the speed() method
  }
}
```
![](https://i.imgur.com/LB8VHK3.png)

### 3. Constructors: 1 special method để khởi tạo các đối tượng, tạo những thuộc tính đầu tiên cho đối tượng đó 
- Tên của constructors phải trung tên class (chỉ có 1 constructor trong 1 class)
- Constructor được gọi khi object được tạo
- Constructor k có data type (public Main)

```java=
// Create a Main class
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  public static void main(String[] args) {
    Main myObj = new Main(); // Create an object of class Main (This will call the constructor)
    System.out.println(myObj.x); // Print the value of x
  }
}

// Outputs 5
```
- Khởi tạo tham số trong Constructor
```java=
public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}

// Outputs 1969 Mustang
```
## 14. Modifiers: những công cụ sửa đổi
- **Public** là một keyword được phép **truy cập chỉnh sửa**
- Modifiers chia thành 2 lớp:
    - Access modifiers: kiểm soát mức độ truy cập
    - Non-Access modifiers: do not control access level, but provides other functionality
### 1. Access Modifiers
- public: có thể được truy cập bởi tất cả các class
- default: Trong cùng Package
- private: Trong cùng class
- protected: trong cùng **Package** và **Subclass**(kế thừa(extends) từ cha nó)
![](https://i.imgur.com/Xb5awKB.png)

### 2. Non-Access Modifiers
- final: Không cho phép **kế thừa**
- abstract: Không thể tạo được object, chức nắng cho các class khác kế thừa
- static: những thuộc tính, phương thức thuộc class chứ k phải là của những đối tượng (có thể được truy xuất mà k cần tạo đối tượng)
- Abstract methods: Chỉ dùng trong Abstract class, không có body (abstract void run()), body được cung cấp bởi 1 subclass 
- Transient: Những thuộc tính và phương thức bị bỏ qua khi **tuần tự hoá** đối tượng chứa chúng
- synchronized: Những phương thức chỉ có thể được truy cập bởi một lượng trong 1 thời điểm
- volatile: giá trị một thuộc tính không được lưu vào bộ đệm cục bộ, mà được đọc từ bộ nhớ chính
![](https://i.imgur.com/0yeiEXL.png)
- Ví dụ cho **final**
![](https://i.imgur.com/uf8w7si.png)

- Ví dụ: abstract class
```java=
// Code from filename: Main.java
// abstract class
abstract class Main {
  public String fname = "John";
  public int age = 24;
  public abstract void study(); // abstract method
}

// Subclass (inherit from Main)
class Student extends Main {
  public int graduationYear = 2018;
  public void study() { // the body of the abstract method is provided here
    System.out.println("Studying all day long");
  }
}
// End code from filename: Main.java

// Code from filename: Second.java
class Second {
  public static void main(String[] args) {
    // create an object of the Student class (which inherits attributes and methods from Main)
    Student myObj = new Student();

    System.out.println("Name: " + myObj.fname);
    System.out.println("Age: " + myObj.age);
    System.out.println("Graduation Year: " + myObj.graduationYear);
    myObj.study(); // call abstract method
  }
}
```
![](https://i.imgur.com/Qy1vvM2.png)
## 15. Encapsulation: Bao đóng
- Để đảm bảo các dữ liệu nhạy cảm từ người dùng
- Khai báo các thuộc tính là Private
- Cung cấp public get and set method để update các thuộc tính private
### 1. Get and set method
```java=
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```
## 15. Package AND API
- Package: để group những cái classes có liên quan nhau
- Có 2 loại
    - Gói tích hợp sản từ Java API: thư viện các classes viết sẳn
    - Gói người dùng tự định nghĩa
- Library chia làm Packages và classes: tức là có thể import class đơn thay vì all class trong 1 package
![](https://i.imgur.com/77ol26I.png)
### 1. Packages có sẳn
- Ví dụ: class Scanner năm trong package java.util
![](https://i.imgur.com/TXwZ89h.png)
- Để sử dụng class **Scanner** ta tạo một đối tượng của nó để sử dụng các thuộc tính của class đó
![](https://i.imgur.com/J0EpaEx.png)
- Import all class của package java.util
![](https://i.imgur.com/BZdFOKd.png)

### 2. Package người dùng tự định nghĩa
![](https://i.imgur.com/CMQ6K3i.png)
![](https://i.imgur.com/mumjaxY.png)
![](https://i.imgur.com/TCk9FXp.png)

## 16. Kế thừa (Inheritance)
### 1. extends
- class **Car** kế thừa từ class **Vehicle** bằng **extends** keyword
```java=
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```
![](https://i.imgur.com/o3pZ3oP.png)

### 2. final
- Không cho phép kế thừa (class type)
- Không cho phép sửa đổi (atribute type)
```java=
final class Vehicle {
  ...
}

class Car extends Vehicle {
  ...
}
```
![](https://i.imgur.com/DeUCq0n.png)

## 17. Tính đa hình (Polymorphism)
- Pig, Dog kế thừa từ Animal nhưng lại có phương thức

```java=
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```
![](https://i.imgur.com/bnqNJVf.png)


## 18. Class bên trong Class
### 1. Mục đích
- Mục đích cho điều này là tính dễ đọc và dễ bảo trì
```java=
class OuterClass {
  int x = 10;

  class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}

// Outputs 15 (5 + 10)

```
### 2. Private inner class
- Class bên ngoài k thể truy cập được
```java=
class OuterClass {
  int x = 10;

  private class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```
![](https://i.imgur.com/z53XxMc.png)
### 3. Static inner class
- Có thể truy xuất mà k cậu tạo đối tượng cho class ngoài
```java=
class OuterClass {
  int x = 10;

  static class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass.InnerClass myInner = new OuterClass.InnerClass();
    System.out.println(myInner.y);
  }
}

// Outputs 5
```
### 4. Truy xuất outer class
- x đã bị thay đổi khi truy xuất phương thức trước
![](https://i.imgur.com/6wUwmvv.png)


## 19. Abstraction
- Dùng để ẩn những dữ liệu (bảo mật)
- Abstract class: Không thể tạo với abstraction class mà chỉ có thể kế thừa từ nó
- Abstract method: chỉ được sử dụng trong Abstract class, không có body. Body được tạo bởi subclass kế thừa từ nó
```java=
// Abstract class
abstract class Animal {
  // Abstract method (does not have a body)
  public abstract void animalSound();
  // Regular method
  public void sleep() {
    System.out.println("Zzz");
  }
}

// Subclass (inherit from Animal)
class Pig extends Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig(); // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
```
![](https://i.imgur.com/hmOnH29.png)
## 20. Interface
- Một cách khác để làm được như Abstract class

### 1. "implements" keyword (thay vì "extends")
- Các methods trong **interface** mặc định đều là **abstract methods**
- ![](https://i.imgur.com/HyNueHG.png)
- Trong interface k thể tạo một **constructor**
```java=
// Interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void sleep(); // interface method (does not have a body)
}

// Pig "implements" the Animal interface
class Pig implements Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
  public void sleep() {
    // The body of sleep() is provided here
    System.out.println("Zzz");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
```
### 2. Đa kế thừa với Multiple interfaces
- Bởi vì trong java không hổ trợ kế thừa đa classes
```java=
interface FirstInterface {
  public void myMethod(); // interface method
}

interface SecondInterface {
  public void myOtherMethod(); // interface method
}

class DemoClass implements FirstInterface, SecondInterface {
  public void myMethod() {
    System.out.println("Some text..");
  }
  public void myOtherMethod() {
    System.out.println("Some other text...");
  }
}

class Main {
  public static void main(String[] args) {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```
![](https://i.imgur.com/fKdk3GI.png)

## 21. Enum
- Là 1 special class: chứa những cái **Hằng** (giá trị không thay đổi được)
- Sử dụng Enum khi biết có những giá trị không thay đổi: month days, days, colors, deck of cards, etc.
```java=
enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class Main {
  public static void main(String[] args) {
    Level myVar = Level.MEDIUM;

    switch(myVar) {
      case LOW:
        System.out.println("Low level");
        break;
      case MEDIUM:
         System.out.println("Medium level");
        break;
      case HIGH:
        System.out.println("High level");
        break;
    }
  }
}
```
![](https://i.imgur.com/dyTAhk5.png)

### Lặp qua ENUM
![](https://i.imgur.com/Yecd6m2.png)

## 22. Class SCANNER
- 1 class được tạo sẳn 
- "nextline()": để đọc 1 chuỗi từ bàn phím
```java=
import java.util.Scanner;  // Import the Scanner class

class Main {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);  // Create a Scanner object
    System.out.println("Enter username");

    String userName = myObj.nextLine();  // Read user input
    System.out.println("Username is: " + userName);  // Output user input
  }
}
```
![](https://i.imgur.com/3mq0dAI.png)
![](https://i.imgur.com/Dr9rWX6.png)

```java=
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);

    System.out.println("Enter name, age and salary:");

    // String input
    String name = myObj.nextLine();

    // Numerical input
    int age = myObj.nextInt();
    double salary = myObj.nextDouble();

    // Output input by user
    System.out.println("Name: " + name);
    System.out.println("Age: " + age);
    System.out.println("Salary: " + salary);
  }
}
```
![](https://i.imgur.com/37hYcAm.png)
## 23. Java Dates
![](https://i.imgur.com/IEm6Ddo.png)
![](https://i.imgur.com/VdHu0y2.png)

- Ví dụ: myDateObj hình thức hoá (format) theo kiểu myFormatObj 
```java=
import java.time.LocalDateTime;  // Import the LocalDateTime class
import java.time.format.DateTimeFormatter;  // Import the DateTimeFormatter class

public class Main {
  public static void main(String[] args) {  
    LocalDateTime myDateObj = LocalDateTime.now();  
    System.out.println("Before Formatting: " + myDateObj);  
    DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("E, MMM dd yyyy HH:mm:ss");  
    
    String formattedDate = myDateObj.format(myFormatObj);  
    System.out.println("After Formatting: " + formattedDate);  
  }  
}  
```
![](https://i.imgur.com/ddJFcaa.png)

```java=
import java.time.LocalDateTime; // Import the LocalDateTime class
import java.time.format.DateTimeFormatter; // Import the DateTimeFormatter class

public class Main {
  public static void main(String[] args) {
    LocalDateTime myDateObj = LocalDateTime.now();
    System.out.println("Before formatting: " + myDateObj);
    DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");

    String formattedDate = myDateObj.format(myFormatObj);
    System.out.println("After formatting: " + formattedDate);
  }
}
```
![](https://i.imgur.com/naCQ4KU.png)
![](https://i.imgur.com/FvhCkTU.png)

## 24. ArrayList class
```java=
import java.util.ArrayList;

public class Main { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
    //get size Array
    System.out.println(cars.size());
    //get item
    System.out.println(cars.get(0));
    
    // Set item
    cars.set(0, "Opel");
    System.out.println(cars);
    System.out.println("---------------");
    // loop through array
    for (int i = 0; i < cars.size(); i++) {
    System.out.println(cars.get(i));
    }
    System.out.println("---------------");
    // Cách 2 để loop
        for (String i : cars) {
      System.out.println(i);
    }
    System.out.println("---------------");
    // Remove item
    cars.remove(0);
    System.out.println(cars);
    
    // remove all item
    cars.clear();
    System.out.println(cars);
  } 
}

```
![](https://i.imgur.com/UiAklZk.png)

### Sắp xếp array 
```java=
import java.util.ArrayList;
import java.util.Collections;

public class Main { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    
    Collections.sort(cars);

    for (String i : cars) {
      System.out.println(i);
    }
  } 
}

```
![](https://i.imgur.com/L89AEzF.png)

## 25. Linked list
- Tương tự ArrayList, khác là lưu theo kiểu con trỏ nên chỉ có thể truy xuất tuần tự
![](https://i.imgur.com/WiXQc0k.png)

![](https://i.imgur.com/sPq7Z5q.png)

## 26. Hashmap (key - value)
```java=
import java.util.HashMap;

public class Main {
  public static void main(String[] args) {
    HashMap<String, String> capitalCities = new HashMap<String, String>();
    capitalCities.put("England", "London");
    capitalCities.put("Germany", "Berlin");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("USA", "Washington DC");
    System.out.println(capitalCities);
    // get size
        System.out.println(capitalCities.size());
     	System.out.println("-----------------");

    // loop qua keys
    for (String i : capitalCities.keySet()) {
      System.out.println(i);
    }
    System.out.println("-----------------");
    // loop qua valuse
        for (String i : capitalCities.values()) {
      System.out.println(i);
    }
    // loop qua key-value tương ứng
        for (String i : capitalCities.keySet()) {
      System.out.println("key: " + i + " value: " + capitalCities.get(i));
    }
        System.out.println("-----------------");

    // get Value of "England" key
    System.out.println(capitalCities.get("England"));
    
    // remove a pair key-value
    capitalCities.remove("England");
    System.out.println(capitalCities); 
    // remove all
        capitalCities.clear();
    System.out.println(capitalCities); 

    
  }
}

```
![](https://i.imgur.com/jhUnWm5.png)

## 27. Hashset (set: độc nhất, no index)
```java=
// Import the HashSet class
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {
    HashSet<String> cars = new HashSet<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("BMW");
    cars.add("Mazda");
    // get size
    System.out.println(cars.size());
    // loop qua
    for (String i : cars) {
  	System.out.println(i);
}
    System.out.println(cars);
    // CHeck sự tồn tại
    System.out.println(cars.contains("Mazda"));
    // Xoá item
        cars.remove("Volvo");
    System.out.println(cars);
    // clear
        cars.clear();
    System.out.println(cars);
    // 
  }
}

```
![](https://i.imgur.com/KVari2Q.png)
## 28. Iterator package
- Lặp qua Arraylist, Hashset có thứ tự
```java=
import java.util.ArrayList;
import java.util.Iterator;

public class Main {
  public static void main(String[] args) {
  
    // Make a collection
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
  
    // Get the iterator
    Iterator<String> it = cars.iterator();
  
    // Print the first item
    System.out.println(it.next());
    // con trỏ đã bị next đi 1 đơn vị
    // Lặp qua có thứ tự
    System.out.println("--------------");
        while(it.hasNext()) {
      System.out.println(it.next());
    }
  }
}
```
![](https://i.imgur.com/yUdZ5vP.png)

### Remove
```java=
import java.util.ArrayList;
import java.util.Iterator;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(12);
    numbers.add(8);
    numbers.add(2);
    numbers.add(23);
    Iterator<Integer> it = numbers.iterator();
    while(it.hasNext()) {
      Integer i = it.next();
      if(i < 10) {
        it.remove();
      }
    }
    System.out.println(numbers);
  }
}
```
![](https://i.imgur.com/EZTRHzc.png)

## 29. Wrapper Class
- Môt class hỗ trợ primitive data trong các Package (Arraylist..)
![](https://i.imgur.com/6Pk1oZU.png)
```java=
public class Main { 
  public static void main(String[] args) { 
    Integer myInt = 5; 
    Double myDouble = 5.99; 
    Character myChar = 'A'; 
    System.out.println(myInt.intValue());
    System.out.println(myDouble.doubleValue());
    System.out.println(myChar.charValue());
  }
}
```
![](https://i.imgur.com/fDAYQFt.png)

### ep kiểu thành chuỗi bằng toString()
![](https://i.imgur.com/dNhrDbm.png)
## 30. Biểu thức chính quy (Regular Expressions)
https://www.w3schools.com/java/java_regex.asp
- Check cái pattern có trong matcher k?
```java=
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
  public static void main(String[] args) {
    Pattern pattern = Pattern.compile("w3schools", Pattern.CASE_INSENSITIVE);
    Matcher matcher = pattern.matcher("Visit W3Schools!");
    boolean matchFound = matcher.find();
    if(matchFound) {
      System.out.println("Match found");
    } else {
      System.out.println("Match not found");
    }
  }
}
```
![](https://i.imgur.com/bW4JfMg.png)
![](https://i.imgur.com/XVCHFCr.png)

- ví dụ: Pattern.compile(["a""b"],Pattern.CASE_INSENSITIVE)
![](https://i.imgur.com/OYruURr.png)
![](https://i.imgur.com/xWOeq6v.png)
![](https://i.imgur.com/wb73DOF.png)

## 31. JAVA Threads
https://www.w3schools.com/java/java_threads.asp
- CÓ 2 cách để tạo môt luồng
![](https://i.imgur.com/oMDMyfe.png)
![](https://i.imgur.com/OMi8akJ.png)
![](https://i.imgur.com/wRl4MUg.png)
![](https://i.imgur.com/dO9FZu3.png)

### Vấn đề đồng thời trong Threads
- Khi thực hiện phương thức này, 1 thread khác đồng thời cũng đang chạy
```java=
public class Main extends Thread {
  public static int amount = 0;

  public static void main(String[] args) {
    Main thread = new Main();
    thread.start();
    System.out.println(amount);
    amount++;
    System.out.println(amount);
  }

  public void run() {
    amount++;
  }
}
```
![](https://i.imgur.com/P46SpBa.png)
### Để giải quyết vấn đề đó ta sử dụng phương thức: isAlive()
- Lệnh sau khí start() sẽ chạy
- xong hàm run() sẽ chạy
- ...
```java=
public class Main extends Thread {
  public static int amount = 0;

  public static void main(String[] args) {
    Main thread = new Main();
    thread.start();
    // Wait for the thread to finish
    while(thread.isAlive()) {
    System.out.println("Waiting...");
  }
  // Update amount and print its value
  System.out.println("Main: " + amount);
  amount++;
  System.out.println("Main: " + amount);
  }
  public void run() {
    amount++;
  }
}
```
![](https://i.imgur.com/x2doqVk.png)
## 32. Lambda
### 1. Cách sử dụng thông thường
- Là một biểu thức giống như phương thức nhưng không cần tên và được thực hiện ngay trong phần thân
- Hàm lamba trong code sau: "(n) -> { System.out.println(n);"
```java=
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(5);
    numbers.add(9);
    numbers.add(8);
    numbers.add(1);
    numbers.forEach( (n) -> { System.out.println(n); } );
  }
}
```
### 2. Sử dụng interface "Consumer" để lưu phương thức của lambda
```java=
import java.util.ArrayList;
import java.util.function.Consumer;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(5);
    numbers.add(9);
    numbers.add(8);
    numbers.add(1);
    Consumer<Integer> method = (n) -> { System.out.println(n); };
    numbers.forEach( method );
  }
}
```
![](https://i.imgur.com/DYebMaf.png)
- Một các dùng khác
```java=
interface StringFunction {
  String run(String str);
}

public class Main {
  public static void main(String[] args) {
    StringFunction exclaim = (s) -> s + "!";
    StringFunction ask = (s) -> s + "?";
    printFormatted("Hello", exclaim);
    printFormatted("Hello", ask);
  }
  public static void printFormatted(String str, StringFunction format) {
    String result = format.run(str);
    System.out.println(result);
  }
}
```
![](https://i.imgur.com/xJJ1yPr.png)
## 33. Java file
- creating, reading, updating, and deleting files.
- Tạo đối tượng cho class file, gắn path đến file cụ thể
```java=
import java.io.File;  // Import the File class

File myObj = new File("filename.txt"); // Specify the filename
```
![](https://i.imgur.com/Rhj0TwB.png)
### 1. Tạo file
- Tạo file bằng: createNewFile()
```java=
import java.io.File; 
import java.io.IOException;
  
public class CreateFileDir {  
  public static void main(String[] args) {  
    try {  
      File myObj = new File("C:\\Users\\MyName\\filename.txt");  
      if (myObj.createNewFile()) {  
        System.out.println("File created: " + myObj.getName());  
        System.out.println("Absolute path: " + myObj.getAbsolutePath());  
      } else {  
        System.out.println("File already exists.");  
      }  
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();  
    }  
  }  
} 
```
![](https://i.imgur.com/f3Xeunp.png)

### 2. Ghi file bằng class FileWriter
```java=
import java.io.FileWriter;   // Import the FileWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class WriteToFile {
  public static void main(String[] args) {
    try {
      FileWriter myWriter = new FileWriter("filename.txt");
      myWriter.write("Files in Java might be tricky, but it is fun enough!");
      myWriter.close();
      System.out.println("Successfully wrote to the file.");
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```
![](https://i.imgur.com/2G6us4J.png)

### 3. Read file
```java=

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class ReadFile {  
  public static void main(String[] args) {  
    try {
      File myObj = new File("filename.txt");
      Scanner myReader = new Scanner(myObj);  
      while (myReader.hasNextLine()) {
        String data = myReader.nextLine();
        System.out.println(data);
      }
      myReader.close();
    } catch (FileNotFoundException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    } 
  }  
} 
```
![](https://i.imgur.com/KsZqa3h.png)

### 4. Nhận thông tin về file
```java=

import java.io.File; 

public class GetFileInfo {  
  public static void main(String[] args) {  
    File myObj = new File("filename.txt");
    if (myObj.exists()) {
      System.out.println("File name: " + myObj.getName()); 
      System.out.println("Absolute path: " + myObj.getAbsolutePath()); 
      System.out.println("Writeable: " + myObj.canWrite()); 
      System.out.println("Readable: " + myObj.canRead()); 
      System.out.println("File size in bytes: " + myObj.length());
    } else {
      System.out.println("The file does not exist.");
    }
  }  
}
```
![](https://i.imgur.com/J2qQfQb.png)

### 5. Delete file
```java=
import java.io.File; 

public class DeleteFile {
  public static void main(String[] args) { 
    File myObj = new File("filename.txt"); 
    if (myObj.delete()) { 
      System.out.println("Deleted the file: " + myObj.getName());
    } else {
      System.out.println("Failed to delete the file.");
    } 
  } 
}
```
![](https://i.imgur.com/Ba4iXBz.png)
#### xoá folder
- Ở path không có tên file(k có đuôi .txt)
```java= 
import java.io.File; 

public class DeleteFolder {
  public static void main(String[] args) { 
    File myObj = new File("C:\\Users\\MyName\\Test"); 
    if (myObj.delete()) { 
      System.out.println("Deleted the folder: " + myObj.getName());
    } else {
      System.out.println("Failed to delete the folder.");
    } 
  } 
}
```
![](https://i.imgur.com/XfWUxlq.png)
