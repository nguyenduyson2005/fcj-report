---
title: "Worklog Tuần 2"
date: "2025-09-15"
weight: 2
chapter: false
pre: " <b> 1.2. </b>"
---


### Mục tiêu tuần 2:

* Thành thạo việc triển khai và quản lý máy chủ EC2
* Triển khai mạng AWS và kết nối VPN

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Học cách triển khai máy chủ Amazon EC2 <br>&emsp; + Tạo máy chủ EC2 <br>&emsp; + Kết nối vào máy chủ EC2  <br>&emsp; + Tạo NAT Gateway     <br>&emsp;   + Sử dụng Reachability Analyzer               <br>&emsp;  + Tạo EC2 Instance Connect Endpoint <br>&emsp;  + Truy cập Secure Shell với AWS Systems Manager Session Manager <br>&emsp;     +   Triển khai Giám sát CloudWatch và cảnh báo cho tài nguyên VPC                                                       | 15/09/2025 | 15/09/2025      | <https://000003.awsstudygroup.com/> |
| 3   | - Thiết lập Kết nối VPN Site-to-Site trên AWS <br>&emsp; + Tạo môi trường VPN (VPC cho VPN) <br>&emsp; + Tạo máy chủ EC2 đóng vai trò Customer Gateway <br>&emsp; + Tạo Virtual Private Gateway <br>&emsp; + Tạo Customer Gateway | 16/09/2025 | 16/09/2025      | <https://000003.awsstudygroup.com/> |
| 4   | - Cấu hình Kết nối VPN <br>&emsp; + Tạo Kết nối VPN <br>&emsp; + Thực hiện Cấu hình Customer Gateway <br>&emsp; + Chỉnh sửa cài đặt AWS VPN Tunnel <br>&emsp; + Xem lại các Cấu hình VPN Thay thế | 17/09/2025 | 17/09/2025      | <https://000003.awsstudygroup.com/> |
| 5   | - Tham gia sự kiện Vietnam Cloud Day 2025 : Ho Chi Minh City Connect Edition for Builders | 18/09/2025 | 18/09/2025      |                                           |
| 6   | - Xử lý Sự cố VPN & Cấu hình Nâng cao <br>&emsp; + Làm theo Hướng dẫn Xử lý sự cố VPN <br>&emsp; + Xem lại Hướng dẫn Xử lý sự cố VPN chính thức của AWS <br>&emsp; + Kết nối VPN sử dụng Strongswan với Transit Gateway | 19/09/2025 | 19/09/2025      | <https://000003.awsstudygroup.com/> |

### Kết quả đạt được tuần 2:

* Triển khai và quản lý thành công máy chủ EC2:
  * Đã tạo và khởi chạy máy chủ EC2 sử dụng AWS Management Console.
  * Kết nối vào máy chủ thông qua EC2 Instance Connect và Systems Manager Session Manager.
  * Cấu hình NAT Gateway để cho phép subnet private truy cập internet.
  * Sử dụng Reachability Analyzer để xác minh kết nối mạng.
  * Triển khai giám sát CloudWatch và cảnh báo cho tài nguyên VPC và EC2.

* Thiết lập và cấu hình kết nối VPN Site-to-Site:
  * Tạo môi trường VPN bao gồm VPC chuyên dụng cho cấu hình VPN.
  * Triển khai máy chủ EC2 đóng vai trò Customer Gateway.
  * Tạo và gắn Virtual Private Gateway.
  * Cấu hình kết nối VPN giữa AWS và Customer Gateway.
  * Chỉnh sửa cài đặt VPN tunnel và xem xét các cấu hình VPN thay thế.

* Thực hiện xử lý sự cố và cấu hình nâng cao VPN:
  * Làm theo hướng dẫn xử lý sự cố VPN của AWS để xác định và giải quyết các vấn đề kết nối phổ biến.
  * Kiểm tra kết nối VPN sử dụng Strongswan tích hợp với AWS Transit Gateway.
  * Xác minh giao tiếp an toàn giữa tài nguyên on-premises và VPC trên AWS.

* Nâng cao hiểu biết về các thành phần mạng AWS và quản lý kết nối,
  bao gồm mạng EC2, NAT Gateway, VPN và các công cụ giám sát.


