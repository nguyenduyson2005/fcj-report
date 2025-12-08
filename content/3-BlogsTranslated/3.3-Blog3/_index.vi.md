---
title: "Blog 3"
date: "2025-10-10"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# Các mô hình Qwen hiện đã có mặt trên Amazon Bedrock

**bởi Danilo Poccia vào 18 THG 9 2025 trong Amazon Bedrock, Amazon Machine Learning, Thông báo, Trí tuệ nhân tạo, Nổi bật, Ra mắt, Tin tức, Mã nguồn mở, Serverless**

[▶️ Nghe bản audio](/images/da4b9237bacccdf19c0760cab7aec4a8359010b0amazon_polly_99109.mp3) Lồng tiếng bởi Amazon Polly

Hôm nay, chúng tôi bổ sung các mô hình Qwen từ Alibaba vào Amazon Bedrock. Với việc ra mắt này, Amazon Bedrock tiếp tục mở rộng lựa chọn mô hình bằng cách bổ sung quyền truy cập vào các mô hình nền tảng (FMs) mã nguồn mở Qwen3 theo cách thức được quản lý hoàn toàn và không máy chủ. Bản phát hành này bao gồm bốn mô hình: Qwen3-Coder-480B-A35B-Instruct, Qwen3-Coder-30B-A3B-Instruct, Qwen3-235B-A22B-Instruct-2507 và Qwen3-32B (Dense). Cùng nhau, các mô hình này có cả kiến trúc hỗn hợp chuyên gia (MoE) và kiến trúc dày đặc, cung cấp các lựa chọn linh hoạt cho các yêu cầu ứng dụng khác nhau.

Amazon Bedrock cung cấp quyền truy cập vào các FM dẫn đầu ngành thông qua một API thống nhất mà không yêu cầu quản lý cơ sở hạ tầng. Bạn có thể truy cập các mô hình từ nhiều nhà cung cấp, tích hợp các mô hình vào ứng dụng của mình và mở rộng quy mô sử dụng dựa trên yêu cầu khối lượng công việc. Với Amazon Bedrock, dữ liệu khách hàng không bao giờ được sử dụng để đào tạo các mô hình cơ bản. Với sự bổ sung của các mô hình Qwen3, Amazon Bedrock mang đến nhiều lựa chọn hơn cho các trường hợp sử dụng như:

- **Tạo mã và phân tích kho lưu trữ** với khả năng hiểu ngữ cảnh mở rộng
- **Xây dựng quy trình làm việc dạng tác nhân** có khả năng phối hợp nhiều công cụ và API cho tự động hóa kinh doanh
- **Cân bằng chi phí và hiệu suất AI** bằng cách sử dụng các chế độ tư duy lai để suy luận thích ứng

### Các mô hình Qwen3 trong Amazon Bedrock

Bốn mô hình Qwen3 này hiện đã có mặt trên Amazon Bedrock, mỗi mô hình được tối ưu hóa cho các yêu cầu về hiệu suất và chi phí khác nhau:

- **Qwen3-Coder-480B-A35B-Instruct** – Đây là mô hình hỗn hợp chuyên gia (MoE) với 480B tham số tổng và 35B tham số hoạt động. Nó được tối ưu hóa cho các tác vụ viết mã và tác nhân, đạt kết quả mạnh mẽ trong các điểm chuẩn như mã hóa tác nhân, sử dụng trình duyệt và sử dụng công cụ. Những khả năng này làm cho nó phù hợp để phân tích mã ở quy mô kho lưu trữ và tự động hóa quy trình làm việc nhiều bước.
- **Qwen3-Coder-30B-A3B-Instruct** – Đây là mô hình MoE với 30B tham số tổng và 3B tham số hoạt động. Được tối ưu hóa đặc biệt cho các tác vụ viết mã và các tình huống tuân theo hướng dẫn, mô hình này thể hiện hiệu suất mạnh mẽ trong việc tạo mã, phân tích và gỡ lỗi trên nhiều ngôn ngữ lập trình.
- **Qwen3-235B-A22B-Instruct-2507** – Đây là mô hình MoE được điều chỉnh theo hướng dẫn với 235B tham số tổng và 22B tham số hoạt động. Nó mang lại hiệu suất cạnh tranh trên các tác vụ về mã hóa, toán học và suy luận chung, cân bằng giữa khả năng và hiệu quả.
- **Qwen3-32B (Dense)** – Đây là mô hình dày đặc với 32B tham số. Nó phù hợp với các môi trường thời gian thực hoặc bị hạn chế tài nguyên như thiết bị di động và các triển khai điện toán biên nơi hiệu suất ổn định là quan trọng.

### Các tính năng kiến trúc và chức năng trong Qwen3

Các mô hình Qwen3 giới thiệu một số tính năng kiến trúc và chức năng:

**Kiến trúc MoE so với kiến trúc dày đặc** – Các mô hình MoE như Qwen3-Coder-480B-A35B, Qwen3-Coder-30B-A3B-Instruct và Qwen3-235B-A22B-Instruct-2507 chỉ kích hoạt một phần tham số cho mỗi yêu cầu, cung cấp hiệu suất cao với suy luận hiệu quả. Mô hình dày đặc Qwen3-32B kích hoạt tất cả các tham số, mang lại hiệu suất ổn định và dễ dự đoán hơn.

**Khả năng tác nhân** – Các mô hình Qwen3 có thể xử lý lập luận nhiều bước và lập kế hoạch có cấu trúc trong một lần gọi mô hình. Chúng có thể tạo đầu ra để gọi các công cụ hoặc API bên ngoài khi được tích hợp vào một khuôn khổ tác nhân. Các mô hình cũng duy trì ngữ cảnh mở rộng trong các phiên làm việc dài. Ngoài ra, chúng hỗ trợ gọi công cụ để cho phép giao tiếp tiêu chuẩn hóa với môi trường bên ngoài.

**Chế độ tư duy lai** – Qwen3 giới thiệu một cách tiếp cận lai để giải quyết vấn đề, hỗ trợ hai chế độ: tư duy và không tư duy. Chế độ tư duy áp dụng lập luận từng bước trước khi đưa ra câu trả lời cuối cùng. Điều này lý tưởng cho các vấn đề phức tạp đòi hỏi suy nghĩ sâu hơn. Trong khi chế độ không tư duy cung cấp phản hồi nhanh và gần như tức thì cho các tác vụ ít phức tạp hơn, nơi tốc độ quan trọng hơn chiều sâu. Điều này giúp các nhà phát triển quản lý sự đánh đổi giữa hiệu suất và chi phí hiệu quả hơn.

**Xử lý ngữ cảnh dài** – Các mô hình Qwen3-Coder hỗ trợ cửa sổ ngữ cảnh mở rộng, lên đến 256K token một cách tự nhiên và lên đến 1 triệu token với các phương pháp ngoại suy. Điều này cho phép mô hình xử lý toàn bộ kho lưu trữ, tài liệu kỹ thuật lớn hoặc lịch sử hội thoại dài trong một tác vụ duy nhất.

### Khi nào nên sử dụng mỗi mô hình

Bốn mô hình Qwen3 phục vụ các trường hợp sử dụng riêng biệt. Qwen3-Coder-480B-A35B-Instruct được thiết kế cho các tình huống kỹ thuật phần mềm phức tạp. Nó phù hợp để tạo mã nâng cao, xử lý ngữ cảnh dài như phân tích ở cấp độ kho lưu trữ và tích hợp với các công cụ bên ngoài. Qwen3-Coder-30B-A3B-Instruct đặc biệt hiệu quả cho các tác vụ như hoàn thiện mã, tái cấu trúc và trả lời các truy vấn liên quan đến lập trình. Nếu bạn cần hiệu suất linh hoạt trên nhiều lĩnh vực, Qwen3-235B-A22B-Instruct-2507 cung cấp sự cân bằng, mang lại khả năng suy luận đa mục đích và tuân theo hướng dẫn mạnh mẽ trong khi tận dụng các lợi thế hiệu quả của kiến trúc MoE. Qwen3-32B (Dense) phù hợp cho các tình huống mà hiệu suất ổn định, độ trễ thấp và tối ưu hóa chi phí là quan trọng.

### Bắt đầu với các mô hình Qwen trong Amazon Bedrock

Để bắt đầu sử dụng các mô hình Qwen, trong bảng điều khiển Amazon Bedrock, tôi có thể sử dụng phần **Chat/Text Playground** ở thanh điều hướng để nhanh chóng thử nghiệm các mô hình Qwen mới với một vài prompt.

Để tích hợp các mô hình Qwen3 vào ứng dụng của mình, tôi có thể sử dụng bất kỳ AWS SDKs nào. Các AWS SDK bao gồm quyền truy cập vào API **InvokeModel** và **Converse** của Amazon Bedrock. Tôi cũng có thể sử dụng các mô hình này với bất kỳ khuôn khổ tác nhân nào hỗ trợ Amazon Bedrock và triển khai các tác nhân bằng Amazon Bedrock AgentCore. Ví dụ: đây là mã Python của một tác nhân đơn giản với quyền truy cập công cụ được xây dựng bằng Strands Agents:

```python
from strands import Agent
from strands_tools import calculator

agent = Agent(
    model="qwen.qwen3-coder-480b-a35b-v1:0",
    tools=[calculator]
)

agent("Tell me the square root of 42 ^ 9")

with open("function.py", 'r') as f:
    my_function_code = f.read()

agent(f"Help me optimize this Python function for better performance:\n\n{my_function_code}")
```
### Hiện có sẵn

Các mô hình Qwen hiện đã được cung cấp tại các Khu vực AWS sau:

- **Qwen3-Coder-480B-A35B-Instruct** có sẵn ở các khu vực: US West (Oregon), Asia Pacific (Mumbai, Tokyo) và Europe (London, Stockholm).

- **Qwen3-Coder-30B-A3B-Instruct, Qwen3-235B-A22B-Instruct-2507 và Qwen3-32B** có sẵn ở các khu vực: US East (N. Virginia), US West (Oregon), Asia Pacific (Mumbai, Tokyo), Europe (Ireland, London, Milan, Stockholm) và South America (São Paulo).

Hãy kiểm tra [danh sách Khu vực đầy đủ](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/) để cập nhật trong tương lai. Bạn có thể bắt đầu thử nghiệm và xây dựng ngay lập tức mà không cần thiết lập cơ sở hạ tầng hoặc lập kế hoạch công suất. Để tìm hiểu thêm, hãy truy cập [trang sản phẩm Qwen trong Amazon Bedrock](https://aws.amazon.com/bedrock/features/qwen/) và [trang giá cả Amazon Bedrock](https://aws.amazon.com/bedrock/pricing/).

Hãy thử ngay các mô hình Qwen trên [bảng điều khiển Amazon Bedrock](https://console.aws.amazon.com/bedrock/), và đưa ra phản hồi thông qua [AWS re:Post for Amazon Bedrock](https://repost.aws/tags/TAxZAJ5PL9qHTYFdH8yKBPBw/amazon-bedrock) hoặc các kênh Hỗ trợ AWS thông thường của bạn.

— Danilo

**Cập nhật vào ngày 18 tháng 9 năm 2025** – Đã loại bỏ phần quyền truy cập mô hình. Amazon Bedrock sẽ đơn giản hóa quyền truy cập vào tất cả các mô hình nền không máy chủ, và bất kỳ mô hình mới nào, bằng cách tự động kích hoạt chúng cho mọi tài khoản AWS, loại bỏ việc cần kích hoạt thủ công thông qua bảng điều khiển Bedrock. Trang quyền truy cập mô hình sẽ ngừng hoạt động vào ngày 8 tháng 10 năm 2025. Quản trị viên tài khoản vẫn giữ toàn quyền kiểm soát quyền truy cập mô hình thông qua các chính sách AWS IAM và Chính Sách Kiểm Soát Dịch Vụ (SCPs) để hạn chế quyền truy cập mô hình khi cần.

---

![Hình ảnh Hồ sơ](/images/danilo.png)

**Danilo Poccia**

Danilo làm việc với các công ty khởi nghiệp và công ty thuộc mọi quy mô để hỗ trợ sự đổi mới của họ. Trong vai trò Chief Evangelist (EMEA) tại Amazon Web Services, anh ấy tận dụng kinh nghiệm của mình để giúp mọi người hiện thực hóa ý tưởng, tập trung vào kiến trúc không máy chủ và lập trình hướng sự kiện, cũng như tác động kỹ thuật và kinh doanh của máy học và điện toán biên. Ông là tác giả của AWS Lambda in Action từ Manning.