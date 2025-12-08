---
title: "Event 2"
date: "2025-11-15"
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “AWS Cloud Mastery Series #1”

### Mục Đích Của Sự Kiện

*   Cung cấp kiến thức thực tế về AWS Bedrock và phát triển AI hiện đại
*   Giới thiệu khái niệm mô hình nền tảng và phương pháp kỹ thuật prompt hiệu quả
*   Minh họa quy trình làm việc RAG và tìm kiếm dựa trên embedding
*   Trình bày các dịch vụ AI của AWS thường được sử dụng trong ứng dụng thực tế
*   Giải thích kiến trúc hệ thống AgentCore và GenAI sẵn sàng cho sản xuất

### Danh Sách Diễn Giả

*   **Lâm Tuấn Kiệt** – Kỹ sư DevOps cao cấp, FPT Software
*   **Đặng Hoàng Hiếu Nghi** – Kỹ sư AI, Reonova Cloud
*   **Đinh Lê Hoàng Anh** – Thực tập sinh Kỹ sư Đám mây, FCJ
*   **Khá** – Chia sẻ lời khuyên về xây dựng dự án hướng sản phẩm cho CV
*   **Đại diện FPT** – Nói về việc các công ty sử dụng AI trên đám mây để tối ưu hóa và tiết kiệm chi phí

### Nội Dung Nổi Bật

#### Mô Hình Nền Tảng & Xu Hướng Ngành

*   Các mô hình ML truyền thống xử lý *một tác vụ* và yêu cầu dữ liệu được gán nhãn.
*   Mô hình nền tảng trong GenAI được đào tạo trên tập dữ liệu không nhãn khổng lồ, cho phép thực hiện đa tác vụ linh hoạt.
*   Bedrock hiện tích hợp các mô hình như **OpenAI** và **DeepSeek**.
*   Các công ty ngày càng xây dựng sản phẩm AI trên nền tảng đám mây để giảm chi phí vận hành.

#### Góc Nhìn Từ Lâm Tuấn Kiệt

*   Giải thích sự phát triển từ ML truyền thống → mô hình nền tảng.
*   Nhấn mạnh tầm quan trọng của kỹ thuật prompt để có đầu ra chất lượng cao.
*   Chứng minh cách Bedrock đơn giản hóa việc truy cập các mô hình tiên tiến mà không cần DevOps phức tạp.
*   Nhấn mạnh rằng việc xây dựng sản phẩm AI đòi hỏi kỹ năng, lặp lại và triển khai có trách nhiệm.

#### Kỹ Thuật Prompt

*   **Prompt zero-shot** – Ngữ cảnh tối thiểu; kết quả có thể đơn giản hoặc mơ hồ.
*   **Prompt few-shot** – Cung cấp các ví dụ trong prompt để nhận phản hồi rõ ràng hơn.
*   **Prompt chain-of-thought** – Hướng dẫn mô hình với các bước lập luận để cải thiện độ chính xác và chi tiết.

#### Hệ Thống Sinh Tăng Cường Truy Xuất (RAG)

*   Hệ thống truy xuất thông tin liên quan từ nguồn dữ liệu.
*   Tự động kết hợp prompt của người dùng với ngữ cảnh được truy xuất.
*   Tạo ra phản hồi chính xác và phù hợp hơn.

#### Embeddings

*   Văn bản được chuyển đổi thành vector biểu thị ý nghĩa.
*   Các ý nghĩa tương tự được nhóm lại với nhau trong không gian vector.
*   **AWS Titan Text Embeddings** hỗ trợ hơn 100 ngôn ngữ.

#### Các Dịch Vụ AI Của AWS

*   **Rekognition** – Phát hiện đối tượng trong hình ảnh/video
*   **Translate** – Dịch tự động
*   **Textract** – Trích xuất văn bản và cấu trúc bố cục
*   **Transcribe** – Chuyển giọng nói thành văn bản với nhận diện người nói
*   **Polly** – Chuyển văn bản thành giọng nói
*   **Comprehend** – NLP, trích xuất thực thể, hiểu mối quan hệ
*   **Kendra** – Tìm kiếm tài liệu thông minh
*   **Lookout Family** – Phát hiện bất thường cho số liệu, thiết bị và thị giác máy tính
*   **Personalize** – Hệ thống đề xuất
*   **Pipecat** – Khung công tác đường ống tác nhân AI

Các nhà phát triển có thể sử dụng trực tiếp các dịch vụ này qua API.

#### Amazon Bedrock AgentCore

*   Cho phép xây dựng ứng dụng AI mà không cần quản lý hạ tầng và DevOps nặng nề.
*   Hỗ trợ các khung công tác hiện đại như **LangGraph** và **LangChain**.
*   Được thiết kế để giúp các nhóm chuyển từ nguyên mẫu → sản xuất hiệu quả.

**Cơ Chế Chính**

*   Thời gian chạy
*   Bộ nhớ
*   Danh tính
*   Cổng kết nối
*   Trình thông dịch mã
*   Công cụ duyệt web
*   Khả năng quan sát

### Những Gì Học Được

#### Tư Duy Phát Triển AI

*   Việc tạo ra sản phẩm thực tế có giá trị hơn việc chỉ đáp ứng yêu cầu học thuật.
*   Mô hình nền tảng cho phép thử nghiệm và triển khai nhanh chóng.
*   Kỹ thuật prompt ảnh hưởng đáng kể đến chất lượng đầu ra.

#### Tác Động Kỹ Thuật

*   RAG nâng cao độ chính xác bằng cách căn cứ phản hồi vào dữ liệu thực.
*   Embeddings cải thiện tìm kiếm ngữ nghĩa và truy xuất thông tin.
*   Các dịch vụ AI của AWS bao quát quy trình làm việc từ đầu đến cuối — từ giọng nói, thị giác đến NLP.

#### Tính Ứng Dụng Thực Tế

*   Các công ty ngày càng áp dụng AI dựa trên đám mây để giảm chi phí và đẩy nhanh phát triển sản phẩm.
*   Kỹ năng về kỹ thuật prompt, embeddings và dịch vụ Bedrock đang trở nên thiết yếu.

### Trải Nghiệm Trong Event

Tham dự **AWS Cloud Mastery Series #1** mang lại hiểu biết thực tế về cách các hệ thống AI hiện đại hoạt động trên AWS.

#### 1. Học Hỏi Trực Tiếp Từ Kỹ Sư

*   Các diễn giả chia sẻ kinh nghiệm làm việc thực tế từ các vai trò DevOps, AI và kỹ sư đám mây.

#### 2. Kiến Thức Kỹ Thuật Thực Hành

*   Ví dụ về kỹ thuật prompt
*   Minh họa về RAG
*   Các trường hợp sử dụng cho từng dịch vụ AI của AWS

#### 3. Xây Dựng Cho Tương Lai

*   Được khuyến khích xây dựng sản phẩm thực
*   Kỹ năng Đám mây + AI đang trở thành yêu cầu cốt lõi
*   Tập trung mạnh vào triển khai thực tế thay vì lý thuyết

### Một Số Hình Ảnh Khi Tham Gia Sự Kiện

![Ảnh sự kiện](/images/event-5.jpg)

![Ảnh sự kiện](/images/event-6.jpg)

![Ảnh sự kiện](/images/event-7.jpg)

![Ảnh sự kiện](/images/event-8.jpg)
