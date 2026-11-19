**CHƯƠNG 0: NỀN TẢNG MÁY TÍNH VÀ LẬP TRÌNH:**



\#



BÀI 1. MÁY TÍNH THỰC THI CHƯƠNG TRÌNH NHƯ THẾ NÀO?



1\. CPU

2\. RAM

3\. Storage

4\. Quy trình thực thi chương trình

5\. Bộ nhớ và chương trình đang chạy



BÀI 2. BIT, BYTE VÀ BIỂU DIỄN SỐ



1\. Bit và hệ nhị phân

2\. Byte

3\. Đổi nhị phân sang thập phân

4\. Đổi thập phân sang nhị phân

5\. Kiểu số nguyên không dấu

6\. Kiểu số nguyên có dấu

7\. Two's Complement

8\. Integer Overflow



BÀI 3. BIỂU DIỄN DỮ LIỆU VÀ KIỂU DỮ LIỆU



1\. Bit pattern và cách diễn giải

2\. ASCII

3\. Unicode

4\. UTF-8

5\. Unicode Scalar Value

6\. String và \&str

7\. char trong Rust

8\. Byte, Scalar Value, Grapheme Cluster và Glyph

9\. Truy cập chuỗi trong Rust

10\. Độ dài chuỗi trong Rust

11\. Cấu trúc byte UTF-8

12\. String và chuỗi C



TỔNG KẾT CHƯƠNG 0



1\. CPU - CENTRAL PROCESSING UNIT



CPU là bộ xử lý trung tâm của máy tính.



Nhiệm vụ:



\- Thực thi các lệnh của chương trình.

\- Thực hiện phép tính số học.

\- Thực hiện phép so sánh và logic.

\- Điều khiển hoạt động thực thi.

\- Phối hợp với các thành phần khác của máy tính.



CPU có thể hiểu là bộ phận trực tiếp thực hiện các chỉ thị máy.



2\. RAM - RANDOM ACCESS MEMORY



RAM là bộ nhớ truy cập ngẫu nhiên, được sử dụng để lưu dữ liệu và chương trình đang hoạt động.



Đặc điểm:



\- Truy cập dữ liệu nhanh.

\- Cho phép CPU đọc và ghi dữ liệu.

\- Lưu dữ liệu tạm thời trong quá trình hoạt động.

\- Thông thường mất dữ liệu khi mất nguồn điện.



Ví dụ:

Khi mở VS Code:



\- Các thành phần cần thiết của VS Code được nạp vào RAM.

\- CPU thực thi các lệnh của chương trình.

\- RAM lưu dữ liệu cần thiết trong quá trình hoạt động.



3\. STORAGE - BỘ NHỚ LƯU TRỮ



Storage là nơi lưu dữ liệu lâu dài.



Ví dụ:



\- HDD.

\- SSD.

\- USB.

\- Thẻ nhớ.



Đặc điểm:



\- Lưu trữ dữ liệu khi tắt máy.

\- Có thể chứa hệ điều hành, chương trình và tệp cá nhân.

\- Thường chậm hơn RAM.



Ví dụ:

Một dự án Rust được lưu trên SSD. Khi mở dự án, hệ điều hành và các chương trình cần thiết sẽ đọc dữ liệu từ SSD để sử dụng.



4\. QUY TRÌNH THỰC THI CHƯƠNG TRÌNH



Quy trình khái quát:



STORAGE

|

v

Đọc dữ liệu chương trình

|

v

RAM

|

v

CPU lấy lệnh và dữ liệu cần thiết

|

v

DECODE - Giải mã lệnh

|

v

EXECUTE - Thực thi lệnh

|

v

Ghi kết quả hoặc tiếp tục xử lý



Ba bước cơ bản của chu trình CPU:



FETCH:

Lấy lệnh từ bộ nhớ.



DECODE:

Giải mã lệnh để xác định CPU cần thực hiện điều gì.



EXECUTE:

Thực thi lệnh.



Chu trình này được lặp lại trong quá trình CPU thực thi chương trình.



5\. BỘ NHỚ VÀ CHƯƠNG TRÌNH ĐANG CHẠY



Không phải cứ một chương trình có dung lượng 500 MB trên SSD thì nó phải chiếm đúng 500 MB RAM khi chạy.



Lý do:



\- Chương trình có thể chỉ nạp một phần dữ liệu cần thiết.

\- Có dữ liệu được cấp phát trong quá trình chạy.

\- Có thư viện dùng chung.

\- Có vùng nhớ được ánh xạ từ tệp.

\- Bộ nhớ có thể được giải phóng khi không còn cần thiết.



Các khái niệm cần phân biệt:



PROCESS:

Một tiến trình đang thực thi, có không gian địa chỉ và tài nguyên được hệ điều hành quản lý.



THREAD:

Luồng thực thi bên trong một tiến trình. Một tiến trình có thể có nhiều thread.



SERVICE:

Dịch vụ chạy nền do hệ điều hành hoặc phần mềm quản lý.



1\. BIT - ĐƠN VỊ DỮ LIỆU CƠ BẢN



Bit là đơn vị dữ liệu nhỏ nhất trong mô hình biểu diễn nhị phân.



Một bit chỉ có hai trạng thái:



0 hoặc 1.



Máy tính sử dụng các trạng thái nhị phân để biểu diễn dữ liệu và xử lý thông tin.



2\. BYTE



Một byte bằng 8 bit.



1 Byte = 8 bits.



Với n bit, số tổ hợp có thể biểu diễn là:



2^n



Ví dụ:



\- 1 bit: 2 tổ hợp.

\- 2 bit: 4 tổ hợp.

\- 4 bit: 16 tổ hợp.

\- 8 bit: 256 tổ hợp.

\- 16 bit: 65.536 tổ hợp.



Lưu ý:

Số tổ hợp không đồng nghĩa với số giá trị dương có thể biểu diễn. Còn phụ thuộc kiểu dữ liệu và quy tắc diễn giải.



3\. HỆ NHỊ PHÂN



Hệ nhị phân sử dụng hai chữ số:

0 và 1.



Mỗi vị trí bit có trọng số là một lũy thừa của 2.



Ví dụ:



1101₂



Tính từ phải sang trái:



Vị trí:   3   2   1   0

Bit:      1   1   0   1

Trọng số: 8   4   2   1



Giá trị:



1×8 + 1×4 + 0×2 + 1×1 = 13



Vậy:



1101₂ = 13₁₀



4\. ĐỔI NHỊ PHÂN SANG THẬP PHÂN



Ví dụ:



10101010₂



Trọng số từ phải sang trái:



128, 64, 32, 16, 8, 4, 2, 1



Tính:



1×128 + 0×64 + 1×32 + 0×16



\- 1×8 + 0×4 + 1×2 + 0×1



\\= 128 + 32 + 8 + 2



\\= 170



Vậy:



10101010₂ = 170₁₀



5\. ĐỔI THẬP PHÂN SANG NHỊ PHÂN



Phương pháp chia liên tiếp cho 2.



Ví dụ: đổi 25 sang nhị phân.



25 / 2 = 12 dư 1

12 / 2 = 6  dư 0

6  / 2 = 3  dư 0

3  / 2 = 1  dư 1

1  / 2 = 0  dư 1



Đọc các số dư từ dưới lên:



11001₂



Vậy:



25₁₀ = 11001₂



6\. KIỂU SỐ NGUYÊN KHÔNG DẤU



Unsigned Integer là số nguyên không dấu.



Ví dụ: u8 trong Rust.



u8 sử dụng 8 bit.



Số tổ hợp:



2^8 = 256



Miền giá trị:



0 đến 255.



Một số kiểu số nguyên không dấu:



u8   : 8 bit

u16  : 16 bit

u32  : 32 bit

u64  : 64 bit

u128 : 128 bit



Công thức miền giá trị của kiểu unsigned n bit:



0 đến 2^n - 1.



Ví dụ:

u8 không thể biểu diễn số 256.



7\. KIỂU SỐ NGUYÊN CÓ DẤU



Signed Integer là số nguyên có dấu.



Ví dụ: i8 trong Rust.



i8 sử dụng 8 bit và biểu diễn cả số âm lẫn số không âm.



Miền giá trị:



\-128 đến 127.



Một số kiểu:



i8

i16

i32

i64

i128



Với kiểu signed sử dụng Two's Complement, miền giá trị của n bit là:



\-2^(n-1) đến 2^(n-1)-1.



Ví dụ:

i8 có 256 tổ hợp bit nhưng miền giá trị là -128 đến 127.



8\. TWO'S COMPLEMENT



Two's Complement là phương pháp biểu diễn số nguyên có dấu được sử dụng phổ biến trong máy tính.



Đối với số âm, quy trình tạo biểu diễn 8 bit:



Bước 1:

Viết giá trị tuyệt đối dưới dạng nhị phân 8 bit.



Bước 2:

Đảo tất cả bit:

0 thành 1.

1 thành 0.



Bước 3:

Cộng thêm 1.



Ví dụ: biểu diễn -19 bằng 8 bit.



Bước 1:

+19 = 00010011



Bước 2:

Đảo bit:



11101100



Bước 3:

Cộng 1:



11101100



\-

&#x20; ```

&#x20;   1

&#x20; ```



\---



11101101



Vậy:



\-19 = 11101101 trong biểu diễn i8.



Kiểm tra ngược:



\-128 + 64 + 32 + 8 + 4 + 1 = -19.



9\. CÁCH ĐỌC BIT PATTERN CỦA i8



Với i8, trọng số các vị trí bit:



Bit 7: -128

Bit 6: 64

Bit 5: 32

Bit 4: 16

Bit 3: 8

Bit 2: 4

Bit 1: 2

Bit 0: 1



Ví dụ:



11111111



Tính:



\-128 + 64 + 32 + 16 + 8 + 4 + 2 + 1



\\= -1



Vậy:



11111111 = -1 nếu diễn giải là i8.



Nhưng nếu diễn giải là u8:



11111111 = 255.



Cùng một bit pattern nhưng kết quả khác nhau do kiểu dữ liệu khác nhau.



10\. VÌ SAO SỬ DỤNG TWO'S COMPLEMENT?



Two's Complement cho phép hệ thống sử dụng cùng cơ chế cộng nhị phân để thực hiện phép cộng và phép trừ.



Ví dụ:



7 - 5



Có thể chuyển thành:



7 + (-5)



CPU có thể xử lý phép tính thông qua cơ chế cộng nhị phân.



Two's Complement không phải chỉ đơn giản là thêm một bit dấu. Nó là một quy tắc biểu diễn số được thiết kế để hoạt động phù hợp với phép toán nhị phân.



11\. INTEGER OVERFLOW - TRÀN SỐ NGUYÊN



Integer Overflow xảy ra khi kết quả phép toán vượt ngoài miền giá trị của kiểu dữ liệu.



Ví dụ:



i8 có miền giá trị:

\-128 đến 127.



Phép toán:



100 + 40 = 140



140 vượt quá 127 nên không thể biểu diễn bằng i8.



Một trường hợp đặc biệt:



\-(-128) = 128



128 không thể biểu diễn bằng i8.



Trong Rust, hành vi khi tràn số phụ thuộc vào cách biên dịch và phương thức được sử dụng.



Các phương thức xử lý tràn đáng chú ý:



checked\_add:

Trả về Option, báo None nếu tràn.



wrapping\_add:

Thực hiện phép cộng theo kiểu cuộn vòng.



saturating\_add:

Giới hạn kết quả tại giá trị tối đa hoặc tối thiểu.



Không nên mặc định mọi phép toán tràn đều có cùng hành vi trong mọi cấu hình.



1\. BIT PATTERN VÀ CÁCH DIỄN GIẢI



Bit pattern là một chuỗi bit.



Bản thân chuỗi bit không tự xác định nó đại diện cho loại dữ liệu nào.



Ví dụ:



01000001



Nếu diễn giải là u8:



65\.



Nếu diễn giải theo ASCII:



Ký tự A.



Điều quan trọng:

Kiểu dữ liệu và quy tắc mã hóa quyết định cách hiểu chuỗi bit.



2\. ASCII



ASCII là bộ mã ký tự cơ bản.



ASCII cơ bản có 128 mã:



0 đến 127.



Bao gồm:



\- Chữ cái tiếng Anh.

\- Chữ số.

\- Dấu câu.

\- Một số ký tự điều khiển.



Ví dụ:



A = 65 = 01000001₂.



Trong UTF-8, các mã ASCII cơ bản được giữ nguyên bằng một byte.



ASCII không phải là tên khác của Unicode.



3\. UNICODE



Unicode là tiêu chuẩn dùng để gán mã số cho các ký tự và ký hiệu trong hệ thống văn bản.



Ví dụ:



A  = U+0041

é  = U+00E9

ế  = U+1EBF

🙂 = U+1F642



Unicode bao phủ nhiều hệ thống chữ viết và ký hiệu trên thế giới.



Unicode Code Point:

Một mã số trong không gian mã Unicode.



Unicode Scalar Value:

Một giá trị Unicode hợp lệ, không bao gồm vùng surrogate từ U+D800 đến U+DFFF.



Lưu ý:

Không phải mọi Unicode code point đều là Unicode scalar value.



4\. UTF-8



UTF-8 là phương pháp mã hóa Unicode thành các byte.



Một Unicode scalar value được mã hóa bằng từ 1 đến 4 byte.



Ví dụ:



A  : 1 byte

ñ  : 2 byte

ế  : 3 byte

🙂 : 4 byte



Độ dài UTF-8 thay đổi theo giá trị cần mã hóa.



UTF-8 có khả năng tương thích với ASCII cơ bản.



Ví dụ:



Ký tự A có mã ASCII 65.



Trong UTF-8, A vẫn được lưu bằng byte có giá trị 65.



5\. CẤU TRÚC BYTE UTF-8



Các mẫu bit cơ bản:



ASCII:

0xxxxxxx



Byte mở đầu chuỗi 2 byte:

110xxxxx



Byte mở đầu chuỗi 3 byte:

1110xxxx



Byte mở đầu chuỗi 4 byte:

11110xxx



Byte tiếp nối:

10xxxxxx



Ví dụ:



Một chuỗi UTF-8 4 byte gồm:



1 byte mở đầu có dạng 11110xxx.

3 byte tiếp nối có dạng 10xxxxxx.



Lưu ý:

Không được nhầm byte tiếp nối với byte mở đầu.



6\. STRING TRONG RUST



String là kiểu dữ liệu chuỗi có quyền sở hữu dữ liệu.



Đặc điểm:



\- Lưu văn bản UTF-8 hợp lệ.

\- Có thể thay đổi nội dung khi có quyền sở hữu phù hợp.

\- Quản lý vùng dữ liệu của chuỗi.

\- Có thể được mở rộng hoặc thu nhỏ.



Ví dụ:



let s = String::from("Hello");



String sở hữu dữ liệu văn bản của nó.



7\. \&str TRONG RUST



\&str là một tham chiếu dạng lát cắt đến dữ liệu văn bản UTF-8 hợp lệ.



Ví dụ:



let owner = String::from("Rust");

let view: \&str = \&owner;



Trong ví dụ:



\- owner sở hữu dữ liệu.

\- view tham chiếu đến dữ liệu của owner.

\- view không tạo ra một bản sao độc lập của toàn bộ chuỗi.



Về mặt khái niệm, \&str chứa:



\- Con trỏ đến dữ liệu.

\- Độ dài tính bằng byte.



\&str không bắt buộc dữ liệu phải nằm trên heap.



8\. CHAR TRONG RUST



char là kiểu dữ liệu biểu diễn một Unicode scalar value.



Kích thước:



4 byte.



Ví dụ:



let c: char = 'A';

let d: char = 'ế';

let e: char = '🙂';



Mỗi giá trị trên là một char hợp lệ.



Lưu ý:

Kích thước char luôn là 4 byte trong Rust, nhưng khi mã hóa thành UTF-8, các ký tự có thể chiếm từ 1 đến 4 byte.



char không đồng nghĩa với một ký tự hiển thị hoàn chỉnh trong mọi trường hợp.



9\. BỐN KHÁI NIỆM CẦN PHÂN BIỆT



BYTE:

Đơn vị dữ liệu lưu trữ.



UNICODE SCALAR VALUE:

Một giá trị Unicode hợp lệ.



GRAPHEME CLUSTER:

Một nhóm gồm một hoặc nhiều Unicode scalar value mà người dùng thường cảm nhận là một ký tự.



GLYPH:

Hình dạng được font chữ sử dụng để hiển thị văn bản.



Ví dụ:



e + dấu sắc kết hợp.



Có thể có:



\- 3 byte UTF-8.

\- 2 Unicode scalar value.

\- 1 grapheme cluster.

\- Hình dạng hiển thị phụ thuộc font và hệ thống dựng chữ.



Grapheme cluster và glyph không phải hai khái niệm hoàn toàn giống nhau.



10\. UNICODE NORMALIZATION



Một số văn bản có thể trông giống nhau nhưng được biểu diễn bằng các dãy Unicode scalar value khác nhau.



Ví dụ:



Dạng dựng sẵn:

é = U+00E9.



Dạng kết hợp:

e = U+0065.

Dấu sắc kết hợp = U+0301.



Dạng dựng sẵn:



\- 2 byte UTF-8.

\- 1 scalar value.



Dạng kết hợp:



\- 3 byte UTF-8.

\- 2 scalar value.



Hai dạng có thể hiển thị giống nhau nhưng khác nhau về biểu diễn bên trong.



11\. STRING INDEXING - TRUY CẬP CHUỖI



Rust không cho phép truy cập String bằng chỉ số trực tiếp như:



s\[0]



Lý do:



String sử dụng UTF-8.



Một Unicode scalar value có thể chiếm nhiều byte.



Nếu truy cập tùy ý theo chỉ số byte, vị trí đó có thể nằm giữa mã hóa của một ký tự.



Rust yêu cầu thao tác chuỗi phải tôn trọng ranh giới UTF-8.



Ví dụ:



let s = String::from("é");



Ký tự é chiếm 2 byte UTF-8.



Phạm vi:



\&s\[0..1]



Không hợp lệ vì byte thứ nhất không tạo thành một chuỗi UTF-8 hoàn chỉnh.



Việc lấy lát cắt String với ranh giới byte không hợp lệ sẽ gây panic.



12\. ĐỘ DÀI CHUỖI TRONG RUST



Phương thức len():



Đếm số byte.



Phương thức chars().count():



Đếm số Unicode scalar value.



Muốn đếm grapheme cluster:



Có thể sử dụng crate unicode-segmentation.



Ví dụ:



let s = String::from("A🙂");



s.len() = 5



s.chars().count() = 2



Giải thích:



A  = 1 byte.

🙂 = 4 byte.



Tổng:

5 byte.



Số Unicode scalar value:

2\\.



Ví dụ khác:



let s = String::from("ABCế");



len() = 6

chars().count() = 4



Giải thích:



A = 1 byte.

B = 1 byte.

C = 1 byte.

ế = 3 byte.



Tổng:

6 byte.



13\. STRING VÀ CHUỖI C



Chuỗi C truyền thống thường sử dụng byte null 0x00 để đánh dấu kết thúc.



Rust \&str không sử dụng cơ chế đó.



\&str xác định vùng dữ liệu bằng:



\- Con trỏ.

\- Độ dài.



Ví dụ:



let s: \&str = "Hello";



println!("{}", s.len());



Kết quả:



5



Rust không cần tìm byte null để xác định độ dài chuỗi.



1\. MÁY TÍNH



CPU:

Thực thi lệnh.



RAM:

Lưu dữ liệu và chương trình đang hoạt động.



Storage:

Lưu trữ dữ liệu lâu dài.



FETCH:

Lấy lệnh.



DECODE:

Giải mã lệnh.



EXECUTE:

Thực thi lệnh.



2\. BIT VÀ BYTE



1 Byte = 8 bits.



n bit có 2^n tổ hợp.



u8:

0 đến 255.



i8:

\-128 đến 127.



3\. TWO'S COMPLEMENT



Biểu diễn số âm:



1\. Viết số dương dưới dạng nhị phân.

2\. Đảo toàn bộ bit.

3\. Cộng 1.



Mục đích:

Hỗ trợ xử lý số âm bằng cơ chế phép toán nhị phân thống nhất.



4\. UNICODE VÀ UTF-8



ASCII:

128 mã cơ bản.



Unicode:

Tiêu chuẩn gán mã số cho ký tự và ký hiệu.



UTF-8:

Mã hóa Unicode thành 1 đến 4 byte.



Unicode scalar value:

Giá trị Unicode hợp lệ, không thuộc vùng surrogate.



5\. RUST STRING



String:

Sở hữu dữ liệu văn bản UTF-8.



\&str:

Tham chiếu dạng lát cắt đến văn bản UTF-8.



char:

Một Unicode scalar value, kích thước 4 byte.



len():

Đếm byte.



chars().count():

Đếm Unicode scalar value.



Grapheme cluster:

Nhóm scalar value thường được cảm nhận như một ký tự.



Glyph:

Hình dạng hiển thị của văn bản.



6\. NHỮNG ĐIỂM TUYỆT ĐỐI KHÔNG ĐƯỢC NHẦM



\- 1 ký tự hiển thị không nhất thiết bằng 1 byte.

\- 1 Unicode scalar value không nhất thiết bằng 1 byte UTF-8.

\- char không đồng nghĩa với grapheme cluster.

\- String::len() không đếm ký tự hiển thị.

\- u8 và i8 có thể diễn giải cùng một bit pattern thành hai giá trị khác nhau.

\- \&str không cần byte null kết thúc.

\- String không thể truy cập trực tiếp bằng s\[0].

\- i8 có miền giá trị -128 đến 127, không phải -127 đến 127.

\- Two's Complement phải có bước cộng 1 sau khi đảo bit.





