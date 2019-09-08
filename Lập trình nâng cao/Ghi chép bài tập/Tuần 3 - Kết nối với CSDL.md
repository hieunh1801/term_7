# Tuần 3 - SET, Hash, MAP - JDBC

## MAP
- Khái niệm:
    - Map không phải là một Collection. Nó đại diện sự tương ứng giữa tập khóa và tập giá trị
    - Chỉ một giá trị tương ứng với khóa; nhiều khóa có thể map tới cùng một giá trị
- java.util:
    - Map
        - TreeMap: khóa phải so sánh được, cài đặt khóa như trên Binary Tree - cây cân bằng
        - HashMap: định nghĩa 2 method hashCode() và equals()
    - SortedMap
    
## JDBC

- Tổng quát khi làm việc - quy trình 4 bước xử lý
    - Mở một kết nối tới CSDL (Open connection)
    - Thực thi câu lệnh SQL (Execute SQL)
    - Xử lý dữ liệu (Process result)
    - Đóng kết nối (Close connection)
- Cài đặt
    - Tải JDBC - Giúp làm việc với DB
    - Tải SQLDriver - kết nối tới SQL
- Trình điều khiển JDBC
    - Kết nối tới các DBMS như SLQ, MySQL, Oracle, MS Access, FoxPro, ...
    - Để sử dụng DBMS (Database Management System) ta cần các JDBC Driver tương ứng
- JDBC Connection
```java
try {
    Class.forName("tên chương trình điều khiển csdl"); // tên chương trình điều khiển csdl
    Class.forName("com.mysql.jdbc.Driver"); // Nạp driver for mysql
    Class.forName("com.jdbc.driver.OracleDriver"); // Nạp driver for oracle
    Class.forName("com.sybase.jdbc.SybDriver"); // Nạp driver for sybase
} catch (Exception e) {
    System.out.print("Error ", e);
} finally {
    System.out.print("Finish ");
}
```
- Chú ý khi nạp driver thì phải thử luôn
- Các lỗi cần check khi nạp SQL Server
    - 1. SQL Server chạy chưa
    - 2. Database có chưa
    - 3. Tên tài khoản, mật khẩu đúng không
    - 4. Cổng đúng chưa
- Khi ta làm việc với db
    - Có thằng đang insert, có thằng update
        - Ta đọc tới bản ghi 10, thằng kia nó update thằng 1000 sang mới, thì ta load tới bản ghi 1000 thì bản ghi 1000 là bản ghi cũ. <phi ngữ cảnh - Insensitive>
        - Khi ta muốn làm việc với kiểu dữ liệu mới nhất - Sensitive
