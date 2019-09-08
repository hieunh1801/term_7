# Tuần 4: JavaWeb

## Yêu cầu cài đặt
- NetBeans
- Webserver - GlassFish hoặc Tomcat
- JavaEE - Java Enterprise Edition
- JDK

## Kiến thức

- Webserver có Servlet container - để chạy các servlet
- sevlet kế thừa HTTPServlet và có 2 method cơ bản cần override
    - doGet - xử lý method Get
    - doPost - xử lý method Post
    - init: khởi tạo: nạp một lần duy nhất trong bộ nhớ, không nạp lại 
        - khi mà nhiều thằng client cùng chạy servlet - thì thằng này chạy duy nhất lần đầu tiên. 
```java
import java.io.*; import javax.servlet.*; import javax.servlet.http.*;
public class ServletTemplate extends HttpServlet {
    public void init(ServletConfig config) throws Servlet Exception {
        // Nạp các tham số khởi tạo
    }
    public void doGet (HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    // Use "request" to read incoming
    // Use "response" to write ….
    PrintWriter out = response.getWriter();
    // Use "out" to send content to browser.
    }

    public void doPost() {
        // Do something
    }
    public void service (HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        // Được gọi khi có request từ client thông qua threads
    }
}
```

- Vòng đời của Servlet
## Đa luồng
- Khi client đầu tiên gọi tới Servlet => Servelet -tạo ra-> 1 Instance duy nhất. Mỗi khi một request được gửi đến, một thread được tạo ra để xử lý request đó. Khi mà nhiều request gửi tới cùng một lúc -> dẫn tới việc cùng xử lý trên một instance của servlet trên. Do đó nếu có biến instance variable(là attribute của class mà không có static) gây ra lỗi.
- Handle:
    - Kế thừa interface SingleThreadMode
    - Sử dụng method synchronized() - để thực thi tuần tự hóa các 
## Other
- Truyền dữ liệu từ client tới server 
- Servelet Cloboration - Cộng tác giữa các Servelet
    - Interface - Request Dispatcher: điều hướng request
    - Redirect()
    - Nó chuyển yêu cầu tới servlet khác 
    - Sự khác nhau giữa forward() và sendRedirect()
        - Forward chạy phía serverside. gửi request tới một servlet khác
            - VD: Sevlet1 nhận requset - xử lý trả res1. rồi forward cái res tới Servlet2. Sevlet2 handle res1 và trả res2. Khi đó thì server trả res2 chứ không nhận res1