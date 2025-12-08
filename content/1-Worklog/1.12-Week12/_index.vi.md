---
title: "Worklog Tuần 12"
date: "2025-11-24"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Mục tiêu tuần 12:

* Thành thạo kỹ thuật di chuyển VM sử dụng AWS VM Import/Export
* Triển khai di chuyển database với AWS Database Migration Service (DMS)
* Sử dụng Schema Conversion Tool (SCT) để chuyển đổi schema database
* Tham gia sự kiện AWS Cloud Mastery Series #3
* Hỗ trợ hợp tác nhóm qua dịch tài liệu workshop

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Di chuyển VM với AWS VM Import/Export <br>&emsp; + Chuẩn bị môi trường VMWare Workstation <br>&emsp; + Export virtual machine từ cơ sở hạ tầng on-premises <br>&emsp; + Upload file virtual machine lên AWS S3 <br>&emsp; + Import virtual machine vào đám mây AWS <br>&emsp; + Triển khai EC2 instances từ AMI đã import | 11/24/2025 | 11/24/2025 | <https://000014.awsstudygroup.com/> |
| 3   | - Di chuyển VM với AWS VM Import/Export <br>&emsp; + Cấu hình S3 bucket ACL để export VM <br>&emsp; + Export virtual machine từ EC2 instance đang chạy <br>&emsp; + Export virtual machine từ AMI hiện có <br>&emsp; + Tham khảo video hướng dẫn di chuyển <br>&emsp; + Thực hiện dọn dẹp tài nguyên trên đám mây AWS | 11/25/2025 | 11/25/2025 | <https://000014.awsstudygroup.com/> |
| 4   | - Di chuyển Database với AWS Database Migration Service (DMS) và Schema Conversion Tool (SCT): <br>&emsp; + Bắt đầu với cấu hình AWS DMS <br>&emsp; + Chọn và cấu hình source database cho DMS <br>&emsp; + Chọn và cấu hình target database cho DMS <br>&emsp; + Triển khai serverless replication setup <br>&emsp; + Giám sát tiến trình và hiệu suất di chuyển DMS <br>&emsp; + Xử lý sự cố di chuyển với AWS DMS <br>&emsp; + Thực hiện dọn dẹp môi trường và kết thúc tài nguyên | 11/26/2025 | 11/26/2025 | <https://000043.awsstudygroup.com/> |
| 5   | - Tạo phiên bản tiếng Việt của các file workshop tiếng Anh của nhóm | 11/27/2025 | 11/28/2025      | |
| 6   | - Tham gia sự kiện AWS Cloud Mastery Series #3 | 11/29/2025 | 11/29/2025      | |


### Kết quả đạt được tuần 12:

* Thành thạo quy trình di chuyển virtual machine:
  * Chuẩn bị môi trường VMWare Workstation cho di chuyển
  * Export virtual machines từ cơ sở hạ tầng on-premises
  * Upload file VM lên AWS S3 storage
  * Import virtual machines vào môi trường đám mây AWS
  * Triển khai EC2 instances từ AMI images đã import
  * Cấu hình S3 bucket ACLs cho hoạt động export VM
  * Export virtual machines từ EC2 instances đang chạy
  * Export virtual machines từ các AMIs hiện có

* Triển khai giải pháp di chuyển cơ sở dữ liệu  toàn diện:
  * Cấu hình AWS Database Migration Service (DMS)
  * Chọn và cấu hình source databases cho di chuyển
  * Chọn và cấu hình target databases cho di chuyển
  * Triển khai serverless replication setups
  * Giám sát tiến trình và hiệu suất di chuyển DMS
  * Xử lý sự cố di chuyển sử dụng công cụ AWS DMS
  * Quản lý vòng đời di chuyển cơ sở dữ liệu  từ thiết lập đến dọn dẹp

* Chuyên môn di chuyển đám mây nâng cao:
  * Thiết lập khả năng di chuyển VM end-to-end
  * Xây dựng thành thạo di chuyển cơ sở dữ liệu xuyên suốt các nền tảng
  * Triển khai chiến lược quản lý tài nguyên toàn diện
  * Phát triển kỹ năng xử lý sự cố cho thách thức di chuyển


