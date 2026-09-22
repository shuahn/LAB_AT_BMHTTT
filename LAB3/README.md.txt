LAB 3: Các mối đe dọa và tài sản (Threats & Assets)

- Họ và tên: Lê Thị Anh Thư
- MSSV: 1150070042
- Lớp :11TMĐT
- Phiên bản môi trường: Windows 2025, Python 3.11, Sysmon

1. Cách dựng môi trường
- Cài đặt và cấu hình Sysmon trên hệ thống ảo hóa sử dụng file cấu hình `sysmon-lab.xml` để theo dõi các tiến trình và sự kiện hệ thống.
- Thiết lập môi trường thực thi Python cục bộ để chạy script `local_load_test.py`.
- Chuẩn bị các thư mục dữ liệu mẫu, bao gồm:
  - Thư mục dữ liệu tấn công mẫu (`ddos_sample.csv`, `mailbomb_sample.csv`).
  - Thư mục phân tích tấn công xã hội (`phishing_email.txt`, `social_engineering_cases.csv`).
  - Thư mục giao diện web tĩnh (`www/index.html`).

 2. Các tình huống đã thực hiện
- Giám sát hệ thống: Triển khai Sysmon với cấu hình tùy chỉnh để thu thập log hoạt động và ghi nhận các sự kiện tiến trình đáng ngờ.
- Kiểm tra tải ứng dụng web: Chạy script `local_load_test.py` trỏ tới địa chỉ cục bộ `127.0.0.1:8080` nhằm kiểm tra khả năng chịu tải và mô phỏng các mẫu lưu lượng truy cập bất thường.
- Phân tích mối đe dọa xã hội: Đọc và phân tích cấu trúc của mẫu email lừa đảo (`phishing_email.txt`) cùng các kịch bản kỹ nghệ xã hội.

3. Kết quả (PASS/FAIL)
- Cấu hình và ghi nhận log Sysmon: Thành công
- Kiểm tra tải ứng dụng web cục bộ (`local_load_test.py`): Thành công
- Phân tích mẫu tấn công xã hội và phishing: Thành công


4. Lỗi gặp phải và cách khắc phục
- Lỗi : Không thể tải trực tiếp các gói phần mềm và công cụ (Python, Wireshark, Sysinternals) từ bên trong môi trường máy ảo do giới hạn kết nối hoặc cấu hình mạng.
- Cách khắc phục:Tải các bộ cài đặt và công cụ cần thiết trực tiếp trên máy thật (host machine), sau đó truyền/chép (pass) các file cài đặt vào máy ảo để tiến hành cài đặt và sử dụng cục bộ