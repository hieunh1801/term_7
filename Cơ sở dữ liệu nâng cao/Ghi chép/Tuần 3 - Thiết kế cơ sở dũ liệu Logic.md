# Thiết kế cơ sở dữ liệu Logic

## Mục tiêu

- Chuyển đổi mô hình __thiết kế khái niệm__ ==> Mô hình quan hệ

- Thiế kế __phi chuẩn hóa__ đáp ứng được tối ưu hệ thống, __mở rộng hệ thống__

## Khái niệm

- Mô hình CSDL quan hệ 
- Một quan hệ
- Mô hình quan hệ
- Lược đồ quan hệ
    - R là quan hệ
    - Dom là kiểu quan hệ được lưu trữ
- Khi nói đến quan hệ => nói đến mối quan hệ thực sự
- Sự tương ứng mô hình thực thể và mô hình quan hệ
- Các tính chất của 1 quan hệ
    - giá trị đưa vào cột là đơn trị
- Mối quan hệ:
    - Trong mô hình quan hệ: chỉ chấp nhận 1-1 hoặc 1-n.
    - Quan hệ n-n phải loại bỏ.
- Khóa chính: xác định duy nhất, mọi quan hệ đều có khóa chính
    - Nghĩa là: bảng nào cũng phải có khóa
    - Trong khi cài đặt SQL - mức vật lý - có những bảng ta không thiết lập khóa
- Các ràng buộc:

- Ràng buộc miền giá trị
- Phương pháp thiết kế
    - Top-down:
        - Các quy tắc chuyển đổi __mô hình thực thể__ sang mô hình quan hệ:
            - 1-1
            - 1-n
            - n-n
            - Đa trị -> đơn trị
            - __Chú ý:__ trong mô hình thực thể: không có khóa ngoại, khóa ngoại sinh ra khi ta chuyển đổi các mối quan hệ
            
    - Bottom-up:
        - Phụ thuộc hàm -> xác định được đâu là khóa và chuẩn hóa 1NF, 2NF, 3NF, BCNF dựa trên phụ thuộc hàm
        - Phụ thuộc hàm một phần, đầy đủ, bắc cầu. quan hệ phản xạ, bao đóng
        - Khóa tối thiểu(chính là khóa bình thường ta gọi), siêu khóa
        - Thuật toán tìm khóa.

- Tips, Trick

## Xử lý các mối quan hệ đặc biệt
- Đa trị:
    - VD: trong bảng điểm 
        - có điểm của nhiều sinh viên. -> tách ra thành 1 nhóm
        - có ít nhất 2 giáo viên chấm thi. -> tách ra thành 1 nhóm
- Thuộc tính phức hợp: tách thành nhiều thuộc tính nhỏ hơn  
    - VD: quê quán: tách thành: xã, phường, thị trấn, thành phố.

## Các dạng chuẩn và nâng chuẩn

- 1NF: 
    - Tách các thuộc tính lặp hay không tồn tại thuộc tính lặp hoặc thuộc tính đa trị 
    - Vì 1 ô chỉ lưu 1 giá trị, do đó phải loại bỏ thuộc tính lặp để tối thiểu có thể lưu trữ trong database

- 2NF: 
    - Một quan hệ ở dạng chuẩn 2 nếu nó đã ở dạng chuẩn 1 và không tồn tại phụ thuộc hàm bộ phận vào khoá. 
    - Phụ thuộc vào một bộ phận của khóa
        - VD: SinhVien(__ma_sinh_vien__, __ma_mon_hoc__, ten_mon_hoc, so_hoc_trinh, diem)
            - {__ma_sinh_vien__, __ma_mon_hoc__} -> {diem}
            - {__ma_mon_hoc__} -> {ten_mon_hoc, so_hoc_trinh} (phụ thuộc vào 1 phần của khóa)

- 3NF:
    - Đạt 2NF và không tồn tại phụ thuộc hàm ngoài khóa (hay phụ thuộc hàm bắc cầu)
    - VD: SinhVien(__Masv__,Hoten,NS,GT,Malop,Tenlop)
        - MaLop -> TenLop
        - Masv -> MaLop -> TenLop (bắc cầu)

- BCNF:
    - Đạt 3NF và không tồn tại phụ thuộc hàm có nguồn là thuộc tính không khóa, đích là thuộc tính khóa. 
    - VD: Sinhvien(__Malop__,__MaMH__, diem, MaSV)
        - MaSV -> Malop: Malop là thuộc tính khóa, MaSV là thuộc tính không khóa

## Chuyển dổi giữa các ERD 

- ERD mở rộng: ta nghĩ ra cái gì ta lưu cái đó lại
- ERD kinh điển: có thể lưu trữ được rồi. 
    - Chuẩn 1NF: Loại bỏ các thuộc tính đa trị là OK

- ERD hạn chế: bó buộc thêm một số thứ

## Bài tập về nhà

- Bài tập 1: Quản lý bán sách
    - Từ kinh điển về hạn chế => mô hình quan hệ
    
- Bài tập 2: Quản lý đào tạo
    - Viết thành các step 
    - Từ mô hình thực thể => tạo ra mô hình quan hệ
        - Cách 1: Mô hình mở rộng => mô hình quan hệ. Sau đó chuẩn hóa 1NF, 2NF, 3NF
        - Cách 2: Từ mô hình mở rộng => mô hình kinh điển => mô hình hạn chế => mô hình quan hệ
