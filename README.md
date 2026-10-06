# [Vận dụng chuyên sâu] THIẾT KẾ VẬN HÀNH SCRUM CHO TÍNH NĂNG ĐẶT XE GHÉP

## Phần 1 - Phân tích

### 1.1. Đầu vào và Đầu ra của một Sprint

*   **Đầu vào của một Sprint:**
    *   **Product Backlog đã được sắp xếp ưu tiên:** Danh sách các hạng mục công việc (Product Backlog Items - PBIs) tiềm năng cho sản phẩm, được Product Owner ưu tiên theo giá trị kinh doanh và chiến lược.
    *   **Product Increment mới nhất:** Sản phẩm tăng trưởng có khả năng phát hành được từ Sprint trước đó.
    *   **Đội ngũ Developers:** Với năng lực, kinh nghiệm và cam kết thực hiện công việc.
    *   **Definition of Done (DoD):** Tập hợp các tiêu chí và yêu cầu mà tất cả các PBIs phải đáp ứng để được coi là "Hoàn thành".
    *   **Sprint Goal:** Mục tiêu rõ ràng mà đội Developers cam kết đạt được trong Sprint đó, cung cấp hướng đi và sự tập trung.
*   **Đầu ra của một Sprint:**
    *   **Product Increment tiềm năng có thể phát hành:** Một phiên bản tăng trưởng mới của sản phẩm, đã đáp ứng DoD, có giá trị và có thể được trình diễn cho các bên liên quan để lấy phản hồi.
    *   **Product Backlog đã được cập nhật:** Các PBIs đã hoàn thành sẽ bị xóa khỏi Product Backlog. Các PBI còn lại có thể được điều chỉnh, thêm mới hoặc sắp xếp lại thứ tự ưu tiên dựa trên phản hồi, kinh nghiệm mới và sự thay đổi của thị trường.
    *   **Kinh nghiệm và kiến thức mới:** Các bài học kinh nghiệm về sản phẩm, quy trình và cách làm việc của đội, được chia sẻ và áp dụng để cải thiện trong các Sprint tiếp theo (thông qua Sprint Retrospective).

### 1.2. Độ dài Sprint và Số Sprint

*   **Độ dài Sprint được chọn:** 2 tuần.
*   **Số Sprint trong 6 tuần:** 3 Sprints (6 tuần / 2 tuần = 3 Sprints).
*   **Lý do lựa chọn độ dài Sprint (gắn với trụ cột Scrum):**
    Việc chọn độ dài Sprint 2 tuần gắn liền chặt chẽ với các trụ cột của Scrum là **Minh bạch (Transparency)** và **Kiểm tra (Inspection)**, từ đó thúc đẩy **Thích nghi (Adaptation)**.
    *   **Minh bạch:** Chu kỳ 2 tuần cho phép người dùng thử được xem bản chạy được (Product Increment) sau mỗi Sprint. Điều này tạo ra sự minh bạch cao về tiến độ và chất lượng sản phẩm, giúp các bên liên quan dễ dàng nắm bắt hiện trạng.
    *   **Kiểm tra:** Khoảng thời gian 2 tuần cung cấp cơ hội thường xuyên để kiểm tra Product Increment và hiệu suất làm việc của đội thông qua Sprint Review. Phản hồi sớm từ người dùng thử và các bên liên quan giúp đội kiểm tra và đánh giá lại hướng đi của sản phẩm một cách kịp thời.
    *   **Thích nghi:** Nhờ việc kiểm tra và thu thập phản hồi thường xuyên, đội có thể nhanh chóng thích nghi và điều chỉnh kế hoạch ở mỗi Sprint Planning tiếp theo, đảm bảo sản phẩm luôn đi đúng hướng và phù hợp với yêu cầu thay đổi, đúng với tinh thần "Phản hồi với thay đổi hơn bám sát kế hoạch" của Agile. Độ dài này là sự cân bằng tốt giữa việc có đủ thời gian để hoàn thành các hạng mục có giá trị và cung cấp phản hồi đủ thường xuyên để đưa ra các quyết định sáng suốt.

## Phần 2 - Thiết kế Product Backlog

Dựa trên 4 nhu cầu thô từ khách hàng, Product Owner (Đức) sẽ sắp xếp thành Product Backlog theo thứ tự ưu tiên dựa trên giá trị cốt lõi của tính năng "đặt xe ghép" cho lần ra mắt đầu tiên. 

| Thứ tự ưu tiên | Hạng mục Product Backlog (Nhu cầu thô)               | Lý do                                                                                                                                                                                                                                                                                              |
| :-------------- | :---------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1               | (a) Ghép khách đi cùng tuyến đường vào một chuyến.    | Đây là giá trị cốt lõi và định nghĩa trực tiếp tính năng "đặt xe ghép". Không có tính năng này, sản phẩm không thể thực hiện chức năng chính. Đây là nền tảng bắt buộc để có thể ra mắt Phiên bản sản phẩm tối thiểu (MVP) có giá trị.                                                                                                                                                                                                                                                                                                                                                                                           |
| 2               | (b) Tự động chia tiền cho từng khách trong chuyến.     | Tính năng này hoàn thiện giá trị của việc đi ghép bằng cách tự động hóa và minh bạch hóa việc chia sẻ chi phí, là một phần không thể thiếu của trải nghiệm "chia tiền" khi đi chung xe. Nó giúp loại bỏ rắc rối cho người dùng và thúc đẩy việc sử dụng xe ghép.                                                                                                                                                                                                                                                                                                                                                                                                 |
| 3               | (c) Thanh toán bằng thẻ ngân hàng.                  | Cung cấp một phương thức thanh toán cơ bản và phổ biến, cho phép người dùng hoàn tất giao dịch và hệ thống có thể tạo ra doanh thu. Một phương thức thanh toán khả dụng là bắt buộc để tính năng có thể vận hành hiệu quả.                                                                                                                                                                                                                                                                                                                                                                                           |
| 4               | (d) Khách đánh giá bạn đi ghép sau mỗi chuyến.       | Tính năng này nâng cao chất lượng dịch vụ và xây dựng lòng tin cộng đồng nhưng không phải là yếu tố cốt lõi để ra mắt tính năng đặt xe ghép lần đầu. Nó có thể được xem xét và ưu tiên trong các Sprint tiếp theo hoặc các giai đoạn phát triển sau này để cải thiện và mở rộng sản phẩm.                                                                                                                                                                                                                                                                                                                                                                 |

*Ghi chú:* Đối với 3 Sprint trong 6 tuần đầu tiên, đội sẽ tập trung phát triển các hạng mục có độ ưu tiên 1, 2 và 3 để đảm bảo một sản phẩm có thể hoạt động được với giá trị cốt lõi và khả năng thu hút người dùng ban đầu.

## Phần 3 - Xử lý thay đổi

Khi có yêu cầu ưu tiên thanh toán qua ví điện tử trước thẻ ngân hàng vào giữa Sprint 2, đội RikkeiGo sẽ xử lý như sau:

*   **Ai quyết định:** Product Owner (Đức) là người duy nhất có thẩm quyền và trách nhiệm trong việc quản lý, sắp xếp lại thứ tự ưu tiên của Product Backlog. Anh ấy sẽ tiếp nhận phản hồi từ khách hàng, đánh giá giá trị kinh doanh của yêu cầu mới và quyết định vị trí của hạng mục "Thanh toán qua ví điện tử" trong Product Backlog.
*   **Đưa vào đâu:** Yêu cầu "Thanh toán qua ví điện tử" sẽ được thêm vào Product Backlog dưới dạng một hạng mục mới. Product Owner sẽ xem xét và sắp xếp lại thứ tự ưu tiên của các hạng mục liên quan đến thanh toán (ví dụ: có thể đẩy "Thanh toán qua ví điện tử" lên cao hơn "Thanh toán bằng thẻ ngân hàng" nếu đánh giá giá trị cho khách hàng là lớn hơn).
*   **Áp dụng từ khi nào:** Thay đổi về thứ tự ưu tiên này sẽ được xem xét và đưa vào kế hoạch làm việc từ **Sprint Planning của Sprint kế tiếp (Sprint 3)**. Sprint đang chạy (Sprint 2) sẽ không bị gián đoạn để đảm bảo sự ổn định và tập trung của đội Developers vào Sprint Goal đã cam kết. Điều này tuân thủ nguyên tắc "thích nghi với thay đổi" của Agile mà vẫn bảo vệ tính ổn định của Sprint hiện tại và sự tập trung của đội.