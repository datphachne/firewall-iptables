#Lab: Xây dựng chính sách an toàn Firewall bằng Iptables trên Linux
Đề tài thực nghiệm xây dựng hệ thống tường lửa (Firewall) sử dụng Iptables trên hệ điều hành Linux để bảo vệ mô hình mạng Cơ sở 1 cho Học viện Kỹ thuật Mật mã.
---

## Tổng quan
Hệ thống áp dụng nguyên tắc an toàn **"Deny All – Permit by Exception"** (Chặn tất cả - Chỉ mở những gì được cấp phép) để kiểm soát dữ liệu giữa 3 vùng mạng: **LAN nội bộ, DMZ và Internet**.
---

###Các chính sách được triển khai
Lab đã thực nghiệm thành công các chính sách sau:
1. *Cấm tất cả truy cập trái phép:** Mặc định chặn mọi kết nối không hợp lệ vào/ra hệ thống.
2. *Cho phép dịch vụ Web:** Mở cổng HTTP (80) và HTTPS (443) cho người dùng truy cập WebServer trong DMZ.
3. *Kiểm soát dịch vụ Email:** Ép luồng thư gửi nhận qua MailServer qua SMTP (25) và POP3 (110).
4. *Duyệt web an toàn qua Proxy:** Máy trạm LAN bắt buộc đi Internet qua Proxy Server (Cổng 8080).
---
