LAB 2 – MÃ HÓA ĐỐI XỨNG HIỆN ĐẠI

Thông tin sinh viên
- Họ và tên: Lê Thị Anh Thư
- MSSV: 1150070042
- Môn học: An toàn và bảo mật hệ thống thông tin
- Bài thực hành: LAB 2 – Mã hóa đối xứng hiện đại


Yêu cầu môi trường
- Windows và Apache NetBeans IDE 25.
- JDK 17 và Maven (NetBeans hỗ trợ chạy project Maven).
- Microsoft SQL Server và SQL Server Management Studio (SSMS).
- SQL Server JDBC Driver "12.8.1.jre11" và BouncyCastle "bcprov-jdk18on" (khai báo trong "pom.xml").
- Python 3, Tkinter và thư viện "cryptography" cho bài AES-CBC.

Hướng dẫn chạy phần Java bằng NetBeans:
1. Mở NetBeans → File → Open Project...
2. Chọn thư mục "LAB2_MaHoaHienDai_AnhThu" (thư mục chứa `pom.xml`).
3. Nhấp chuột phải project → Clean and Build
4. Nhấn Run Project (F6). Lớp khởi chạy được cấu hình là "week_02.frm_Menu".
5. Từ menu, chọn thuật toán hoặc chức năng muốn kiểm thử.

Nếu chạy không được, kiểm tra JDK 17, các dependency Maven và cấu hình "exec.mainClass" trong "pom.xml".

Hướng dẫn chuẩn bị SQL Server
1. Mở "SSMS", kết nối với SQL Server bằng tài khoản có quyền tạo cơ sở dữ liệu.
2. Chạy "01_Tao_CSDL.sql" để tạo database "LAB2_MaHoaHienDai" và các bảng "dbo.app_users", "dbo.crypto_history".
3. Xem và điều chỉnh "02_Tao_Tai_Khoan_SQL.sql" để sử dụng "mật khẩu thực hành riêng", rồi chạy nhằm tạo tài khoản "lab2_user" và phân quyền.
4. Trong ứng dụng Java, nhấn "Kết nối SQL Server", nhập server, port, database, user và mật khẩu.
5. Nhấn "Test Connection". Khi kết nối thành công, mở "Xem lịch sử" để kiểm tra bản ghi.

"Cấu hình đã dùng khi thực hành: server "127.0.0.1", port "14333", database "LAB2_MaHoaHienDai", user "lab2_user"


Hướng dẫn chạy AES-CBC bằng Python
Mở Command Prompt:

py --version
py -m pip install cryptography
cd /d C:\duong-dan-den\LAB2\LAB2_Python
py aes_cbc_gui.py --self-test
py aes_cbc_gui.py


Dòng lệnh `cd` cần thay bằng đường dẫn thực tế sau khi giải nén. Khi tự kiểm thử đúng, chương trình sẽ hiển thị:


SELF-TEST OK: 4 thông điệp mã hóa/giải mã đúng, sai khóa bị phát hiện.


Trong giao diện Tkinter: chọn "Generate Key → Generate IV → nhập Plaintext → Encrypt → xóa Plaintext → Decrypt". Có thể kiểm thử "Save File" và "Open File"; file lưu IV và bản mã, không lưu khóa.




# LAB2_1150070042_LeThiAnhThu
