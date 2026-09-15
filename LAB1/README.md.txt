Sinh viên thực hiện: Lê Thị Anh Thư
Lớp: 11_TMĐT
MSSV: 1150070042


Lab 1.2: Bắt gói tin Telnet – SSH


1. Nội dung đã thực hiện
- Thiết lập môi trường mạng lab:
    + Cài đặt máy ảo Windows Server 2008 (10.0.0.1/24). 
    + Cấu hình card mạng máy ảo chế độ Internal Network (tên: lab_network, Promiscuous Mode: Allow All). 
    + Cài đặt Kali Linux (10.0.0.2/24) kết nối chung mạng nội bộ. 
- Cấu hình dịch vụ & Tài khoản:
    + Cài đặt và bật dịch vụ Telnet Server trên Windows Server 2008. 
    + Tạo User sinh viên lethianhthu và cấp quyền vào nhóm TelnetClients. 
- Thực hành 
   + Kiểm tra thông mạng bằng lệnh ping giữa Kali Linux và Windows Server. 
   + Sử dụng Wireshark trên Kali Linux chọn interface eth0 để bắt gói tin. 
   + Thực hiện kết nối từ xa bằng telnet 10.0.0.1 và đăng nhập tài khoản sinh viên. 

2. Kết quả thực hiện
- Kết nối thông suốt: Khởi tạo thành công phiên làm việc từ xa từ Kali Linux tới Windows Server qua giao thức Telnet. 
- Bắt gói tin Telnet thành công:
   + Wireshark bắt trọn toàn bộ lưu lượng dữ liệu trên cổng TCP 23. 
   + Phân tích cho thấy Telnet không mã hóa dữ liệu; lộ rõ tên đăng nhập lethianhthu, mật khẩu và các lệnh thực thi trong phiên kết nối. 


