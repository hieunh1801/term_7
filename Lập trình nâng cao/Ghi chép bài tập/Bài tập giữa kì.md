# Bài tập giữa kì - Xây dựng Stock Exchange(Sàn giao dịch chứng khoán)

- Giao dịch chứng khoán nhỏ

- Use TreeSet, TreeMap, HashMap

- Chức năng:

- Quản lý các Registered Traders: người chơi cổ phiếu 
    - Tạo class Trader lưu thông tin đầy đủ của 1 người
    - Lưu danh sách người chơi dưới dạng TreeMap<String, Trader> (string lưu mã người dùng)
        - ListRegisteredTraders = TreeMap<String, Trader>
- Những người login vào traders 
    - Dùng TreeSet<Trader> => ô nào login thì ta nhét vào đây => kiểm tra đã login để thực hiện giao dịch (true, false)
        - LoggedInTraders = TreeSet<Trader>
        
- MailBox Dùng Queue Cài Mailbox dưới dạng linklist => lưu string đầu vào. Khi nào mua/ bán thành công sẽ gửi mail box cho người đó.

- Trên sàn lưu ListedStock để mua bán chứng khoán: listStock để lưu các cổ phiếu của các công ty
    - HashMap(String, Stock) => string lưu mã chứng khoán

- Hàng đợi bán:
    - Nhiều người bán, đặt mã bao nhiêu, cổ phiếu gì
    - Mỗi mã cổ phiếu ta tạo ra hàng đợi lệnh bán. 
        - Hàng đợi ưu tiên ta sếp theo giá 1, giá thấp sẽ ưu tiên ở đầu hàng. 
        - VD: cùng bán cổ phiếu FPT vào 1 dòng. ai đặt lệnh bán: giá thấp sẽ được ưu tiên ở đầu hàng

- Hàng đợi mua
    - Nhiều người đặt mua
    - Mỗi cổ phiếu ta tạo ra một hàng đợi mua
        - Ai mua giá cao sẽ được mua trước

- Mỗi 1 phút sẽ duyệt song song 2 hàng đợi để khớp: ai bán rẻ thì được bán trước, ai mua đắt thì được mua trước. Chú ý: người bán nhiều: người bán 1000, người mua 200, 300 ... thì 1 người bán bán cho nhiều người hoặc ngược lại

- Mua là mua theo giá bán.
- Lệnh mua là giá cao nhất chịu được.
- VD: A đặt mua 1000 cổ phiếu giá 7 đồng. B bán 500 cổ phiếu giá 5 đồng
    => Khi đó A sẽ mua theo giá của B giá 500 cổ phiếu giá 5 đồng
- Chú ý: Mỗi 5' ta lại khớp 2 hàng đợi để xem ai bán được cho ai, ai mua của ai