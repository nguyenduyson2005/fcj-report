---
title: "Worklog Tuần 9"
date: "2025-11-03"
weight: 9
chapter: false
pre: " <b> 1.9. </b>"
---



### Mục tiêu tuần 9:

* Thành thạo sử dụng Amazon ElastiCache cho lưu trữ dữ liệu trong bộ nhớ
* Triển khai các giải pháp mạng và kết nối AWS nâng cao
* Phát triển kỹ năng cấu hình VPC và DNS toàn diện

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Chuẩn bị & Tạo Cluster ElastiCache: <br>&emsp; + Tạo AWS Access Key để truy cập theo chương trình <br>&emsp; + Cài đặt và cấu hình AWS CLI <br>&emsp; + Tạo subnet groups sử dụng Console và CLI <br>&emsp; + Tạo cluster ElastiCache (cluster mode disabled) <br>&emsp; + Tạo cluster ElastiCache (cluster mode enabled) <br>&emsp; + Cấu hình quyền truy cập cluster | 11/03/2025 | 11/03/2025 | <https://000061.awsstudygroup.com/> |
| 3   | - Kết nối & Thao tác Dữ liệu ElastiCache: <br>&emsp; + Kết nối đến cluster nodes (cả hai cluster modes) <br>&emsp; + Kiểm tra endpoints sử dụng AWS CLI <br>&emsp; + Kiểm tra chức năng user group <br>&emsp; + Thực hiện các thao tác string cơ bản (Set và Get) <br>&emsp; + Làm việc với cấu trúc dữ liệu hash (nhiều items) | 11/04/2025 | 11/04/2025 | <https://000061.awsstudygroup.com/> |
| 4   | - Mạng VPC Nâng cao: <br>&emsp; + Triển khai các thành phần cơ sở hạ tầng VPC <br>&emsp; + Xem lại Cisco CSR agreement để thiết lập VPN <br>&emsp; + Tìm hiểu sâu kiến trúc các thành phần VPC <br>&emsp; + Triển khai Transit Gateway <br>&emsp; + Truy cập Cisco CSR Router sử dụng Cloud9 | 11/05/2025 | 11/05/2025 | <https://000092.awsstudygroup.com/> |
| 5   | - VPN, Endpoints & Peering: <br>&emsp; + Thiết lập kết nối VPN site-to-site <br>&emsp; + Cấu hình các đường dẫn ECMP bổ sung để dự phòng <br>&emsp; + Triển khai VPC Endpoints cho AWS Services <br>&emsp; + Thực hiện kiểm tra endpoint NP2 <br>&emsp; + Tạo yêu cầu VPC peering <br>&emsp; + Cấu hình peering routing tables | 11/06/2025 | 11/06/2025 | <https://000092.awsstudygroup.com/> |
| 6   | - DNS & Quản lý Mạng: <br>&emsp; + Triển khai Route53 DNS endpoints và internal hosted zones <br>&emsp; + Thực hiện kiểm tra DNS toàn diện <br>&emsp; + Triển khai VPC Endpoint Services <br>&emsp; + Thiết lập Transit Gateway Network Manager <br>&emsp; + Cấu hình network sites và topology <br>&emsp; + Sử dụng Network Insights để giám sát <br>&emsp; + Kiểm tra cuối cùng kết nối VPC peering | 11/07/2025 | 11/07/2025 | <https://000092.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

* Thành thạo sử dụng kho dữ liệu trong bộ nhớ Amazon ElastiCache:
  * Tạo và cấu hình Redis clusters trong cả hai cluster modes
  * Thiết lập quyền truy cập bảo mật và user groups
  * Thực hiện các thao tác dữ liệu bao gồm strings, hashes và key-value pairs
  * Kết nối đến cluster nodes và kiểm tra endpoints qua AWS CLI

* Triển khai các giải pháp mạng AWS toàn diện:
  * Triển khai cơ sở hạ tầng VPC nâng cao với nhiều thành phần
  * Cấu hình Transit Gateway để quản lý mạng tập trung
  * Thiết lập kết nối VPN site-to-site với Cisco CSR routers
  * Thiết lập các đường dẫn ECMP để dự phòng mạng và cân bằng tải

* Phát triển chuyên môn về các dịch vụ kết nối AWS:
  * Triển khai VPC Endpoints để truy cập dịch vụ AWS riêng tư
  * Tạo kết nối VPC peering và cấu hình routing tables
  * Triển khai Route53 DNS endpoints và internal hosted zones
  * Thực hiện kiểm tra và xác thực mạng toàn diện

* Quản lý và giám sát mạng nâng cao:
  * Cấu hình Transit Gateway Network Manager để hiển thị mạng toàn cầu
  * Thiết lập network sites và ánh xạ topology
  * Sử dụng Network Insights để giám sát hiệu suất và xử lý sự cố
  * Truy cập thiết bị mạng sử dụng Cloud9 để quản lý từ xa

* Nâng cao kỹ năng tích hợp đa dịch vụ:
  * Kết nối ElastiCache với các mẫu dữ liệu ứng dụng
  * Tích hợp mạng VPC với DNS và dịch vụ endpoint
  * Kết hợp Transit Gateway với VPN và giải pháp peering
  * Triển khai các kiến trúc kết nối mạng end-to-end


