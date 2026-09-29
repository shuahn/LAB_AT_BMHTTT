

Họ và tên: Lê Thị Anh Thư
MSSV: 1150070042
Lớp: 11TMĐT

LAB 4: KHẢO SÁT VÀ ĐÁNH GIÁ BỀ MẶT MẠNG BẰNG NMAP


PHIÊN BẢN MÔI TRƯỜNG THỰC HÀNH
Máy quét (Attacker): Kali Linux (IP: "192.168.56.129/24") | Nmap v7.99
Máy mục tiêu (Target):Metasploitable 2 (IP: "192.168.56.128/24") | Kernel Linux 2.6.X
Phần mềm ảo hóa: VMware Workstation
Chế độ mạng: Custom VMnet1 (Host-Only - Cách ly hoàn toàn với Internet)


CÁCH DỰNG MÔI TRƯỜNG THỰC HÀNH

1. Giai đoạn 1: Cài đặt công cụ (Chế độ NAT)
  - Chuyển Card mạng Kali Linux sang NAT
  - Cập nhật và cài đặt Nmap, Zenmap, xsltproc trên Terminal Kali:
  - Tắt máy ảo Kali Linux sau khi hoàn tất.

2. Giai đoạn 2: Thiết lập mạng cách ly (Chế độ Host-Only)
   - Chuyển Card mạng của cả "Kali Linux" và "Metasploitable 2" về "VMnet1 (Host-Only)".
   - Khởi động 2 máy ảo, kiểm tra IP ("ifconfig" / "ip -br addr").
   - Kiểm tra kết nối từ Kali Linux tới máy mục tiêu:
     
     

 CÁC TÌNH HUỐNG THỰC HIỆN VÀ KẾT QUẢ (PASS/FAIL)

1. Quét Host Discovery (Tìm máy sống) --> PASS--> Phát hiện 3 hosts (".128", ".129", ".254") 
2. Quét cổng TCP bằng SYN Scan -->PASS-->Phát hiện 23 cổng TCP dạng "open"
3. Nhận diện dịch vụ và phiên bản -->PASS -->Phát hiện vsftpd 2.3.4, Apache 2.2.8,... 
4. Dò tìm Hệ điều hành (OS Fingerprinting) -->PASS--> Nhận diện chính xác Linux 2.6.9 - 2.6.33 
5. Quét kịch bản NSE kiểm tra MS17-010 -->PASS -->Thực thi thành công (Không dính MS17-010) 
6. Báo cáo HTML & hiển thị trên Browser -->PASS-->Xuất báo cáo HTML và mở bằng Firefox 
