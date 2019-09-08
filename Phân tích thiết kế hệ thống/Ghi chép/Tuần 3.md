# Khảo sát hệ thống

## Tổng quan về khảo sát
- Mục tiêu:
    - Khảo sát hiện trạng của hệ thống 
        - Quan sát bề ngoài, chưa phân tích gì, chỉ thu thập thông tin cần thiết.
        - Bản thân hệ thống đã hoạt động rồi. Ta làm hệ thống phần mềm cho họ.
    - Tìm ra điểm thiếu xót và đưa ra phương án giải quyết
        - Lý do: tại sao lại phải làm hệ thống? vì hệ thống hiện tại còn thiết xót => tìm ra lỗi và giải quyết yếu kém đó.
        - Cách tìm ra điểm thiếu xót: 
            - Phầm mềm xây dựng cho nhân viên => khi nhân viên cảm thấy khó khăn khi làm việc => đó chính là điểm yếu của hệ thống
            - Ta đi hỏi trực tiếp người sử dụng hệ thống
    - Xác định yêu cầu của hệ thống trong tương lai

- Kết quả sau khi khảo sát: Hồ sơ xác lập dự án
    - Từ việc Đưa ra một phương án khả thi để khắc phục thiết xót => tạo ra các tài liệu
        - Yêu cầu chức năng, phi chức năng: 
            - Về mặt chức năng: giúp giải quyết được đầy đủ nghiệp vụ, rồi sau đó cải tiến thêm cũng được
            - Phi chức năng: thiết kế giao diện tương tác cố gắng khắc phục về mặt thực hiện, làm ít => được nhiều. chính là làm ra thêm các thống kê, báo cáo, mẫu biểu.
        - Hồ sơ vào ra, tài nguyên
            - Hồ sơ vào: người dùng nhập vào. Ra: hệ thống đưa ra
            - Tài nguyên: các tài nguyên hệ thống cần lưu trữ
            - Ra = Vào + Tài nguyên + Xử lý thông tin trong hệ thống
            - Mục tiêu: càng đưa ra nhiều càng tốt
        - Dự trù thiết bị phần cứng, phần mềm.
            - Bản thân tổ chức đã có phần cứng, phần mềm rồi. VD: diệt virus
        - Lịch trình làm việc sơ bộ
            - Kế hoạch thực hiện để bám sát.

- Tiếp cận tổ chức
    - Ba đặc trưng
        - Mô hình tổ chức
        - Mô hình quản lý
        - Mô hình nghiệp vụ(chủ yếu: vì phần mềm để giải quyết nghiệp vụ)
    - Tiến trình tiếp cận tổ chức
        - Step 1: Khảo sát tổ chức. VD: Thư viện
            - Phòng mượn, trả --> liên quan tới mượn trả sách (focus)
            - Kho sách --> liên quan tới việc trả sách (focus)
            - Phòng đọc
            - Phòng Internet
            - Ban quản lý TV
            - Phòng photo
        - Step 2: Khảo sát quản lý: trong 2 bộ phận trên, khảo sát ai làm gì để phục vụ việc mượn trả sách
        - Step 3: Khảo sát quy trình nghiệp vụ: trong các bộ phận trên, tìm hiểu công việc của mỗi người. Người ta có phàn nàn cái gì không => điểm yếu
        - Step 4: Khi mà tổ chức có nhiều hệ thống thì ta làm thêm bước phác họa phát triển hệ thống, ảnh hưởng của hệ thống ta đang khảo sát tới các hệ thống khác, có thể connect tới hệ thống khác bằng cách nào.

- Yêu cầu với phân tích viên
    - Phẩm chất cần có
        - Khả năng quan sát
        - Có cách nhìn đa chiều
        - Khả năng ghi chép = các mô hình

## Nội dung và quy trình khảo sát
- Nội dung khảo sát
    - Cơ cấu tổ chức:
        - Là những bộ phận tham gia trực tiếp vào bài toán của ta
        - Phần mềm của ta có chức năng gì?
        - Để thực hiện chức năng chính thì có bao nhiêu bộ phận tham gia? 
    - Chức năng, nhiệm vụ và phân cấp quyền hạn
    - Các tài liệu và  đặc trưng sử dụng
        - Hồ sơ đầu vào và ra
        - Ta cần hồ sơ ra trước để xác định mục tiêu của hệ thống: chính là các báo cáo, thống kê, mẫu biểu
    - Các quy tắc nghiệp vụ, quy trình xử lý
        - đi chi tiết vào nghiệp vụ
    - Chính sách và hướng dẫn
        - Luật pháp
    - Nguồn lực 
    - Điều kiện môi trường
    - Sự mong đợi về hệ thống mới
        - Người ta mong cái gì trong hệ thống mới
        - Cái gì đáp ứng được, cái gì không
- Quy trình khảo sát
    - Phát hiện, thu thập
    - Bổ sung, hoàn thiện
    - Tổng hợp, phân loại
    - Hợp thức hóa
## Các phương pháp sử dụng để khảo sát

- Phương pháp truyền thống
    - Phỏng vấn
    - Quan sát tại chỗ: xem người ta làm. quan sát liên tục, nhiều lần và đánh 
    - Điều tra bảng hỏi: tạo ra phiếu khảo sát và cho người dùng tích tích
    - Nghiên cứu tài liệu viết: cực kì quan trọng trong việc phân tích dữ liệu

- Phương pháp hiện đại
    - Thiết kế ứng dụng liên kết
    - Hệ thống trợ giúp nhóm
    - Công cụ CASE
    - Làm bản mẫu


## Hướng dẫn làm bài tập 1
- Mô tả: viết bằng lời
    - Nhiệm vụ cơ bản
        - Hệ thống có chức năng chính là gì => Chỉ thực việc công việc cho 1 việc cụ thể. vì bài tập là nhóm
        - Vẽ hoặc viết đều OK
    - __Cơ cấu tổ chức__:
        - Để thực hiện nhiệm vụ trên 
            - Bao nhiêu bộ phận tham gia
            - Vai trò của từng bộ phận
            - Mối quan hệ giữa các bộ phận
        - Tìm các bộ phận trong mô hình tổ chức tham gia việc mà ta xem xét

    - Quy trình xử lý và quy tắc quản lý
        - Hệ thống có quy trình nghiệp vụ nào => liệt kê ra
        - Ứng với mỗi quy trình nghiệp vụ     => ta mô tả chi tiết ra
    
    - Mẫu biểu: 
        - Các mẫu biểu

- Mô hình hóa hệ thống: 2 loại - vẽ bằng mô hình
    - Mô hình tiến trình nghiệp vụ(tổng quan về hệ thống)
        - Kí hiệu sử dụng cho 3 phần
            - Luồng thông tin phải có tên
            - Bộ phận trong hệ thống
            - Tác nhân tác động vào hệ thống
        - __Khi vẽ các mô hình :__ Ta vẽ các đỉnh trước(bộ phận, tác nhân) => cung sau(mối quạ hệ)
        - Vẽ các bộ phân trước => tác nhân sau => luông thông tin cuối cùng
        - Các bộ phận vẽ thế nào?
            - Thông tin trong các bộ phận tương ứng với cơ cấu tổ chức đã liệt kê
        - Tác nhân như thế nào?
            - Xem trong nhiệm vụ cơ bản: cái nào lấy thông tin vào, cái nào lấy thông tin ra
        - Luồng thông tin:
            - Đọc lại nghiệp vụ sẽ xác định được luồng thông tin
    - Biểu đồ hoạt động (mô tả chi tiết nghiệp vụ)
        - Với mỗi quy trình nghiệp vụ sẽ vẽ bấy nhiêu biểu đồ hoạt động
        - Kí hiêu:
            - Điểm bắt đầu, kết thúc
            - Công việc
            - Rẽ nhánh (đúng/ sai)
            - Giấy tờ giao dịch (mẫu biểu) mô tả  trên giấy tờ, mẫu biểu vào ra hệ thống
            - Kho dữ liệu
            - __Luồng dữ liệu: nét đứt__
        - Làm sao vẽ:
            - Xác định đối tượng tham gia vào hoạt động của mình
            - 

- Chú ý: Mô hình và mô tả cần tinh chỉnh lẫn nhau
- Xây dựng hồ sơ dự án 
    - Hồ sơ vào ra
        - Vào từ quy trình  nào ra quy trình nào, mô tả chi tiết
    - Tài nguyên lưu trữ, ghi ra
    - Nhóm người dùng hệ thống: về mặt nghiệp vụ 
        - Dựa vào cơ cấu tổ chức phân định
    - Dự trù thiết bị
        - Phần cứng
        - Phần mềm
