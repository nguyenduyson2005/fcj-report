---
title: "Worklog Tuần 10"
date: "2025-11-10"
weight: 10
chapter: false
pre: " <b> 1.10 </b>"
---


### Mục tiêu tuần 10:

* Thành thạo sử dụng Amazon CloudFront để phân phối nội dung và edge computing
* Triển khai cấu hình CDN nâng cao với Lambda@Edge
* Triển khai và quản lý desktop ảo với Amazon WorkSpaces
* Tham gia sự kiện AWS Cloud Mastery Series #1

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Phân phối Nội dung với Amazon CloudFront: <br>&emsp; + Tạo và cấu hình S3 bucket để host tĩnh <br>&emsp; + Upload file `index.html` ví dụ <br>&emsp; + Cấu hình Amazon CloudFront distribution với S3 bucket origin <br>&emsp; + Xác thực truy cập distribution qua CloudFront URL <br>&emsp; + Thực hiện teardown và dọn dẹp tài nguyên | 11/10/2025 | 11/10/2025 | <https://000094.awsstudygroup.com/> |
| 3   | - Edge Computing với CloudFront và Lambda@Edge: <br>&emsp; + Tạo EC2 instance để host ứng dụng <br>&emsp; + Tạo S3 bucket để lưu trữ nội dung tĩnh <br>&emsp; + Cấu hình CloudFront distribution với EC2 origin <br>&emsp; + Kiểm tra phân phối ứng dụng qua CloudFront <br>&emsp; + Kiểm tra distribution invalidations <br>&emsp; + Cấu hình custom error pages | 11/11/2025 | 11/11/2025 | <https://000130.awsstudygroup.com/> |
| 4   | - Cấu hình CloudFront Nâng cao: <br>&emsp; + Tạo origin groups cho các kịch bản failover <br>&emsp; + Cấu hình response headers policies <br>&emsp; + Tạo custom cache behaviors <br>&emsp; + Tạo Lambda@Edge functions <br>&emsp; + Deploy Lambda@Edge đến CloudFront distribution <br>&emsp; + Cấu hình metrics và access logs <br>&emsp; + Thực hiện dọn dẹp và teardown tài nguyên | 11/12/2025 | 11/13/2025 | <https://000130.awsstudygroup.com/> |
| 5   | - Windows Workloads trên AWS: <br>&emsp; + Chuẩn bị môi trường triển khai cho Amazon WorkSpaces <br>&emsp; + Triển khai và cấu hình Amazon WorkSpaces <br>&emsp; + Truy cập WorkSpaces qua web browser <br>&emsp; + Truy cập WorkSpaces sử dụng WorkSpaces client application <br>&emsp; + Thực hiện dọn dẹp dịch vụ và kết thúc tài nguyên | 11/14/2025 | 11/14/2025 | <https://000093.awsstudygroup.com/> |
| 6   | - Tham gia sự kiện AWS Cloud Mastery Series #1 | 11/15/2025 | 11/15/2025 | |


### Kết quả đạt được tuần 10:

* Thiết lập chuyên môn CloudFront toàn diện:
  * Tạo và cấu hình S3 buckets để host nội dung tĩnh
  * Upload và quản lý file website tĩnh (index.html)
  * Cấu hình CloudFront distributions với S3 bucket origins
  * Triển khai EC2 instances để host ứng dụng
  * Thiết lập CloudFront distributions với EC2 origins
  * Kiểm tra phân phối ứng dụng qua CDN CloudFront

* Nâng cao khả năng edge computing:
  * Triển khai cấu hình custom error pages
  * Kiểm tra distribution invalidations để quản lý cache
  * Tạo origin groups cho các kịch bản failover
  * Cấu hình response headers policies
  * Tạo custom cache behaviors
  * Phát triển và triển khai Lambda@Edge functions

* Thành thạo sử dụng cơ sở hạ tầng desktop ảo:
  * Chuẩn bị môi trường triển khai cho Amazon WorkSpaces
  * Triển khai và cấu hình Amazon WorkSpaces
  * Truy cập WorkSpaces qua giao diện web browser
  * Truy cập WorkSpaces sử dụng native client application
  * Thực hiện dọn dẹp dịch vụ và kết thúc tài nguyên

* Nâng cao kỹ năng giám sát và tối ưu hóa:
  * Cấu hình CloudFront metrics và access logs
  * Thực hiện dọn dẹp và teardown tài nguyên toàn diện
  * Xác thực truy cập distribution qua CloudFront URLs