# Chương 1: Generic, Collections, JDBC

## 1. Generic Programming - Lập trình tổng quát

- Tại sao lại có lập trình tổng quát?
  - Trước khi có generic programming thì 
    - trong C có con trỏ void [là con trỏ không định kiểu nghĩa là nó có thể trỏ tới kiểu dữ liệu bất kì]. Thường dùng để khai báo tham số của chương trình con. Nên khi mà muốn in ra giá trị của con trỏ void thì phải ép sang kiểu cụ thể nào đấy.
    - C++ dùng template
    => Hạn chế: cứ mỗi khi dùng lại phải ép kiểu => làm chậm chương trình
  __=> Mục đích: lưu cái gì cũng được. Một class làm được nhiều việc__

  - Để giải quyết các hạn chế trên => đưa ra lập trình tổng quát:

- Giải quyết việc gì?
  - VD: Ta xây dựng lớp tập hợp (để thực hiện các phép toán trên một tập hợp: thêm, sửa, xóa)
    - Khi tập hợp có kiểu là kiểu nguyên thì ta xây một class intSet
    - Khi tập hợp kiểu float => floatSet
    - Khi tập hợp kiểu string => stringSet
    __.... => Sinh ra rất nhiều__
    => Từ đó ta xây dựng một lớp kiểu object => ta quản lý được mọi tập hợp. Tuy nhiên mỗi khi dùng ta lại phải ép kiểu.
    => Sinh tiếp ra khái niệm lập trình tổng quát. (cấu trúc dữ liệu tham số)


```java
public class Genericset<T> {
  private ArrayList<T> al;
}
```

## Collections - Các cấu trúc dữ liệu tiện ích cho việc lập trình
  - ArrayList, LinkedList
  - TreeSet, HashSet
  - TreeMap, HashMap

- __Chú ý:__
  - List là danh sách có thứ tự, phần tử có thể lặp lại. 
  - Set là tập hợp, không có thứ tự, phần tử chỉ tồn tại duy nhất 1.
  - Map (ánh xạ): map lưu trữ cặp đối tượng, key - value.

## Hướng dẫn
```java
public class IntSet {
  // ...
  public IntSet() {
    this(DefaultCapacity); // gọi tới constructor 1 tham số.
  }
}
/*
  - Trong cây kế thừa thì constructor gọi theo từ constructor của lớp cha -> constructor của lớp con.
  - Khi đó ta chỉ định bằng từ khóa this.super() để biết được là ta chỉ định tới constructor nào của lớp cha.
  - Khi ta không chủ động gọi từ khóa super() trong lớp con thì nó tự động gọi tới constructor mặc định của lớp cha (không tham số)
*/
```

## Bài tập về nhà
- Học lại lập trình hướng đối tượng.
- Array Linked- Linked list.
- Class lồng trong class.
  - Class có gì?
    + atribute, constructor, class, method
- Class, Interface, Abstract.
- Các từ khóa định phạm vi (public, protected, private)
- Các cấu trúc dữ liệu.
  - Hash, stack, queue
- Collections: include interator.
- Interator: là một đối tượng hỗ trợ duyệt các collection. bằng cách nào đó nó duyệt qua hết các phần tử, không bị bỏ xót hoặc lặp lại. (giống vòng lặp for)

- Xây dựng Stack tổng quát.
- Xây dựng lớp tập hợp tổng quát.

- __Bài tập thầy giao__
- Array list, link list, stack, queue, priority queue

- BT 1. Array list
  - Sử dụng Array List tổng quát
  - Array<String> hoặc interger, double
  - Thêm vào 5 đối tượng
  - Sắp xếp
  - Tạo một đối tượng mới và tìm đối tượng đó trong ArrayList
- BT 2. Array List
  - Xây dựng một lớp mới Student
  - Thêm vào array list 5 đối tượng
  - Sắp xếp
  - Tạo một đối tượng mói và tìm kiếm đối tượng đó
