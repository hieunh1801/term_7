# Các bước xây dựng một ứng dụng Servlet
[See detail at]('https://o7planning.org/vi/10169/huong-dan-lap-trinh-java-servlet#a721558')
## Cài đặt và cấu hình
- JDK
- Java EE
- Eclipse
- Tomcat - Server để chạy ứng dụng Servlet

## Các bước
- Step 1: Cấu hình Tomcat Server để chạy ứng dụng web
- Step 2: Cấu hình Servlet đầu tiên. Chú ý các vấn đề sau:
    - 2 method doGet() và doPost()
    - Vòng đời của một Servlet
    - Multiple Thread và cách handle Multiple Thread khi xử lý Instance variable (slide 1_2 của thầy)
- Step 3: Cấu hình JSP - Java Server Page và mô hình MVC

## Các vấn đề cần chú ý
- Xử lý kí tự đặc biệt khi nhập TextArea
    - SevletUntilities
- SQL Injection
- Xử lý dữ liệu thiếu