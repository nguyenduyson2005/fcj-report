---
title: "Blog 2"
date: "2025-10-10"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# DeepSeek-V3.1 Model Đã Có Mặt Trong Amazon Bedrock

**bởi Channy Yun (윤석찬) | ngày 18 tháng 9 năm 2025 | Amazon Bedrock, Amazon Machine Learning, Announcements, Artificial Intelligence, Featured, Launch, News, Open Source, Serverless**

[▶️ Nghe bản audio](/images/voice-deepseekv3.mp3)
Lồng tiếng bởi Amazon Polly

Vào tháng 3, Amazon Web Services (AWS) đã trở thành nhà cung cấp dịch vụ đám mây đầu tiên triển khai DeepSeek-R1 theo cách không máy chủ bằng cách ra mắt nó dưới dạng một mô hình được quản lý hoàn toàn và có sẵn rộng rãi trong  Amazon Bedrock. Kể từ đó, khách hàng đã sử dụng khả năng của DeepSeek-R1 thông qua Amazon Bedrock để xây dựng các ứng dụng generative AI, hưởng lợi từ các biện pháp bảo vệ mạnh mẽ và công cụ toàn diện của Bedrock để triển khai AI an toàn.

Hôm nay, tôi rất vui được thông báo rằng DeepSeek-V3.1 hiện đã có mặt như một mô hình nền tảng được quản lý hoàn toàn trong Amazon Bedrock. DeepSeek-V3.1 là một mô hình hybrid open weight chuyển đổi giữa chế độ suy nghĩ (chain-of-thought reasoning) để phân tích từng bước chi tiết và chế độ không suy nghĩ (direct answers) để có phản hồi nhanh hơn.

Theo DeepSeek, chế độ suy nghĩ của DeepSeek-V3.1 đạt được chất lượng câu trả lời tương đương với kết quả tốt hơn, khả năng lập luận đa bước mạnh mẽ hơn cho các tác vụ tìm kiếm phức tạp và cải thiện lớn về hiệu quả suy nghĩ so với DeepSeek-R1-0528.

| Benchmarks | DeepSeek-V3.1 | DeepSeek-R1-0528 |
|------------|---------------|------------------|
| Browsecomp | 30.0 | 8.9 |
| Browsecomp_zh | 49.2 | 35.7 |
| HLE | 29.8 | 24.8 |
| xbench-DeepSearch | 71.2 | 55.0 |
| Frames | 83.7 | 82.0 |
| SimpleQA | 93.4 | 92.3 |
| Seal0 | 42.6 | 29.7 |
| SWE-bench Verified | 66.0 | 44.6 |
| SWE-bench Multilingual | 54.5 | 30.5 |
| Terminal-Bench | 31.3 | 5.7 |

*(c) https://api-docs.deepseek.com/news/news250821*

Hiệu suất của model DeepSeek-V3.1 trong việc sử dụng công cụ và các tác vụ tác nhân đã được cải thiện đáng kể thông qua tối ưu hóa sau đào tạo so với các model DeepSeek trước đây. DeepSeek-V3.1 cũng hỗ trợ hơn 100 ngôn ngữ với trình độ gần như bản địa, bao gồm cải thiện đáng kể trong các ngôn ngữ ít tài nguyên thiếu các kho ngữ liệu đơn ngữ hoặc song ngữ lớn. Bạn có thể xây dựng các ứng dụng toàn cầu để mang lại độ chính xác cao hơn và giảm ảo giác so với các model DeepSeek trước đó, đồng thời duy trì khả năng quan sát quá trình ra quyết định của nó.

Đây là các công dụng chính khi sử dụng model này:

- **Tạo mã** – DeepSeek-V3.1 xuất sắc trong các tác vụ mã hóa với những cải tiến trong benchmark của kỹ thuật phần mềm và khả năng của tác nhân, làm cho nó lý tưởng cho việc tạo mã tự động, gỡ lỗi và quy trình kỹ thuật phần mềm. Nó hoạt động tốt trên các benchmark về lập trình trong khi mang lại kết quả chất lượng cao một cách hiệu quả.
- **Công cụ AI agent** – Mô hình này có tính năng gọi công cụ được cải thiện thông qua tối ưu hậu huấn luyện, giúp nó thể hiện ưu thế trong việc sử dụng công cụ và quy trình làm việc tác nhân. Nó hỗ trợ gọi công cụ có cấu trúc, tác nhân mã và tác nhân tìm kiếm, đưa nó thành một lựa chọn vững chắc để xây dựng các hệ thống AI tự trị.
- **Ứng dụng doanh nghiệp** – Các model DeepSeek được tích hợp vào nhiều nền tảng trò chuyện và công cụ năng suất, nâng cao tương tác người dùng và hỗ trợ quy trình của dịch vụ chăm sóc khách hàng. Nhờ khả năng đa ngôn ngữ và nhạy cảm văn hóa, mô hình phù hợp cho các ứng dụng doanh nghiệp toàn cầu.

Như tôi đã đề cập trong bài viết trước, khi triển khai các mô hình có sẵn công khai, hãy cân nhắc cẩn thận các yêu cầu về quyền riêng tư dữ liệu khi triển khai trong môi trường sản xuất của bạn, kiểm tra sự thiên vị trong đầu ra và giám sát kết quả của bạn về bảo mật dữ liệu, AI có trách nhiệm và đánh giá mô hình.

Bạn có thể truy cập các tính năng bảo mật cấp doanh nghiệp của Amazon Bedrock và triển khai các biện pháp bảo vệ được tùy chỉnh theo yêu cầu ứng dụng cũng như chính sách AI có trách nhiệm của bạn bằng Amazon Bedrock Guardrails. Bạn cũng có thể đánh giá và so sánh các mô hình để xác định mô hình tối ưu cho các trường hợp sử dụng của mình bằng cách sử dụng  các công cụ đánh giá mô hình Amazon Bedrock.

### Bắt đầu với mô hình DeepSeek-V3.1 trong Amazon Bedrock

Để thử nghiệm mô hình DeepSeek-V3.1 trong bảng điều khiển Amazon Bedrock, chọn **Chat/Text** trong mục **Playgrounds** ở thanh menu bên trái. Sau đó chọn **Select model** ở góc trên bên trái, chọn **DeepSeek** làm danh mục và **DeepSeek-V3.1** làm mô hình. Cuối cùng bấm **Apply**.

![Image](/images/2025-deepseek-v3.1-2-select-model-2.jpg)

Sử dụng mô hình DeepSeek-V3.1 đã chọn, tôi chạy ví dụ prompt sau về quyết định kiến trúc kỹ thuật:

> Phác thảo kiến trúc tổng thể cho một dịch vụ rút gọn URL có khả năng mở rộng như bit.ly. Thảo luận các thành phần chính như thiết kế API, lựa chọn cơ sở dữ liệu (SQL vs. NoSQL), cơ chế chuyển hướng hoạt động ra sao, và cách bạn sẽ tạo các mã rút gọn duy nhất.

Bạn có thể bật/tắt chế độ **Model Reasoning** để sinh chuỗi suy luận trước khi đưa ra kết luận cuối cùng.

![Image](/images/2025-deepseek-v3.1-3-chat-example.jpg)

Bạn cũng có thể truy cập mô hình qua AWS Command Line Interface (AWS CLI) và AWS SDK. Mô hình hỗ trợ cả InvokeModel và Converse API. Có nhiều ví dụ mã nguồn cho nhiều trường hợp sử dụng và ngôn ngữ lập trình khác nhau.

Để tìm hiểu thêm, xem [DeepSeek model inference parameters and responses](https://docs.aws.amazon.com/bedrock/latest/useguide/model-parameters-deepseek.html) trong tài liệu AWS.

### Hiện đã có

DeepSeek-V3.1 hiện đã có ở các vùng AWS: US West (Oregon), Asia Pacific (Tokyo), Asia Pacific (Mumbai), Europe (London) và Europe (Stockholm). Kiểm tra danh sách đầy đủ các vùng để cập nhật trong tương lai. Để biết thêm, xem trang sản phẩm [DeepSeek in Amazon Bedrock product page](https://aws.amazon.com/bedrock/features/deepseek/) và trang giá cả [Amazon Bedrock pricing page](https://aws.amazon.com/bedrock/pricing/).

Hãy thử mô hình DeepSeek-V3.1 trong bảng điều khiển Amazon Bedrock hôm nay và gửi phản hồi lên [AWS re:Post for Amazon Bedrock](https://repost.aws/tags/TAxZAJ5PL9qHTYFdH8yKBPBw/amazon-bedrock) hoặc qua các kênh hỗ trợ AWS bạn thường dùng.

— Channy

**Cập nhật ngày 19 tháng 9 năm 2025** — Đã xóa phần truy cập mô hình. Amazon Bedrock sẽ đơn giản hóa truy cập tới tất cả các mô hình nền tảng không máy chủ và các mô hình mới bằng cách tự động bật quyền truy cập cho mọi tài khoản AWS, loại bỏ việc phải kích hoạt thủ công trong bảng điều khiển Bedrock. Trang truy cập mô hình sẽ bị ngừng vào ngày 8 tháng 10 năm 2025. Quản trị viên tài khoản vẫn giữ toàn quyền kiểm soát truy cập mô hình thông qua chính sách AWS IAM và Chính Sách Kiểm Soát Dịch Vụ (SCPs)  để giới hạn truy cập khi cần.

---

![Profile Image](/images/channyun_400x400.jpg)

**Channy Yun (윤석찬)**

Channy là Lead Blogger của AWS News Blog và Principal Developer Advocate cho AWS Cloud. Là một người đam mê web mở và viết blog, anh yêu thích việc học hỏi và chia sẻ công nghệ dựa trên cộng đồng.