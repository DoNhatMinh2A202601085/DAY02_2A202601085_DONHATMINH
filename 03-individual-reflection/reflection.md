# Phase 7 — Individual Reflection
**Họ và tên:** Đỗ Nhật Minh
**Mã sinh viên:** 2A2002601085 
**Nhóm:** A4  
**Ngày:** 27/07/2026
## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Đưa ra các bài toán liên quan đến vận hành, giảm tải cho Trợ giảng (TA). | Giúp nhóm không bỏ quên góc nhìn của người quản trị lớp học. |
| Pitch Problem Card | Trình bày bài "Chấm và cộng điểm tương tác". | Bị nhóm phản biện và rút ra được bài học về Rule. |
| Challenge bài của bạn khác | Đặt câu hỏi phản biện cho các bài toán CSKH và Discord về workflow, quality criteria và khả năng triển khai. | Giúp nhóm làm rõ actor, bottleneck và phạm vi của các bài toán trước khi lựa chọn. |
| Gom trùng / cluster | Tham gia phản biện và thu hẹp phạm vi các problem được thảo luận. | Các problem được làm rõ hơn về workflow và actor. |
| Chọn candidate problem | Tham gia thống nhất chọn bài Discord bị ngập bài chia sẻ làm candidate. | Thống nhất hướng đi chung. |
| Validation / research | Tham gia validation bằng cách đặt câu hỏi về tiêu chí chất lượng bài viết và khả năng triển khai. | Giúp nhóm xác định rõ các giả định cần kiểm chứng. |
| Workflow nhóm | Rà soát workflow và bottleneck của các bài toán được chọn. | Đảm bảo tính thực tế trong tương tác người-máy. |
| Problem Statement | Hỗ trợ làm rõ Actor, Pain Point và Impact. | Làm nổi bật "nỗi đau" từ góc nhìn quản lý giáo dục. |
| Rule / Workflow / Agent | Đặt câu hỏi về tiêu chí AI phân loại bài viết, khả năng xử lý lượng dữ liệu lớn và giới hạn của hệ thống. | Tiết kiệm chi phí vận hành (hidden cost) cho TA. |
| Decision | Tham gia thống nhất lựa chọn hướng Workflow thay vì Agent. | Giúp làm rõ phạm vi triển khai phù hợp với bài toán. |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Ném các ý tưởng thô về nỗi đau của TA vào Gemini nhờ gợi ý thêm và format thành bảng 4 lăng kính. | Cấu trúc bảng rất nhanh, chỉ ra được tiêu chí "Tốn thời gian" và "Lặp lại" khá rõ ràng. | AI tự quét ra vài vấn đề không có trải nghiệm thực tế (như quản lý tài chính sinh viên). | Bỏ qua hoàn toàn các ý bịa đặt. Chỉ giữ lại đúng bài toán chấm điểm và FAQ vì đó là nỗi đau thật của tôi. |
| **Problem Card** | Nhờ AI đóng vai "Skeptical PM" phản biện thẻ vấn đề với prompt: *"Chỉ ra điểm yếu, đừng khen"*. | Rất sắc bén. AI chỉ thẳng mặt bài "Chấm điểm tương tác" của tôi là lấy dao mổ trâu giết gà, có thể fix bằng Excel/Rule. | Đôi lúc AI bắt bẻ quá tiểu tiết về định nghĩa Actor. | Tôi công nhận AI phản biện đúng. Dùng các phản biện để hoàn thiện Problem Card và xác định rõ giới hạn của giải pháp AI. |
| **Workflow** | Cung cấp luồng các bước bằng text thô, nhờ AI sinh mã Mermaid và ép vào bảng Input/Output. | Lên hình sơ đồ (Mermaid) cực nhanh, đẹp và đúng chuẩn cú pháp. | AI bị nhầm timeline, nhét luôn bước Socratic AI vào "Current Workflow". | Tôi phải bắt AI tách bạch lại rạch ròi. Tư duy quy trình (hiện tại vs tương lai) là do tôi tự chốt, AI chỉ làm thợ vẽ. |
| **Research** | Dùng AI hỗ trợ tìm các hướng triển khai Workflow và gợi ý câu hỏi validation. | AI giúp tổng hợp các hướng tiếp cận và tiêu chí đánh giá. | AI đôi khi đưa ra các giả định về hiệu quả mà chưa có bằng chứng. | Chỉ giữ lại các nhận định phù hợp với dữ liệu và thảo luận của nhóm. |
| **Problem Statement** | Ném toàn bộ thảo luận của nhóm cho AI rà soát lỗi logic trong 6 field của bảng PS v0. | Chỉ ra sự nhầm lẫn tai hại của nhóm giữa Impact (hậu quả hiện tại) và Goal (mục tiêu). | Khi nhờ gợi ý Metric, AI toàn đề xuất các Metric viển vông (100% sinh viên hiểu bài). | Tự sửa lại thành các metric đo thời gian xử lý, độ chính xác phân loại và khả năng mở rộng phù hợp với bài toán. |
| **Rule / Workflow / Agent** | Hỏi AI so sánh sự khác biệt giữa Rule, Workflow và Agent cho bài toán Discord. | Giải thích rất dễ hiểu: Workflow phù hợp hơn vì vẫn giữ human-in-the-loop. | AI có xu hướng ưu tiên Agent dù chưa cần thiết. | Tuyệt đối không để AI quyết định thay. Giữ quan điểm chọn Workflow vì phù hợp với workflow thực tế và dễ kiểm soát. |
| **Decision** | (Không dùng AI) | - | - | Tự dựa vào các tiêu chí Go/No-Go để thiết kế quy mô Pilot. |

## Reflection câu hỏi mở

- **Tôi học được gì khi nghe top 3 problems của các bạn khác?** Mình nhận ra Pain của học viên (kẹt lỗi code) lớn hơn và cần cấp bách hơn Pain của TA (chấm điểm thủ công). 
- **Nhóm có lúc nào bị solution-first không?** Có, lúc Hữu Đức gợi ý làm Agent xử lý FAQ. Đang mải bàn cách build RAG thì nhóm nhận ra bài FAQ không có workflow tuyến tính và rủi ro quá lớn.
- **Tôi có thay đổi ý kiến sau khi bị challenge không?** Có. Ban đầu tôi đánh giá cao bài "Chấm và cộng điểm tương tác", nhưng sau khi thảo luận tôi nhận ra bài Discord có phạm vi tác động rộng hơn nên đồng thuận với lựa chọn của nhóm.
- **Tôi đóng góp gì thật sự vào artifact cuối?** Đặt các câu hỏi phản biện về actor, workflow, bottleneck, tiêu chí chất lượng và khả năng triển khai giúp nhóm thu hẹp phạm vi bài toán.
- **Điều khó nhất khi viết Problem Statement là gì?** Xác định đúng bottleneck và tách biệt rõ giữa problem với solution.
- **Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?** Sẽ challenge nhiều hơn về metric, nguồn dữ liệu và tiêu chí đánh giá chất lượng của bài toán Discord.



