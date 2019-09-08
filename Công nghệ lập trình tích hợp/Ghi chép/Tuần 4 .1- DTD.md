# Tuần 4: Sử dụng DTD tạo tài liệu XML hợp lệ

## DTD là gì?

- DTD: __Document Type Definition__ - Định nghĩa kiểu.
    - Một file XML
        - Tự định nghĩa thẻ
        - Lưu trữ dữ liệu được truyền giữa các hệ thống => Có những kiểu dữ liệu chỉ có trên hệ thống này mà không có trên hệ thống khác => phải định kiểu của dữ liệu
        - DTD bản chất cũng là thẻ XML => lưu trữ kiểu của dữ liệu

- Ví dụ:
    - PCdata: dữ liệu mà máy có thể đọc được - file nhị phân, file ảnh, file audio

## Using DTD

- Cách 1: Khai báo trực tiếp trong Document

- Cách 2: Tách ra 1 file.dtd và trỏ tới file đó

## Khai báo trong DTD

- Element - Đại diện cho các node
- ATTLIST - mang tính định danh - duy nhất - trường id

```XML
<!-- CÁCH 1-->
<Student>
    <Id>001</Id> <!-- Id đóng vai trò là element. Khai báo DTD của nó trong ELEMENT-->
    <Name>Nguyễn Hữu Hiếu</Name>
    <Age>21</Age>
</Student>

<!-- CÁCH 2-->
<Student Id="001"> <!-- Id sẽ đóng vai trò là attribute - thuộc tính. Khi này ta cần khai báo DTD của nó trong ATTLIST-->
    <Name>Nguyễn Hữu Hiếu</Name>
    <Age>21</Age>
</Student>
```

## Sử dụng kiểu thuộc tính
- CData(ngày xưa) hoặc PCData(hiện tại dùng)

## Ví dụ DTD
```XML
<!Doctype novel[
    <!Element novel (foreword, chapter*)>
    <!Element foreword (paragraph+)>
    <!Element chapter (paragraph+)>
    <!-- Khai báo kiểu một element -->
    <!Element paragraph (#PCData)> 
    <!-- Khai báo kiểu của một attribute: Trong thẻ chapter -> có một attribute là number -->
    <!ATTRIBUTE chapter number CDATA #REQUIRED> 
]>
<novel>
    <!-- Khai báo một Element -->
    <foreword>
        ABCXYZ
    <foreword>
    <!-- Khai báo một thuộc tính -->
    <chapter number="01">
        ABC XYZ
    </chapter>
</novel>
```