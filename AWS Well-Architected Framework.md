# AWS Well-Architected Framework

## Giới thiệu về AWS Well-Architected Framework

AWS Well-Architected Framework giúp bạn hiểu được những ưu và nhược điểm của các quyết định mà người phát triển đưa ra khi xây dựng hệ thống trên AWS. Bằng cách sử dụng Framework này, người sử dụng sẽ học được những thực hành tốt nhất về kiến trúc cho việc thiết kế và vận hành các <abbr title="khối lượng công việc - đề cập đến các ứng dụng, dịch vụ, hoặc tập hợp các hoạt động mà một hệ thống phải xử lý">workload</abbr> an toàn, đáng tin cậy, hiệu quả, chi phí hiệu quả và bền vững trên đám mây AWS.

AWS Well-Architected Framework cung cấp một cách thức nhất quán để đánh giá hệ thống so với các thực hành tốt nhất và xác định những lĩnh vực cần cải thiện. Quá trình đánh giá kiến trúc là một cuộc đối thoại xây dựng về các quyết định kiến trúc, không phải là một cơ chế kiểm toán.

>Các hệ thống được thiết kế tốt --> Làm tăng đáng kể khả năng thành công của doanh nghiệp.

AWS Well-Architected Framework cung cấp một tập hợp các câu hỏi và cách tiếp cận nhất quán để đánh giá và đưa ra các khuyến nghị cải thiện để thiết kế kiến trúc phù hợp với các thực hành tốt nhất cho hệ thống đám mây hiện đại.

Framework này dành cho những người trong các vai trò kỹ thuật, như giám đốc công nghệ (CTO), kiến trúc sư, lập trình viên và thành viên nhóm vận hành. 
Nó mô tả các thực hành và chiến lược tốt nhất của AWS khi thiết kế và vận hành workload trên đám mây, và cung cấp liên kết đến các chi tiết triển khai và mẫu kiến trúc thêm (xem thêm tại [đây](https://aws.amazon.com/vi/architecture/well-architected/)).

AWS Well-Architected Tool (AWS WA Tool) là một dịch vụ trên đám mây cung cấp một quy trình nhất quán giúp đánh giá và đo lường kiến trúc bằng AWS Well-Architected Framework. AWS WA Tool cung cấp các khuyến nghị để giúp workload trở nên đáng tin cậy, an toàn, hiệu quả và chi phí hiệu quả hơn.

### Các định nghĩa

AWS Well-Architected Framework dựa trên sáu trụ cột:

| Trụ cột                                                        | Mô tả                                                                                                                                                                                                                                                 |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <abbr title="Vận hành xuất sắc">Operational excellence</abbr>  | Khả năng hỗ trợ phát triển và vận hành workload một cách hiệu quả, liên tục cải tiến các quy trình và thủ tục hỗ trợ để mang lại giá trị kinh doanh                                                                                                   |
| <abbr title="Bảo mật">Security</abbr>                          | Tận dụng công nghệ đám mây để bảo vệ dữ liệu, hệ thống và tài nguyên theo cách có thể.                                                                                                                                                                |
| <abbr title="Độ tin cậy">Reliability</abbr>                    | Khả năng workload thực hiện chức năng dự định của nó một cách chính xác và nhất quán.                                                                                                                                                                 |
| <abbr title="Hiệu suất vận hành">Performance efficiency</abbr> | Khả năng sử dụng tài nguyên máy tính một cách hiệu quả để đáp ứng các yêu cầu của hệ thống và duy trì hiệu quả đó khi nhu cầu thay đổi và công nghệ phát triển.                                                                                       |
| <abbr title="Tối ưu hoá chi phí">Cost optimization</abbr>      | Khả năng vận hành các hệ thống để mang lại giá trị kinh doanh ở mức giá thấp nhất.                                                                                                                                                                    |
| <abbr title="Tính bền vững">Sustainability</abbr>              | Khả năng liên tục cải thiện tác động bền vững bằng cách giảm tiêu thụ năng lượng và tăng hiệu quả trên tất cả các thành phần của workload bằng cách tối đa hóa lợi ích từ các tài nguyên được cung cấp và giảm thiểu tổng nguồn tài nguyên cần thiết. |

Bên cạnh đó AWS Well-Architect Framework còn sử dụng các thuật ngữ sau:

- Một **component** (thành phần) là code, cấu hình và Tài nguyên AWS cùng hoạt động để đáp ứng một yêu cầu. Một component thường là đơn vị sở hữu kỹ thuật và được tách biệt với các component khác.

- Thuật ngữ **workload** được sử dụng để xác định một tập hợp các component cùng nhau mang lại giá trị kinh doanh. Một workload thường là mức độ chi tiết mà lãnh đạo kinh doanh và công nghệ đề cập đến.

- Chúng ta coi **architecture** (kiến trúc) là cách các component hoạt động cùng nhau trong một workload. Cách thức giao tiếp và tương tác giữa các component thường là trọng tâm của sơ đồ architecture.

- **Milestone** (mốc) đánh dấu những thay đổi chủ chốt trong architecture của bạn khi nó phát triển trong suốt vòng đời sản phẩm (thiết kế, triển khai, kiểm thử, đưa vào vận hành và trong giai đoạn sản xuất).

- Trong tổ chức, **technology portfolio** là tập hợp các workload cần thiết để doanh nghiệp hoạt động.

- **Level of effort** (Mức độ nỗ lực) được phân loại theo lượng thời gian, công sức và độ phức tạp mà một tác vụ đòi hỏi để triển khai. Mỗi tổ chức cần xem xét quy mô và chuyên môn của nhóm cũng như độ phức tạp của workload để xác định level of effort phù hợp cho tổ chức đó.
	- **Cao**: Công việc có thể mất nhiều tuần hoặc nhiều tháng. Điều này có thể được chia nhỏ thành nhiều câu chuyện, phiên bản và nhiệm vụ.
	- **Trung bình**: Công việc có thể mất nhiều ngày hoặc nhiều tuần. Điều này có thể được chia nhỏ thành nhiều phiên bản và nhiệm vụ.
	- **Thấp**: Công việc có thể mất nhiều giờ hoặc nhiều ngày. Điều này có thể được chia nhỏ thành nhiều nhiệm vụ.

Khi thiết kế architecture cho workload, cần phải cân bằng giữa các trụ cột dựa trên bối cảnh kinh doanh.

VD: trong môi trường phát triển, có thể hy sinh độ tin cậy để giảm chi phí; trong các giải pháp quan trọng, cần tối ưu hoá độ tin cậy từ đó dẫn đến chi phí và tác động bền vững tăng lên,...

> Bảo mật và Hiệu suất vận hành thường không được cân bằng với các trụ cột khác.

### Về kiến trúc

Thường có một nhóm trung tâm cho kiến trúc công nghệ với các vai trò như kiến trúc sư kỹ thuật, kiến trúc sư giải pháp, kiến trúc sư dữ liệu, kiến trúc sư mạng và kiến trúc sư bảo mật.

Thay vì có một nhóm kiến trúc tập trung, AWS phân tán khả năng kiến trúc vào các nhóm sản phẩm/tính năng khác nhau. Điều này giúp các nhóm tập trung vào nhu cầu của khách hàng và xây dựng sản phẩm phù hợp.

> "Ý định tốt không bao giờ có tác dụng, cần có cơ chế tốt để thực hiện hoá mọi thứ" - Jeff Bezos.

Để đảm bảo chất lượng và tuân thủ tiêu chuẩn, AWS có hai cách thức chính:
- Thiết lập các thực hành, quy trình, tiêu chuẩn được chấp nhận và có chuyên gia xác minh việc tuân thủ của các nhóm.
- Triển khai cơ chế kiểm tra tự động để kiểm tra việc đáp ứng các tiêu chuẩn, thay vì hoàn toàn dựa vào nỗ lực con người.

AWS tin rằng kiến trúc doanh nghiệp tốt có thể nảy sinh khi các nhóm tập trung vào nhu cầu khách hàng và tuân thủ các thực hành, các hướng dẫn tốt nhất thông qua mô hình phân tán với cộng đồng kỹ sư chính. Đánh giá Well-Architected Framework giúp hiểu rõ rủi ro và xác định vấn đề cần cải thiện bằng cơ chế, đào tạo hoặc chia sẻ kiến thức.

### Nguyên tắc thiết kế chung

- **Ngừng đoán nhu cầu về tài nguyên**: Trên đám mây, bạn có thể động thái co giãn tài nguyên lên hoặc xuống dựa trên nhu cầu, tránh cung cấp quá nhiều hoặc không đủ.
- **Thử nghiệm hệ thống trên quy mô sản xuất**: Triển khai môi trường kiểm tra quy mô sản xuất theo nhu cầu trên đám mây để kiểm tra, sau đó dỡ bỏ khi xong để tránh chi phí liên tục.
- **Tự động hóa với định hướng thử nghiệm**: Tự động hóa triển khai và khai thác cơ sở hạ tầng bất biến để bạn có thể thử nghiệm, theo dõi thay đổi và dễ dàng khôi phục nếu cần.
- **Cân nhắc các kiến trúc tiến hóa**: Đám mây tạo điều kiện cho kiến trúc tiến hóa theo thời gian thay vì những nỗ lực tái thiết kế lớn, hiếm dùng.
- **Cải thiện kiến trúc bằng việc thu thập dữ liệu**: Thu thập số liệu về tác vụ của bạn để lập trình các lựa chọn thiết kế và cải tiến theo cách thức lặp đi lặp lại.
- **Cải thiện qua *game days***: Định kỳ mô phỏng sự cố/sự kiện thực tế trong môi trường sản xuất để kiểm tra khả năng phục hồi và tìm ra lĩnh vực cần cải thiện quy trình và kiến trúc.

## Trụ cột 1: Operational excellence - Vận hành xuất sắc

Trụ cột Vận hành xuất sắc bao gồm khả năng hỗ trợ phát triển và vận hành workload một cách hiệu quả, hiểu rõ hơn về hoạt động của chúng và liên tục cải tiến các quy trình và thủ tục hỗ trợ để mang lại giá trị kinh doanh.

### Nguyên tắc thiết kế

1. Thực hiện hoạt động dưới dạng code:
   - Định nghĩa toàn bộ môi trường làm việc (ứng dụng, hạ tầng) dưới dạng code.
   - Cập nhật môi trường bằng code.
   - Lập trình các quy trình vận hành và tự động hóa chúng để đáp ứng sự kiện.
   - Giảm thiểu lỗi con người và đảm bảo phản ứng nhất quán.

2. Thực hiện thay đổi nhỏ, đảo ngược thường xuyên:
   - Thiết kế môi trường có khả năng mở rộng và linh hoạt.
   - Cập nhật thường xuyên các thành phần.
   - Sử dụng kỹ thuật triển khai tự động.
   - Thay đổi nhỏ, từng bước để giảm bán kính ảnh hưởng của sự cố.
   - Đảo ngược nhanh chóng khi có lỗi.
   - Tăng Độ tin cậy để thích ứng với thay đổi thị trường.

3. Hoàn thiện quy trình thường xuyên:
   - Xem xét và cập nhật quy trình khi môi trường phát triển.
   - Đánh giá hiệu quả của quy trình và kiến thức của nhóm.
   - Cập nhật, truyền đạt và đào tạo các thay đổi quy trình.
   - Chia sẻ phương pháp hay nhất cho các thành viên trong nhóm.

4. Dự đoán sự cố:  
   - Thực hiện "phân tích hậu quả (pre-moterm)" để xác định nguồn lỗi tiềm ẩn.
   - Loại bỏ hoặc giảm nhẹ các nguyên nhân gây lỗi.
   - Kiểm tra kịch bản sự cố và quy trình ứng phó.
   - Tổ chức các game days để mô phỏng các sự cố.

5. Học hỏi từ sự cố:
   - Rút ra bài học từ tất cả sự cố vận hành.
   - Chia sẻ bài học trong nhóm và toàn bộ tổ chức.

6. Sử dụng dịch vụ được quản lý:
   - Sử dụng các dịch vụ được quản lý của AWS.
   - Xây dựng quy trình tương tác với các dịch vụ đó.

7. Triển khai quan sát hiệu quả: 
   - Theo dõi hành vi, hiệu suất, độ tin cậy, chi phí, sức khỏe.
   - Thiết lập chỉ số hiệu suất chính (KPI).
   - Sử dụng dữ liệu quan sát để ra quyết định và hành động.
   - Cải thiện hiệu suất, độ tin cậy, chi phí dựa trên dữ liệu.

Nhìn chung là áp dụng nguyên lý phát triển phần mềm, tự động hóa quy trình, thường xuyên đánh giá và cải tiến, dự đoán rủi ro, chia sẻ kinh nghiệm và tận dụng các công cụ điện toán đám mây để thực hiện tốt trụ cột này.

## Trụ cột 2: Security - Bảo mật

Trụ cột Bảo mật bao gồm khả năng bảo vệ dữ liệu, hệ thống và tài nguyên, tận dụng công nghệ đám mây nhằm cải thiện bảo mật cho hệ thống, kiến trúc.

### Nguyên tắc thiết kế

1. Xây dựng nền tảng định danh mạnh:
   - Áp dụng nguyên tắc cấp quyền tối thiểu.
   - Thực hiện phân tách nhiệm vụ.
   - Tập trung hóa quản lý định danh.
   - Giảm sử dụng thông tin xác thực tĩnh dài hạn.

2. Duy trì khả năng truy vết:
   - Giám sát và cảnh báo trong thời gian thực.
   - Kiểm toán các hành động và thay đổi.
   - Tích hợp thu thập log và metric.
   - Tự động hóa việc điều tra và phản ứng.

3. Áp dụng bảo mật nhiều lớp:
   - Sử dụng phương pháp phòng thủ theo chiều sâu.
   - Bảo vệ tất cả các tầng: từ mạng đến mã nguồn.

4. Tự động hóa thực hành bảo mật:
   - Triển khai các cơ chế bảo mật tự động.
   - Xây dựng kiến trúc bảo mật bằng mã.
   - Quản lý các biện pháp kiểm soát trong template có version.

5. Bảo vệ dữ liệu:
   - Phân loại dữ liệu theo độ nhạy cảm.
   - Sử dụng mã hóa, tokenization và kiểm soát truy cập.

6. Hạn chế tiếp xúc trực tiếp với dữ liệu:
   - Sử dụng công cụ giảm thiểu xử lý thủ công.
   - Giảm nguy cơ lỗi do con người.

7. Chuẩn bị cho sự cố bảo mật:
   - Xây dựng quy trình quản lý và điều tra sự cố.
   - Thực hiện mô phỏng ứng phó.
   - Sử dụng công cụ tự động để tăng tốc phát hiện và khôi phục.

Các nguyên tắc này tạo nên một chiến lược toàn diện, giúp tăng cường bảo mật, giảm thiểu rủi ro và cải thiện khả năng ứng phó với các mối đe dọa khi triển khai hệ thống trên môi trường đám mây.

## Trụ cột 3: Reliability - Độ tin cậy

Trụ cột Độ tin cậy bao gồm khả năng các workload thực hiện chức năng dự định của nó một cách chính xác và nhất quán như mong đợi. Điều này bao gồm khả năng vận hành và kiểm tra workload trong toàn bộ vòng đời của nó.

### Nguyên tắc thiết kế

1. Tự động phục hồi sau lỗi:
   - Giám sát các chỉ số hiệu suất quan trọng (KPI) của workload.
   - Tập trung vào các KPI đo lường giá trị kinh doanh, không phải khía cạnh kỹ thuật.
   - Thiết lập hệ thống tự động khi vượt ngưỡng KPI.
   - Tự động hóa việc thông báo, theo dõi và khắc phục lỗi.
   - Phát triển khả năng dự đoán và ngăn chặn lỗi trước khi xảy ra.

2. Kiểm tra quy trình phục hồi:
   - Khác biệt với môi trường <abbr title="lưu trữ và quản lý phần cứng, phần mềm và dữ liệu tại chỗ">on-premises</abbr>, tập trung vào kiểm tra chiến lược phục hồi.
   - Sử dụng môi trường đám mây để mô phỏng các kịch bản lỗi.
   - Tái tạo các tình huống lỗi đã xảy ra trước đó.
   - Phát hiện và sửa chữa các lỗ hổng trước khi chúng gây ra vấn đề thực tế.
   - Giảm thiểu rủi ro bằng cách chuẩn bị kỹ lưỡng cho các tình huống lỗi.

3. Mở rộng theo chiều ngang:
   - Thay thế các tài nguyên lớn bằng nhiều tài nguyên nhỏ hơn.
   - Phân tán yêu cầu trên nhiều tài nguyên để tránh điểm lỗi chung.
   - Tăng khả năng chịu lỗi tổng thể của hệ thống.
   - Giảm thiểu tác động của lỗi đơn lẻ đối với toàn bộ workload.

4. Quản lý công suất linh hoạt:
   - Tránh bão hòa tài nguyên, một vấn đề phổ biến trong môi trường on-premises.
   - Giám sát liên tục nhu cầu và mức sử dụng workload.
   - Tự động thêm hoặc xóa tài nguyên để đáp ứng nhu cầu.
   - Tối ưu hóa việc sử dụng tài nguyên, tránh cung cấp quá mức hoặc thiếu hụt.
   - Quản lý hiệu quả các giới hạn và hạn ngạch dịch vụ.

5. Tự động hóa quản lý thay đổi:
   - Thực hiện các thay đổi cơ sở hạ tầng thông qua tự động hóa.
   - Áp dụng tự động hóa cho cả quá trình thay đổi và quy trình tự động hóa.
   - Theo dõi và xem xét các thay đổi một cách có hệ thống.
   - Giảm thiểu lỗi do con người và tăng tính nhất quán trong quản lý hệ thống.

Các nguyên tắc này kết hợp với nhau để tạo ra một hệ thống đám mây đáng tin cậy, linh hoạt và hiệu quả, có khả năng tự phục hồi và thích ứng với các thay đổi và thách thức.

