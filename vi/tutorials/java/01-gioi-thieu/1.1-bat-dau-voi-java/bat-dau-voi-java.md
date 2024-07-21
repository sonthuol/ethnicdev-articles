<div style="background-color: #e7e9eb; padding: 1px 10px; border-radius: 5px; margin-bottom: 20px">

### Nội dung bài viết

1. [Câu lệnh điều khiển | Kiểm soát mã luồng trong java](#cau-lenh-dieu-khien)
2. [Câu lệnh if](#cau-lenh-if)
3. [Câu lệnh switch](#cau-lenh-switch)
4. [Câu lệnh vòng lặp](#cau-lenh-vong-lap)
5. [Câu lệnh break](#cau-lenh-break)
6. [Câu lệnh continue](#cau-lenh-continue)

</div>

<div class="section" id="cau-lenh-dieu-khien"><div>

## Câu lệnh điều khiển | Kiểm soát mã luồng trong java

Trình biên dịch Java thực thị code từ trên xuống dưới. Các câu lệnh trong code được thực thi theo thứ tự chúng xuất hiện. Tuy nhiên, Java cung cấp các câu lệnh có thể được sử dụng để kiểm soát mã luồng trong Java. Những câu lệnh như vậy được gọi là câu lệnh luồng điều khiển. Đây là một trong những tính năng cơ bản của Java, giúp chương trình chạy trơn tru.

Java cung cấp ba loại câu lệnh luồng điều khiển

1. Tuyên bố ra quyết định (Decision making statements)

- if statements
- switch statements

2. Vòng lặp (Loop statements)

- do while loop
- while loop
- for loop
- for-each loop

3. Bước nhảy (Jump statements)

- break statements
- continue statements

## Tuyết bộ ra quyết định (Decisison makring statements)

Như tên cho thấy, các câu lệnh ra quyết định sẽ quyết định câu lệnh nào sẽ được thực thi và được thực thi khi nào.

<div class="section" id="cau-lenh-if"><div>

## Câu lệnh if (if statements)

Trong Java, câu lệnh if được sử dụng để phỏng đoán/quyết định một điều kiện. Việc điều khiển chương trình thì được chuyển hướng theo điều kiện cụ thể. Điều kiện của câu lệnh if cho giá trị boolean, đúng hoặc sai. Trong Java, có 4 kiểu câu lệnh if được giới thiệu bên dưới.

    1. Câu lệnh if đơn giản
    2. Câu lệnh if - else
    3. Câu lệnh if-else-if
    4. Câu lệnh if lồng nhau

Nào, chúng ta hãy tìm hiểu từng câu lệnh if.

### 1\) Câu lệnh if đơn giản

Đây là câu lệnh đơn giản nhất trong số tất cả các câu lệnh luồng điều khiển trong Java. Nó đánh giá một biểu thức boolean và cho phép chương trình nhập một khối code nếu biểu thức đó đúng.

Cú pháp của câu lệnh if thì được đưa ra bên dưới:

```java
if(condition){
    statement 1; // Thực thi khi điều kiện đúng
}
```

Hãy xem xét ví dụ sau trong đó chúng tôi đã sử dụng câu lệnh if trong mã Java.

`Student.java`

```java
public class Student {
    public static void main(String args[]){
        int x = 10;
        int y = 12;
        if(x + y > 20){
            System.out.println("x + y lớn hơn 20");
        }
    }
}
```

Kết quả:

```
x + y lớn hơn 20
```

### 2\) Câu lệnh if-else

Câu lệnh if-else là một sự mở rộng từ câu lệnh if, nó sử dụng một khối mã khác, cụ thể là khối mã else. Khối mã else được thực thi khi mà khối mã if có điều kiện được đánh giá là sai.

Cú pháp:

```java
if(condition) {
    statement 1; //được thi thi khi câu điều kiện đúng
} else{
    statement 2; //được thi thi khi câu điều kiện sai
}
```

Xem xét ví dụ bên dưới:

`Student.java`

```java
public class Student {
    public static void main(String args[]){
        int x = 10;
        int y = 12;
        if(x + y < 10) {
            System.out.println("x + y bé hơn 10");
        } else {
            System.out.println("x + y lớn hơn 10");
        }
    }
}
```

Kết quả:

```
x + y lớn hơn 10
```

### 3\) Câu lệnh if-else-if

Câu lệnh if-else-if chứa câu lệnh if theo sau đó là nhiều câu lệnh else-if. Nói cách khác, chúng ta có thể nói rằng nó là một chuỗi câu lệnh if-else tạo ra một cây điều điện. Khi chương trình thực thi từ trên xuống dưới gặp câu điều khi nào đúng, nó sẽ thực hiện khối code bên trong điều kiện đó. Ngoài ra cuối câu lệnh if-else-if chúng ta cũng có thể thêm một câu lệnh else cuối cùng.

Cú pháp của câu lệnh if-else-if:

```java
if(condition 1) {
    statement 1; // thực hiện khi câu điều kiện 1 is đúng
} else if(condition 2) {
    statement 2; // thực hiện khi câu điều kiện 2 is đúng
} else {
    statement 2; // thực hiện sau khi các câu điều kiện trên đều sai
}
```

Xem xét ví dụ bên dưới:

`Student.java`

```java
public class Student {
    public static void main(String[] args) {
        String city = "Delhi";
        if(city == "Meerut") {
            System.out.println("city is meerut");
        } else if (city == "Noida") {
            System.out.println("city is noida");
        } else if(city == "Agra") {
            System.out.println("city is agra");
        } else {
            System.out.println(city);
        }
    }
}
```

Kết quả:

```
Delhi
```

### 4\) Câu lệnh if lồng nhau

Câu lệnh if lồng nhau, là một câu lệnh có thể chứa một câu lệnh if hoặc một câu lệnh if-else bên trong một câu lệnh if hoặc câu lệnh if-else khác.

Cú pháp của câu lệnh if lồng nhau:

```java
if(condition 1) {
    statement 1; // thực hiện khi điều kiện 1 is true
    if(condition 2) {
        statement 2; // thực hiện khi điều kiện 2 is true
    }  else {
        statement 2; // thực hiện khi điều kiện 2 is false
    }
}
```

Xem xét ví dụ bên dưới:

`Student.java`

```java
public class Student {
    public static void main(String[] args) {
        String address = "Delhi, India";

        if(address.endsWith("India")) {
            if(address.contains("Meerut")) {
                System.out.println("Your city is Meerut");
            } else if(address.contains("Noida")) {
                System.out.println("Your city is Noida");
            } else {
                System.out.println(address.split(",")[0]);
            }
        } else {
            System.out.println("You are not living in India");
        }
    }
}
```

Kết quả:

```
Delhi
```

<div class="section" id="cau-lenh-switch"><div>

## Câu lệnh switch

Trong Java, câu lệnh switch thì tương tự như câu lệnh if-else-if. Câu lệnh switch chưa nhiều khối code hay còn gọi là các trường hợp (case) và trong mỗi trường hợp thì được thực thi dựa trên biến mà được chuyển đổi. Câu lệnh switch thì dễ dàng sử dụng thay vì sử dụng câu lệnh if-else-if. Nó cũng tăng cường khả năng đọc của chương trình.

Những điểm cần lưu ý về câu lệnh switch:

- Các giá trị trong mỗi case có thể là int, short, byte, char hoặc enumeration. Kiểu String cũng được hỗ trợ từ java 7.
- Câu lệnh default ở cuối mỗi case được thực thi khi bất kỳ trường hợp nào không khớp với giá trị của biểu thức. Nó là một option.

- Câu lệnh break kết thúc khối switch khi mà điều kiện được thoả mãn. Nó là tuỳ chọn, nếu không được sử dụng, trường hợp tiếp theo sẽ được thực thi

- Trong khi sử dụng câu lệnh switch, chúng ta phải lưu ý rằng biểu thức trong case sẽ có cùng loại với biến. Tuy nhiên nó sẽ là một giá trị không đổi.

Cú pháp của câu lệnh switch:

```java
switch (expression){
    case value1:
     statement1;
     break;
    .
    .
    .
    case valueN:
     statementN;
     break;
    default:
     default statement;
}
```

Xem xét ví dụ bên dưới để hiểu rõ về luồng của câu lệnh switch

`Student.java`

```java
public class Student implements Cloneable {
    public static void main(String[] args) {
        int num = 2;
        switch (num) {
            case 0:
                System.out.println("number is 0");
                break;
            case 1:
                System.out.println("number is 1");
                break;
            default:
                System.out.println(num);
        }
    }
}
```

Kết quả:

```
2
```

Trong khi sử dụng câu lệnh switch, chúng ta phải lưu ý rằng biểu thức case sẽ có cùng loại với biến. Tuy nhiên, nó cũng sẽ là một giá trị không đổi. Switch chỉ cho phép sử dụng các biến kiểu int, string và Enum.

<div class="section" id="cau-lenh-vong-lap"><div>

## Câu lệnh vòng lặp

Trong lập trình, đôi khi chúng ta cần thực thi khối mã nhiều lần trong khi số điều kiện được đánh giá là đúng. Tuy nhiên, các câu lệnh vòng lặp được sử dụng để thực hiện tập lệnh theo thứ tự lặp lại. Việc thực hiện tập lệnh phụ thuộc vào một điều kiện cụ thể.

Trong Java, chúng ta có ba loại vòng lặp thực thi tương tự nhau. Tuy nhiên, có sự khác biệt về cú pháp và thời gian kiểm tra điều kiện.

    1. Vòng lặp for
    2. Vòng lặp while
    3. Vòng lặp do-while

Chúng ta hãy hiểu từng câu lệnh vòng lặp.

### 1\) Vòng lặp for

Trong Java, vòng lặp for tương tự như C và C++. Nó cho phép chúng ta khởi tạo biến vòng lặp, kiểm tra điều kiện và tăng/giảm trong một dòng mã. Chúng ta chỉ sử dụng vòng lặp for khi biết chính xác số lần chúng ta muốn thực thi khối mã.

```java
for(initialization, condition, increment/decrement) {
//block of statements
}
```

Biểu đồ luồng cho vòng lặp for được đưa ra dưới đây.

![flow chart for the for-loop](https://static.javatpoint.com/core/images/control-flow-in-java.png)

Hãy xem ví dụ sau để hiểu cách hoạt động chính xác của vòng lặp for trong java.

`Calculattion.java`

```java
public class Calculattion {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int sum = 0;
        for(int j = 1; j<=10; j++) {
            sum = sum + j;
        }
        System.out.println("Tổng của 10 số tự nhiên đầu tiên là " + sum);
    }
}
```

Kết quả:

```
Tổng của 10 số tự nhiên đầu tiên là 55
```

### 2\) Vòng lặp for-each

Java cung cấp vòng lặp for nâng cao để duyệt qua các cấu trúc dữ liệu như mảng hoặc tập hợp. Trong vòng lặp for-each, chúng ta không cần cập nhật biến vòng lặp. Cú pháp sử dụng vòng lặp for-each trong java được đưa ra dưới đây.

```java
for(data_type var : array_name/collection_name){
//statements
}
```

Hãy xem ví dụ sau để hiểu cách hoạt động chính xác của vòng lặp for-each trong java.

`Calculattion.java`

```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        String[] names = {"Java","C","C++","Python","JavaScript"};
        System.out.println("Printing the content of the array names:\n");
        for(String name:names) {
            System.out.println(name);
        }
    }
}
```

Kết quả:

```
Printing the content of the array names:

Java
C
C++
Python
JavaScript
```

### 3\) Vòng lặp while

Vòng lặp while cũng được sử dụng để lặp lại số lượng câu lệnh nhiều lần. Tuy nhiên, nếu chúng ta không biết trước số lần lặp thì nên sử dụng vòng lặp while. Không giống như vòng lặp for, việc khởi tạo và tăng/giảm không diễn ra bên trong câu lệnh vòng lặp trong vòng lặp while.

Nó còn được gọi là vòng lặp kiểm soát đầu vào vì điều kiện được kiểm tra ở đầu vòng lặp. Nếu điều kiện đúng thì phần thân vòng lặp sẽ được thực thi; nếu không thì các câu lệnh sau vòng lặp sẽ được thực thi.

Cú pháp của vòng lặp while được đưa ra dưới đây.

```java
while(condition){
//looping statements
}

```

Biểu đồ luồng cho vòng lặp while được đưa ra trong hình ảnh sau đây.

![flow chart for the while loop](https://static.javatpoint.com/core/images/control-flow-in-java2.png)

Hãy xem xét ví dụ sau.

`Calculattion.java`

```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int i = 0;
        System.out.println("Printing the list of first 10 even numbers \n");
        while(i<=10) {
            System.out.println(i);
            i = i + 2;
        }
    }
}
```

Kết quả:

```
Printing the list of first 10 even numbers

0
2
4
6
8
10
```

### 4\) Vòng lặp do-while

Vòng lặp do-while kiểm tra điều kiện ở cuối vòng lặp sau khi thực hiện các câu lệnh vòng lặp. Khi không biết số lần lặp và chúng ta phải thực hiện vòng lặp ít nhất một lần, chúng ta có thể sử dụng vòng lặp do-while.

Nó còn được gọi là vòng lặp kiểm soát lối ra vì điều kiện không được kiểm tra trước. Cú pháp của vòng lặp do-while được đưa ra dưới đây.

```java
do
{
//statements
} while (condition);
```

Biểu đồ luồng của vòng lặp do-while được đưa ra trong hình ảnh sau.

![flow chart of the do-while loop](https://static.javatpoint.com/core/images/control-flow-in-java3.png)

Hãy xem ví dụ sau để hiểu chức năng của vòng lặp do-while trong Java.

`Calculattion.java`

```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int i = 0;
        System.out.println("Printing the list of first 10 even numbers \n");
        do {
            System.out.println(i);
            i = i + 2;
        }while(i<=10);
    }
}
```

Kết quả:

```
Printing the list of first 10 even numbers

0
2
4
6
8
10
```

## Jump Statements

Câu lệnh nhảy được sử dụng để chuyển quyền điều khiển chương trình sang câu lệnh cụ thể. Nói cách khác, câu lệnh nhảy chuyển quyền điều khiển thực thi sang phần khác của chương trình.

Có hai loại câu lệnh nhảy trong Java, tức là `break` và `continue`.

<div class="section" id="cau-lenh-break"><div>

### Câu lệnh break

Như tên cho thấy, câu lệnh break được sử dụng để ngắt luồng hiện tại của chương trình và chuyển điều khiển sang câu lệnh tiếp theo bên ngoài câu lệnh vòng lặp hoặc câu lệnh switch. Tuy nhiên, nó chỉ phá vỡ vòng lặp bên trong trong trường hợp vòng lặp lồng nhau.

âu lệnh break không thể được sử dụng độc lập trong chương trình Java, tức là nó chỉ có thể được viết bên trong câu lệnh vòng lặp hoặc câu lệnh switch.

Ví dụ về câu lệnh break với vòng lặp for

Hãy xem xét ví dụ sau trong đó chúng ta đã sử dụng câu lệnh break với vòng lặp for.

BreakExample.java

```java
public class BreakExample {

    public static void main(String[] args) {
        // TODO Auto-generated method stub
        for(int i = 0; i<= 10; i++) {
            System.out.println(i);
            if(i==6) {
            break;
            }
        }
    }
}
```

Kết quả:

```
0
1
2
3
4
5
6
```

ví dụ về câu lệnh break với vòng lặp được gắn nhãn for

Calculation.java

```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        a:
        for(int i = 0; i<= 10; i++) {
            b:
            for(int j = 0; j<=15;j++) {
                c:
                for (int k = 0; k<=20; k++) {
                    System.out.println(k);
                    if(k==5) {
                        break a;
                    }
                }
            }
        }
    }
}
```

Kết quả:

```
0
1
2
3
4
5
```

<div class="section" id="cau-lenh-continue"><div>

### Câu lệnh continue

Không giống như câu lệnh break, câu lệnh continue không phá vỡ vòng lặp, ngược lại, nó bỏ qua phần cụ thể của vòng lặp và chuyển sang lần lặp tiếp theo của vòng lặp ngay lập tức.

Hãy xem ví dụ sau để hiểu chức năng của câu lệnh continue trong Java.

```java
public class ContinueExample {
public static void main(String[] args) {
        // TODO Auto-generated method stub
        for(int i = 0; i<= 2; i++) {
            for (int j = i; j<=5; j++) {
                if(j == 4) {
                    continue;
                }
                System.out.println(j);
            }
        }
    }

}
```

Kết quả:

```
0
1
2
3
5
1
2
3
5
2
3
5
```
