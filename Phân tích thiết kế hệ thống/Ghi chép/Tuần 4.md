# Tuần 4: Công cụ mô hình hóa chức năng

## Phân tích chức năng hệ thống
- Trong khi khảo sát hệ thống ta thấy được:
    - Các yêu cầu đối với hệ thống về mặt bên ngoài.
    - Các yêu cầu về mặt chức năng
- Phân tích chức năng hệ thống sinh ra  
    ->> Application && CSDL
- PTCNHT là phân rã các chức năng thành các chức năng chi tiết hơn
- Mục tiêu cần đạt được
    - Mối quan hệ các thứ bậc giữa các chức năng
        - Chức năng to A --chia--> A1, A2, A3, A4. 
        - Khi xong hết A1, A2, A3, A4 phải hoàn thành được A
    - Mô tả chi tiết từng chức năng
    - Không còn chỗ nào không rõ nghĩa

## Công cụ mô hình hóa (3 góc nhìn để mô hình hóa chức năng)

- __BFD__ - Bussiness Function Diagram: sơ đồ phân rã chức năng
    - Khái niệm: Là công cụ biểu diễn việc __phân rã có thứ bậc__ (thứ bậc giữa các công việc)
    - Gồm 2 thành phần chính:   
        - Chức năng: từ tổng hợp tới chi tiết. __Chức năng = Động từ + Bổ ngữ (quản lý học sinh)__
        - Quan hệ phân cấp: phân cấp ngang và phân cấp dọc (nó như nhau - để nhìn cho đẹp).
    - Hai dạng:
        - Dạng chuẩn:
            - Diễn tả toàn bộ hệ thống sẽ xây dựng
        - Dạng công ty
            - Ngoài việc mô tả tới hệ thống của mình => Combine thêm các hệ thống khác tác động vào hệ thống
            - Dùng cho công ty, tổ chức lớn
    - Chú ý:
        - Phân rã 1 cha thành nhiều con
        - Khi thực hiện hết con thì sẽ xử lý xong thằng cha
        - Chức năng nhỏ nhất gọi là chức năng chi tiết
        - Không quá 3(dự án nhỏ), 6(dự án lớn)
    - Mục đích sử dụng:
        - Xác định phạm vi của hệ thống
            - vì những cái ta làm thì nó ở trong mô hình rồi
        - Hoàn thiện hệ thống
            - vì khi nhìn vào mô hình thì ta bao quát được toàn hệ thống, cái gì thọt thiết thì ta nhét vào
        - Trao đổi giữa người dùng và nhóm phát triển
    - Điểm yếu:
        - Chưa nhìn được thông tin trao đổi ngang hàng
        - Chỉ show ra cây

- Sơ đồ luồng dữ liệu - __DFD__: Data Flow Diagram
    - Khái niệm: Mối quan hệ thông tin giữa các công việc
    - Chú ý:
        - Những chức năng không có tác động lên dữ liệu(thay đổi dữ liệu) -> bị loại bỏ
    - Thành phần: 5 cái
        - Tiến trình: 
            - Hình Oval
            - Là một hoạt động có liên quan đến sự biến đổi hoặc tác động lên thông tin 
            - VD: Tổ chức lại thông tin, bổ sung thông tin, tạo ra thông tin mới

- Đặc tả chức năng - S Spec
    - Quy chuẩn
        - Tiêu đề
        - Thân:
            - Nội dung xử lý:
                - Với tiến trình đó thì hệ thống xử lý như thế nào
                - Biểu diễn = công thức toán (cho chức năng có công thức tính toán) || sơ đồ khối || ngôn ngữ tự nhiên cấu trúc hóa || Bảng quyết định (cho các chức năng có tính chất lựa chọn)