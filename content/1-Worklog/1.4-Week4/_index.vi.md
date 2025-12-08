---
title: "Worklog Tuần 4"
date: "2025-09-29"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---



### Mục tiêu tuần 4:

* Thành thạo sử dụng vai trò IAM để ủy quyền cho ứng dụng
* Học về môi trường phát triển AWS Cloud9
* Triển khai website tĩnh trên S3 với CloudFront

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Học cách cấp quyền ủy quyền cho ứng dụng truy cập dịch vụ AWS với vai trò IAM <br> - Chuẩn bị <br>&emsp; + Tạo instance EC2 <br>&emsp; + Tạo bucket S3 <br> - Tạo người dùng IAM với access keys để ứng dụng Python upload lên S3 <br> - Tạo vai trò IAM với quyền cho ứng dụng upload files lên bucket S3                                                                                              | 09/29/2025 | 09/29/2025 | <https://000048.awsstudygroup.com/> |
| 3 | - Tạo Instance Cloud9 <br> - Học các tính năng cơ bản của Cloud9: <br>&emsp; + Sử dụng command line <br>&emsp; + Làm việc với text files <br>&emsp; + Quay lại giao diện Dashboard <br> - Sử dụng AWS CLI trong Cloud9 | 09/30/2025 | 09/30/2025 | <https://000049.awsstudygroup.com/> |
| 4   | - Tìm hiểu thông tin về Amazon S3 <br>&emsp; + Hiểu sự khác biệt giữa S3 Buckets và Object <br>&emsp;  + Tính năng chính (storage classes, security and compliance, management and analytics, performance and availability)  <br>&emsp; + Các trường hợp sử dụng phổ biến <br>  - Tạo bucket S3 và upload dữ liệu để chuẩn bị host website tĩnh <br> - Cấu hình website tĩnh: <br>&emsp; + Bật tính năng website tĩnh <br>&emsp; + Cấu hình public access block <br>&emsp; + Cấu hình public objects <br>&emsp; + Kiểm tra website <br> - Tăng tốc với CloudFront: <br>&emsp; + Block all public access <br>&emsp; + Cấu hình Amazon CloudFront <br>&emsp; + Kiểm tra Amazon CloudFront <br> - Tính năng S3 nâng cao: <br>&emsp; + Cấu hình bucket versioning <br>&emsp; + Di chuyển objects giữa các buckets <br>&emsp; + Thiết lập cross-region replication | 10/01/2025 | 10/04/2025      | <https://000057.awsstudygroup.com/> |
| 5   | - Tham gia sự kiện [AWS GenAI Builder Club] AI-Driven Development Life Cycle: Reimagining Software Engineering                                                                                              | 10/03/2025 | 10/03/2025 | |


### Kết quả đạt được tuần 4:

* Thành thạo cấu hình vai trò IAM để ủy quyền cho ứng dụng:
  * Tạo người dùng IAM với access keys để upload lên S3
  * Cấu hình vai trò IAM với quyền truy cập S3
  * Thiết lập instance EC2 và bucket S3 để kiểm tra ứng dụng

* Thành thạo sử dụng môi trường phát triển AWS Cloud9:
  * Tạo và quản lý instance Cloud9
  * Sử dụng command line interface và tính năng chỉnh sửa text
  * Thực thi các lệnh AWS CLI trong Cloud9

* Triển khai thành công hosting website tĩnh trên S3:
  * Cấu hình bucket S3 để host website tĩnh
  * Quản lý public access blocks và quyền truy cập objects
  * Kiểm tra chức năng và hiệu suất website

* Triển khai CloudFront để tăng tốc phân phối nội dung:
  * Cấu hình CloudFront distributions cho website S3
  * Triển khai các biện pháp bảo mật bằng cách block public access
  * Kiểm tra hiệu suất và caching của CloudFront

* Áp dụng các tính năng S3 nâng cao:
  * Bật bucket versioning để bảo vệ dữ liệu
  * Quản lý di chuyển objects giữa các buckets
  * Thiết lập cross-region replication cho disaster recovery


