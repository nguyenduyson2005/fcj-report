---
title: "Blog 1"
date: "2025-10-10"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Mở rộng quy mô sản xuất hình ảnh bằng Stability AI Image Services trong Amazon Bedrock

**Bởi Alex Gnibus, Isha Dua, Fabio Branco và Suleman Patel | ngày 18 tháng 9 năm 2025|  Amazon Bedrock, Amazon Machine Learning, Amazon SageMaker AI, Announcements, Artificial Intelligence, Foundation models, Generative AI, Launch**  

Bài viết này được viết cùng với Alex Gnibus của Stability AI.

Stability AI Image Services hiện đã có sẵn trong Amazon Bedrock, mang đến khả năng chỉnh sửa phương tiện sẵn sàng sử dụng thông qua Amazon Bedrock API.
Các công cụ chỉnh sửa hình ảnh này mở rộng khả năng của các mô hình Stable Diffusion 3.5 (SD3.5) và Stable Image Core và Ultra của Stability AI, vốn đã có trong Amazon Bedrock và đang thiết lập tiêu chuẩn mới trong việc tạo sinh hình ảnh.

Quy trình sản xuất sáng tạo chuyên nghiệp bao gồm nhiều bước chỉnh sửa để tạo ra kết quả chính xác như mong muốn. Với Dịch vụ Hình ảnh Stability AI trong Amazon Bedrock, bạn có thể chỉnh sửa, nâng cấp và biến đổi các hình ảnh hiện có mà không cần phải chuyển đổi giữa nhiều hệ thống hay gửi tệp đến các dịch vụ bên ngoài. Mọi thao tác đều được thực hiện trong cùng một môi trường Amazon Bedrock mà bạn đang sử dụng. Tác động kinh doanh có thể diễn ra ngay lập tức đối với các nhóm sản xuất nội dung hình ảnh quy mô lớn.
Trong bài viết này, chúng ta sẽ cùng tìm hiểu các ví dụ về cách những công cụ này mang lại khả năng kiểm soát sáng tạo chính xác giúp tăng tốc việc tạo ra nội dung hình ảnh đạt chất lượng chuyên nghiệp.

Trong bài viết này, chúng ta sẽ cùng tìm hiểu các ví dụ về cách những công cụ này mang lại khả năng kiểm soát sáng tạo chính xác giúp tăng tốc việc tạo ra nội dung hình ảnh đạt chất lượng chuyên nghiệp.

## Các công cụ chỉnh sửa hiện đã có mặt trong Amazon Bedrock

Stability AI Image Services bao gồm 13 công cụ thuộc ba nhóm: Chỉnh sửa (Edit), Nâng cấp (Upscale) và Kiểm soát (Control). Mỗi công cụ xử lý một tác vụ chỉnh sửa cụ thể, vốn thường đòi hỏi phần mềm chuyên dụng hoặc thao tác thủ công.

### Edit: Các khả năng nâng cao cho các bước chỉnh sửa chi tiết

Những công cụ trong nhóm Edit giúp cho các tác vụ chỉnh sửa phức tạp trở nên dễ tiếp cận và hiệu quả hơn.
 
Bộ công cụ này bắt đầu với những công cụ chỉnh sửa cơ bản nhưng mạnh mẽ. Ví dụ, công cụ Erase Object có thể loại bỏ các chi tiết không mong muốn khỏi hình ảnh đồng thời tự động giữ nguyên sự nhất quán của phông nền. Hình minh họa dưới đây cho thấy công cụ Erase Object loại bỏ một ma-nơ-canh khỏi ảnh chụp sản phẩm trong khi vẫn giữ nguyên nền. Công cụ này có thể biến đổi một hình ảnh gốc dựa trên ảnh mặt nạ (mask image), hoặc tự động tạo mặt nạ từ kênh alpha của ảnh gốc.

![Example Image](/images/ml-19647-1.gif)

Công cụ Remove Background tự động tách chủ thể với độ chính xác cao. Điều này cho phép tạo ra các danh sách sản phẩm sạch sẽ, chuyên nghiệp với nền đồng nhất hoặc nhiều bối cảnh phong cách sống khác nhau, mang tính đột phá cho thương mại điện tử.

Ví dụ dưới đây minh họa việc xóa nền của một hình ảnh, trong khi vẫn giữ nguyên chi tiết của sản phẩm nội thất ở tiền cảnh.

![Example Image](/images/ml-19647-2.gif)

Các công cụ Search and Recolor và Search and Replace tập trung vào việc chỉnh sửa các yếu tố cụ thể trong hình ảnh. Search and Recolor thay đổi màu sắc của đối tượng, ví dụ như thể hiện các phiên bản màu khác nhau của một chiếc váy mà không cần thực hiện buổi chụp ảnh mới. Trong minh họa dưới đây, công cụ Search and Recolor được sử dụng để thay đổi màu của một món đồ nội thất.

![Example Image](/images/ml-19647-3.gif) 

Công cụ Search and Replace có thể thay thế hoàn toàn các đối tượng trong hình ảnh, rất hữu ích khi cần cập nhật các yếu tố theo mùa trong tài liệu tiếp thị hoặc thay thế sản phẩm. Ví dụ dưới đây minh họa việc ứng dụng Search and Replace trong các trải nghiệm thử đồ ảo.

![Example Image](/images/ml-19647-4.gif) 

Công cụ Inpaint chỉnh sửa hình ảnh một cách thông minh bằng cách lấp đầy hoặc thay thế các vùng được chỉ định bằng nội dung mới dựa trên ảnh mặt nạ (mask image). Ngược lại, công cụ Outpaint tạo thêm nội dung để mở rộng hình ảnh theo bất kỳ hướng nào. So với các phương pháp mở rộng hình ảnh tự động hoặc thủ công khác, Outpaint giảm thiểu tối đa các tạo tác (artifacts) và dấu vết cho thấy hình ảnh gốc đã bị chỉnh sửa.

### Upscale: Nâng cấp hình ảnh đạt chất lượng chuyên nghiệp

Nâng độ phân giải (Upscale): Nâng cấp hình ảnh đạt chất lượng chuyên nghiệp
Ba trong số các Dịch vụ Hình ảnh Stability AI (Stability AI Image Services) mới cung cấp các phương pháp tiếp cận khác nhau để nâng độ phân giải (upscale) và cải thiện chất lượng hình ảnh, mỗi công cụ được thiết kế cho các trường hợp sử dụng (use cases) cụ thể.

Công cụ Creative Upscale nâng cao độ phân giải đồng thời bổ sung các chi tiết được cải thiện bằng AI. Công cụ này làm tăng cả số lượng điểm ảnh (pixel) và sức hấp dẫn thị giác, khiến nó phù hợp cho các tài liệu tiếp thị có tác động cao. Những bức ảnh chụp sản phẩm tiêu chuẩn có thể trở thành hình ảnh sẵn sàng cho quảng cáo ngoài trời (billboard) thông qua việc bổ sung chi tiết thông minh và tăng cường độ sống động.

![Example Image](/images/ml-19647-5.gif) 

Đối với những tình huống mà việc duy trì tính toàn vẹn của hình ảnh gốc là rất quan trọng, công cụ Conservative Upscale mang đến một cách tiếp cận tinh tế hơn. Nó tăng độ phân giải trong khi vẫn giữ nguyên chi tiết và đặc trưng của hình ảnh ban đầu. Dịch vụ này có thể phóng to (upscale) hình ảnh lên gấp 20 đến 40 lần, tạo ra hình ảnh đầu ra lên đến 4 triệu điểm ảnh (4-megapixel) với sự thay đổi tối thiểu so với hình ảnh gốc.

![Example Image](/images/ml-19647-6.gif) 

Hoàn thiện bộ ba công cụ là Fast Upscale. Công cụ này nhanh hơn hai công cụ trước và lý tưởng để nâng cao chất lượng của các hình ảnh bị nén (compress), khiến nó phù hợp cho các bài đăng mạng xã hội (social media posts) và các ứng dụng khác.

![Example Image](/images/ml-19647-7.gif) 

### Control: Độ chính xác về cấu trúc và phong cách

Nhóm công cụ này cung cấp khả năng thao tác chính xác về cấu trúc và phong cách của hình ảnh thông qua ba công cụ chuyên biệt.

Công cụ Sketch chuyển đổi các bản vẽ phác thảo thành hình ảnh mang tính chân thực cao. Các công ty kiến trúc có thể sử dụng công cụ này để biến các bản thiết kế ý tưởng thành hình ảnh mô phỏng thực tế, trong khi các thương hiệu thời trang có thể dùng để chuyển bản phác thảo thiết kế thành mô hình sản phẩm. Công cụ này giúp tăng tốc quy trình sáng tạo, từ giai đoạn ý tưởng ban đầu đến hình ảnh hoàn chỉnh.

Trong ví dụ này, công cụ Sketch chuyển đổi bản vẽ kiến trúc của một tòa nhà thành hình ảnh giúp các nhà phát triển bất động sản hình dung ý tưởng trong bối cảnh đô thị.

![Example Image](/images/ml-19647-8.gif) 

Trong một ví dụ khác, công cụ Sketch chuyển đổi bản vẽ ma-nơ-canh thành hình ảnh chụp người mẫu mang tính chân thực cao.

![Example Image](/images/ml-19647-9.gif)

Công cụ Structure giữ nguyên các yếu tố cấu trúc của hình ảnh đầu vào trong khi vẫn cho phép thay đổi nội dung. Công cụ này giúp bảo toàn bố cục, cách sắp xếp và mối quan hệ không gian giữa các thành phần khi thay đổi chủ thể hoặc phong cách. Các nhóm sáng tạo có thể sử dụng công cụ Structure để tái tạo lại khung cảnh với các chủ thể khác, hoặc tạo ra nhân vật mới mà vẫn giữ nguyên bố cục và khung hình nhất quán.

Ví dụ dưới đây minh họa công cụ Structure chuyển đổi một khung cảnh xưởng làm việc thành một khung cảnh mới trong khi vẫn duy trì bố cục và mối quan hệ không gian ban đầu.

![Example Image](/images/ml-19647-10.gif)

Các công cụ Style Guide và Style Transfer giúp các nhóm tiếp thị tạo ra hình ảnh mới phù hợp với phong cách và hướng dẫn nhận diện thương hiệu. Công cụ Style Guide lấy phong cách nghệ thuật và tông màu từ một hình ảnh tham chiếu, sau đó tạo ra các hình ảnh mới dựa trên mô tả văn bản.

Trong ví dụ dưới đây, công cụ Style Guide sử dụng bảng màu và chất liệu đặc trưng của thương hiệu để tạo ra các hình ảnh mới phù hợp với bản sắc thương hiệu.

![Example Image](/images/ml-19647-11.gif)

Công cụ Style Transfer sử dụng các đặc điểm thị giác từ hình ảnh tham chiếu để biến đổi những hình ảnh hiện có, đồng thời vẫn giữ nguyên bố cục gốc. Ví dụ, một nhà bán lẻ đồ trang trí nội thất có thể chuyển đổi hình ảnh sản phẩm từ phong cách tối giản hiện đại sang phong cách truyền thống mà không cần chụp ảnh mới. Các nhóm tiếp thị cũng có thể tạo ra các phiên bản theo mùa bằng cách áp dụng những phong cách thị giác khác nhau lên danh mục sản phẩm sẵn có.

## Tổng quan về giải pháp

Để minh họa cho Dịch vụ Hình ảnh Stability AI trong Amazon Bedrock, chúng ta sẽ cùng xem qua một ví dụ sử dụng Jupyter notebook có sẵn trong kho mã GitHub.

## Yêu cầu trước khi thực hiện 

Để làm theo ví dụ này, bạn cần có các điều kiện sau:

- Một tài khoản AWS.
- Thông tin AWS credentials đã được cấu hình để tạo và truy cập tài nguyên Amazon Bedrock và Amazon SageMaker AI.
- Một vai trò thực thi của AWS Identity and Access Management (IAM) dành cho SageMaker AI, được gắn với hai chính sách quản lý là AmazonSageMakerFullAccess và AmazonBedrockLimitedAccess. Để biết thêm chi tiết, xem mục How to use SageMaker AI execution roles.
- Một SageMaker notebook instance.
- Quyền truy cập mô hình Stability AI Image Services, có thể được yêu cầu thông qua bảng điều khiển Amazon Bedrock. Tham khảo thêm tại Access Amazon Bedrock foundation models để biết chi tiết.

## Tạo một notebook instance trong SageMaker AI

Thực hiện các bước sau để tạo một SageMaker AI notebook instance, dùng để chạy notebook mẫu:

1. Trong bảng điều khiển SageMaker AI, ở thanh điều hướng bên trái, trong phần Applications and IDEs, chọn Notebooks.
2. Chọn Create notebook instance.
3. Ở mục Notebook instance name, nhập tên cho notebook instance của bạn (ví dụ: ai-images-notebook-instance).
4. Ở mục Notebook instance type, chọn ml.t2.medium.
5. Ở mục Platform identifier, chọn Amazon Linux 2.
6. Ở mục IAM role, chọn một vai trò IAM đã có sẵn với hai chính sách AmazonSageMakerFullAccess và AmazonBedrockLimitedAccess, hoặc chọn Create a new role để tạo vai trò mới.
7. Ghi lại tên của IAM role mà bạn đã chọn.
8. Giữ nguyên các thiết lập khác ở giá trị mặc định và chọn Create notebook instance.

Sau vài phút, SageMaker AI sẽ tạo notebook instance, và trạng thái của nó sẽ chuyển từ Pending sang InService.

## Xác nhận vai trò IAM của notebook instance có đủ quyền cần thiết

Thực hiện các bước sau để kiểm tra xem vai trò thực thi của SageMaker AI được gán cho notebook instance đã có đầy đủ quyền hay chưa:

1. Trong bảng điều khiển IAM, ở thanh điều hướng bên trái, trong phần Access management, chọn Roles.
2. Trong thanh tìm kiếm Roles, nhập tên của SageMaker AI execution role mà bạn đã sử dụng khi tạo notebook instance.
3. Chọn vai trò IAM đó.
4. Trong phần Permissions policies, kiểm tra xem hai chính sách do AWS quản lý là AmazonSageMakerFullAccess và AmazonBedrockLimitedAccess có xuất hiện hay không.
5. (Tùy chọn) Nếu thiếu một trong hai chính sách, chọn Add permissions, sau đó chọn Attach policies để gắn thêm chính sách bị thiếu.

    a. Trong thanh tìm kiếm Other permissions policies, nhập tên của chính sách cần thêm.

    b. Chọn chính sách đó, rồi chọn Add permissions để hoàn tất.

## Chạy notebook

 Thực hiện các bước sau để chạy notebook:

1. Trong bảng điều khiển SageMaker AI, ở thanh điều hướng bên trái, trong phần Applications and IDEs, chọn Notebooks.
2. Chọn notebook instance mà bạn vừa tạo — ai-images-notebook-instance.
3. Chờ đến khi notebook có trạng thái InService.
4. Chọn liên kết Open JupyterLab để mở JupyterLab trong một tab trình duyệt mới.
5. Trong menu Git, chọn Clone a Repository.
6. Nhập đường dẫn `https://github.com/aws-samples/stabilityai-sample-notebooks.git` và chọn Include submodules và Download the repository.
7. Chọn Clone.
8. Trong menu File, chọn Open from path.
9. Nhập đường dẫn sau:
`stabilityai-sample-notebooks/stability-ai-image-services/stability-ai-image-services-sample-notebook.ipynb`
1.  Chọn Open.
2.  Khi được hỏi, chọn kernel là conda_python3, sau đó chọn Select.
3.  Chạy lần lượt từng ô trong notebook để trải nghiệm Stability AI Image Services in Amazon Bedrock.

## Dọn dẹp tài nguyên

Để tránh phát sinh chi phí, hãy dừng SageMaker AI notebook instance có tên ai-images-notebook-instance mà bạn đã tạo trong hướng dẫn này:

1. Trong bảng điều khiển SageMaker AI, ở thanh điều hướng bên trái, trong phần Applications and IDEs, chọn Notebooks
2. Chọn SageMaker AI notebook instance có tên ai-images-notebook-instance mà bạn đã tạo.
3. Chọn Actions, sau đó chọn Stop.

Sau vài phút, notebook instance sẽ chuyển trạng thái từ Stopping sang Stopped.

4. Tiếp theo, chọn Actions, rồi chọn Delete.

Sau vài giây, SageMaker AI sẽ xóa notebook instance đó.

Để biết thêm chi tiết, tham khảo mục Clean up Amazon SageMaker notebook instance resources.

## Kết luận

Việc Stability AI Image Services có mặt trong Amazon Bedrock là một bước tiến đầy hứa hẹn trong lĩnh vực tạo và chỉnh sửa nội dung hình ảnh, đặc biệt mang lại lợi ích tiết kiệm thời gian cho các nhóm sáng tạo chuyên nghiệp trong doanh nghiệp.

Ví dụ, trong lĩnh vực truyền thông và giải trí, các nhà sáng tạo có thể nhanh chóng nâng cấp cảnh quay và tạo hiệu ứng đặc biệt, trong khi các nhóm tiếp thị có thể dễ dàng tạo ra nhiều biến thể chiến dịch khác nhau. Ngành bán lẻ và thương mại điện tử có thể tối ưu quy trình chụp ảnh sản phẩm và xây dựng danh mục kỹ thuật số, còn nhà phát triển trò chơi có thể tạo mẫu môi trường nhanh hơn. Các công ty kiến trúc có thể trực quan hóa ý tưởng thiết kế ngay lập tức, và các tổ chức giáo dục có thể tạo ra nội dung trực quan hấp dẫn hơn.

Với các công cụ này, doanh nghiệp ở mọi quy mô đều có thể sản xuất nội dung hình ảnh chuyên nghiệp, sinh động và sáng tạo một cách hiệu quả. Chúng giúp đơn giản hóa quy trình, giảm chi phí và mở ra nhiều khả năng sáng tạo mới — hỗ trợ thương hiệu kể câu chuyện của mình rõ nét hơn và thu hút khách hàng tốt hơn.

Để bắt đầu, hãy khám phá các mô hình Stability AI trong Amazon Bedrock và AWS Samples trên kho GitHub.

___________________________________________________________________________________________________________________________________________

### Về các tác giả

![Profile Image](/images/ml-19647-12.jpeg)

**Alex Gnibus** là Quản lý Tiếp thị Sản phẩm tại Stability AI, người kết nối giữa những đột phá nghiên cứu tiên tiến và các trường hợp ứng dụng thực tiễn. Với kinh nghiệm làm việc từ các công ty sáng tạo đến công nghệ doanh nghiệp chuyên sâu, Alex mang đến cả kiến thức kỹ thuật lẫn sự thấu hiểu về những thách thức mà các nhóm sáng tạo chuyên nghiệp có thể giải quyết bằng công nghệ generative AI.

![Profile Image](/images/ml-19647-13.png)

**Isha Dua** là Kiến trúc sư Giải pháp Cấp cao (Senior Solutions Architect) tại khu vực Vịnh San Francisco. Cô giúp các khách hàng doanh nghiệp của AWS phát triển bằng cách hiểu rõ mục tiêu và thách thức của họ, đồng thời hướng dẫn cách xây dựng ứng dụng trên nền tảng đám mây sao cho vừa có khả năng mở rộng, vừa đảm bảo tính ổn định. Isha đặc biệt đam mê các công nghệ học máy và phát triển bền vững môi trường.

![Profile Image](/images/ml-19647-14.png)

**Fabio Branco** là Quản lý Giải pháp Khách hàng Cấp cao (Senior Customer Solutions Manager) tại Amazon Web Services (AWS) và là cố vấn chiến lược giúp khách hàng đạt được chuyển đổi doanh nghiệp, thúc đẩy đổi mới thông qua các giải pháp dữ liệu và AI tạo sinh, đồng thời định hướng hành trình lên đám mây thành công. Trước khi gia nhập AWS, ông từng đảm nhận các vai trò trong Quản lý Sản phẩm, Kỹ thuật, Tư vấn và Triển khai Công nghệ tại nhiều công ty Fortune 500 trong các lĩnh vực như bán lẻ, hàng tiêu dùng, dầu khí, dịch vụ tài chính, bảo hiểm và hàng không vũ trụ.

![Profile Image](/images/ml-19647-15.jpg) 

**Suleman Patel** là Kiến trúc sư Giải pháp Cấp cao (Senior Solutions Architect) tại Amazon Web Services (AWS), tập trung vào lĩnh vực học máy và hiện đại hóa hạ tầng. Với chuyên môn kết hợp giữa kinh doanh và công nghệ, Suleman giúp khách hàng thiết kế và xây dựng các giải pháp giải quyết những vấn đề thực tiễn trong doanh nghiệp. Ngoài công việc, anh yêu thích khám phá thiên nhiên, đi du lịch bằng xe đường dài và nấu ăn những món ngon trong bếp.