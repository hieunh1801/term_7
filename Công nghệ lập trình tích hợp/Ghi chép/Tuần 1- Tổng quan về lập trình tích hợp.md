# Tổng quan về công nghệ lập trình tích hợp

- Phầm mềm là gì? 
  - Là một tập các chương trình, gồm data, document [tài liệu đặc tả yêu cầu, phân tích và thiết kế ra hệ thống, phục vụ cho việc phát triển phần mềm].

- Tích hợp là gì?
  - Liên kết các phần mềm lại với nhau. 
  - Tại sao lại phải liên kết? 
    - VD1: Nhiều phần mềm cùng dùng chung dữ liệu. Các phần mềm là rời rạc vì qua năm này qua năm khác tạo ra các phần mềm rời rạc khác nhau. Khác về nền tảng công nghệ JAVA, C#, PYTHON ...
    => Giải pháp: tích hợp các phần mềm lại
    - VD2: 2 ngân hàng sát nhập lại với nhau: => dữ liệu cần được tích hợp.

- __*Tích hợp cái gì?*__
  - Giao diện: chỉ dùng chung giao diện
  - Nghiệp vụ: chỉ tích hợp tầng nghiệp vụ - dùng service bên thứ 3. VD: bên bán hàng sử dụng API do nhà vận chuyển cung cấp
  - Dữ liệu: tích hợp tầng dữ liệu. VD: hệ thống quản lý điểm, quản lý học sinh => tích hợp db lại

- Các mô hình tích hợp:
  - Web service

- Nội dung:
  - Viết webservice
  - WCF
  - Web API - là một dạng dịch vụ web sử dụng HTTP

- Thi:
  - 1 câu lý thuyết
  - 1 câu bài tập
  - 1 câu trên bài tập lớn

- Định dạng chuyển đổi dữ liệu
  - JSON
  - XML

## Enterprise Application Integration [EAI]

- Các ứng dụng rời rạc - về mặt công nghệ, nền tảng: chia sẻ dữ liệu và chia sẻ các nghiệp vụ doanh nghiệp
- Các kiểu tích hợp: [A - Application, B - business, C - customer]
  - A - A (app to app), 
  - B - B (business to business: tích hợp hệ thống các phần mềm của 2 doanh nghiệp với nhau VD: 2 ngân hàng sát nhập với nhau), 
  - A - B (Application to Business: sử dụng dịch vụ của google),
  - B - C (Business to customer - sử dụng dịch vụ trực tiếp. VD: ta tra thời tiết)

- Cách tích hợp 
  - Poin to Poin: Mỗi phần mềm sẽ xây dựng liên kết với nháu theo điểm. 1-1
    - Ưu điểm: Nhanh và ổn định, vì ta hiểu hết sâu và ổn định thì ta mới tích hợp được
    - Nhược: cứ thêm 1 phần mềm là ta phải kết nối tới tất cả các poin còn lại.Mà khi viết nhiều, do đó không còn đúng nữa
  - Hub-to-P: tất cả cùng kết nối vào 1 hub. khi 
    - Ưu điểm: Giảm số lượng kết nối xuống.
    - Nhược: hub quá tải

  - Kiến trúc phân tán: distribute intergration:
    - Thông qua mạng lưới bao gồm cả projet
    - 
  - Kiến trúc hướng dịch vụ. Đóng gói phần mềm thành các dịch vụ, khi dùng thì dùng trên đó

- Dịch vụ: thực hiện một nghiệp vụ nào đó. Ta chỉ cần cung cấp đầu vào và nhận đầu ra tương ứng. Ta không quan tâm tới bên trong tính toán thế nào, chỉ cần đầu ra tương ứng

- Điểm yếu: 
  + Khi mà kết nối trực tiếp 2 phần mềm thì ta hiểu rất sâu về nó. Khi mà ta sử dụng dịch vụ => bên sử dụng và bên cung cấp dịch vụ đều phải theo một chuẩn chung để giao tiếp. service contract
  + Khi mà kết nối trực tiếp: tốc độ nhanh. Khi mà sử dụng service - ta tốn time hơn
  + Vấn đề bảo mật - qua nhiều kết nối thì ta ko biết dữ liệu của ta có an toàn không

## Enterprise Service Bus

