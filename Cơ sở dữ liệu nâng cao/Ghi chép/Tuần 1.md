# Buổi 1

## Tổng quan môn học

- Thiết kế CSDL
- Khai thác CSDL
- Thi vấn đáp
- Bài kiểm tra giữa kì
- Điểm danh 8h50

## Làm sao để thiết kế một CSDL ???

## Thiết kế CSDL:
- Quá trình phân tích
  - Thu thập
- Quá trình thiết kế
### CSDL phải đáp ứng gì ?

- Đảm bảo: hệ thống chạy được tất cả chúc năng.
- Cùng 1 đối tượng nhưng có thể có nhiều cách lưu trữ khác nhau => tùy vào mục đích của hệ thống mà ta lưu trữ sao cho phù hợp.
- Hệ thống:
  + Tồn tại dưới dạng (physic hoặc logic - trong đầu ai đó).
  + Ta phải đi khảo sát thực thể.
  + Hệ thống phát triển theo time, làm sao để đáp ứng được ?

### Các bước làm ?

- Step 1: Khảo sát, tập hợp các yêu cầu (mô tả hệ thống)

- Step 2: 
  + Thiết kế CSDL
  + Thiết kế các chức năng

- Step 3: ---> 

### Quy trình thiết kế CSDL

- Đặc tả yêu cầu
- Thiết kế csdl quan hệ (quan hệ giữa các thực thể)
- Chọn hệ quản trị CSDL: MongoDB, PostgreSQL, SQL Server
- Thiết kế CSDL logic:
  + Các dạng chuẩn 1NF, 2NF, 3NF, BCNF
  + Nếu CSDL không tốt => theo các dạng chuẩn mà ta chuyển dổi dần sang tốt hơn.
- Thiết kế logic: là cài đặt và đưa vào vận hành

### Mục đích của các yêu cầu

### Người thiết kế CSDL

- Nghiên cứu thực trạng.
- Ghi nhận mong muốn người sử dụng: VD: khách hàng yêu cầu có thể nhập danh sách bằng file exel
- Mẫu biểu: in ra được mẫu biểu theo yêu cầu. => __*Những mẫu biểu sẽ thể hiện dữ liệu mà ta cần lưu trữ*__

### Đặc tả chức năng

### Một số kĩ thuật phân tích 

- Dễ dàng nhất: Bằng cách nào đó lấy được quy trình xử lý, mẫu biểu, quy trình vận hành trong thế giới thực.
- Kĩ thuật phân tích tài liệu: từ tài liệu -> tạo ra CSDL
- Phiếu khảo sát: tạo các phiếu khảo sát cho một hệ thống lớn, nhiều người tham gia

- Kết quả: tạo ra được Document mô tả được
  - Quy trình xử lý, quy trình vận hành.
  - Các mãu biểu.
  - Những thao tác mà khách hàng yêu cầu.
  - Làm đến mức độ nào.
  - Làm đến yêu cầu nào.

### Thiết kế CSDL quan niệm (quan hệ)

- CSDL quan hệ mô tả cái gì ?
  - Mô tả các đối tượng mà ta hình dung trong hệ thống
  - VD: Hệ thống quản lý bán hàng online
    - Đối tượng
      + mặt hàng: sách
      + mua hàng: khách hàng
      + hóa đơn: mẫu biểu hóa đơn
    - Mối quan hệ giữa các thực thể
      + mặt hàng và mua hàng có quan hệ gì? mua
      + tác giả và sách ??? => sở hữu

- Làm sao để biết được cần bao nhiêu thực thể ?
  - Xác định thực thể ?
    - Từ mẫu biểu: mẫu biểu là một cái mô tả các thực thể.
    - Từ các đối tượng theo yêu cầu và thu thập được.
  - Một thực thể thì cần những thuộc tính gì ?
    - Các thuộc tính thu lượm được từ các mẫu biểu thu thập được => __yêu cầu thu thập ít nhất là đầy đủ thông tin__
    => Vì: mỗi hệ thống khác nhau yêu cầu thông tin theo đối tượng khác nhau. 
      + VD: quản lý học sinh: lưu thông tin học sinh. quản lý hộ khẩu: lưu mối quan hệ của các đối tượng khác nữa.
    - Chú ý: thuộc tính không cần thiết thì có thể bỏ qua.__Cái mà ta cần__
      + VD: hệ thống quản lý điểm: 
        - Nếu trong tất cả mẫu biểu mà không có quê quán => bỏ.

- Các Step xác định sau khi khảo sát => __tạo ra sơ đồ thực thể__
  - Coi 1 mẫu biểu là 1 thực thể
  - Cái chỗ nào mà ta __thay đổi được__ => cho nó là thuộc tính. __Chú ý: thay đổi: theo thời gian, phạm vi của hệ thống__
  - Khi có nhiều mẫu biểu bắt đầu tách thành các thực thể nhỏ hơn, từ đó OK
  - __Chú ý :__ Có những thuộc tính mà ta phân vân, giữa có phải hay không phải là thuộc tính. VD: Khi khảo sát, ta thấy một mẫu biểu có tên trường Đại học => Ta phải xét tới __mức độ yêu cầu, phạm vi của hệ thống__ VD1: quản lý trường HVKTQS: tên trường không đổi => không cần lưu. VD2: Hệ thống quản lý cho nhiều trường ĐH => tên trường thay đổi, nên tên trường cần lưu lại làm một thuộc tính.

- CSDL quan hệ mô tả những cái trên như thế nào ?
  - Đối tượng
  - Quan hệ giữa các đối tượng

### Lựa chọn hệ quản trị CSDL: show off - thể hiện 

- Các vấn đề khi cân nhắc một hệ quản trị CSDL
  - Tính tích hợp với công nghệ của hệ thống: VD: ASP => SQL server
  - Chi phí: 
  - Công nghệ lưu trữ
  - Mức độ lưu trữ: cỡ vừa và nhỏ - sql . cỡ lớn - oracal
  ..............

### Thiết kế CSDL logic:

- Từ sơ đồ CSDL quan hệ => chuẩn hóa: 1NF, 2NF, 3NF, BCNF, 4NF, 5NF ... Tối thiểu quá trình phân tích phải đạt được lược đồ quan hệ đạt mức BCNF.
- Thiết kế logic: cần kinh nghiệm, kĩ năng, quyết đoán. còn gọi là quy trình phi chuẩn hóa: kết quả lược đồ quan hệ có thể không đạt chuẩn gì cả. Vì quá trình này phục vụ cho việc khai thác CSDL một cách hiệu quả hơn.
  VD: Trong một bản ghi: hóa đơn 01, rau cải, giá: 16.000đ, số lượng 12kg, thành tiền: ...
    => Vi phạm tiêu chuẩn ...
> __Tuy nhiên :__ khi in ra hóa đơn thì ta select trực tiếp luôn, không phải tính toán ... các thông tin dư thừa làm vi phạm chuẩn tuy nhiên giải quyết được bài toán phức tạp. VD: đơn giá không cần lưu vì ta có id sản phẩm, thời điểm ... Tuy nhiên để mà lấy được đơn giá ta phải join nhiều bảng, gây ra truy vấn chậm. __Do đó:__ xét về mặt lý thuyết phân tích: ta loại bỏ dư thừa dữ liệu. __Thực tế:__ ta làm ra một CSDL để phục vụ Application, ta chấp nhận dư thừa dữ liệu để truy vấn hiệu quả hơn.

- __Kết quả:__ Ta có một lược đồ CSDL đáp ứng được các tác vụ của Application, chấp nhận sự dư thừa CSDL

### Thiết kế vật lý:

- Xác định cụ thể các thành tố sau:
  - Đặt tên bảng
  = Tên trường
  - Kiểu trường
  - Khóa chính, khóa ngoại
  - Nullable ...

- __Kết quả:__ Tạo ra CSDL có thể cài đặt mà không cần nghĩ ngợi gì nữa

### Khi xác định thực thể

- Thuộc tính
  - Thuộc tính đơn: mô tả thông tin
  - Thuộc tính phức hợp: có thể chia theo nhiều phần nhỏ. Ví dụ: quê quán - nếu ta chỉ nhập vào để in ra bằng cấp, không cần thuộc tính phức hợp. VD2: quản lý, khai thác thông tin trên quê quán - phải quản lý: __Phức hợp nghĩa là một thông tin có nhiều cái nhỏ hơn, chi tiết hơn__
  - __Chú ý:__ thuộc tính phức hợp hay không phụ thuộc vào hệ thống mà ta thiết kế
  
  - Thuộc tính đơn trị: 
  - Thuộc tính đa trị: trong hệ thống quản lý điểm thì tên là đơn trị. trong quản lý sơ yếu lý lịch , tên: đa trị - có 2 tên: tên ở nhà và tên ở ngoài. chứng minh thư - có nhiều nên cũng cần lưu

> - Vậy trong một hệ thống, trong __giới hạn bài toán__ của hệ thống ta cần phải xác định được đâu là thuộc tính đa trị, đơn trị.
> - Ta cần phải xác định trong khoảng thời gian dài mà hệ thống phục vụ. Ta nhìn hệ thống theo lịch sử thực thi chứ không chỉ nhìn trạng thái hiện tại của hệ thống. __Xác định biên của hệ thống .__

  - Thuộc tính suy diễn: tuổi => lưu ngày sinh chứ không lưu tuổi, ta lưu những cái cố đinh, không bị thay đổi theo time, từ các thuộc tính cũ mà ta có thể sinh ra được. tổng tiền: tổng tiền có tĩnh cố định, không bị change theo time.

  - Thuộc tính liên kết: 1-1, 1-n, n-1 ; n-n. chú ý mối liên kết n-n có thể sinh ra nhiều bảng. Ta đặt câu hỏi: một đối tượng bên này có bao nhiêu đối tượng bên kia.
    - __Chú ý:__ vd khi nói về lớp quản lý và sinh viên: tại thời điểm mà ta nói - là 1 - n. Tuy nhiên nếu một học sinh mà bị lưu ban, chuyển lớp, chuyển ngành ...  thì nó là quan hệ n-n ???. Đây là trường hợp đặc biệt do đó ta cần liên hệ để biết rõ được cách hệ thống hoạt động

