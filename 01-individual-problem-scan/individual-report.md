# Phase 1 — Individual Scan: Tìm kiếm và phân tích các vấn đề

**Họ và tên:** Đỗ Nhật Minh
**Mã sinh viên:** 2A2002601085 
**Nhóm:** A4  
**Ngày:** 27/07/2026
## Scan rộng

Minh scan 7 problems dựa trên thực tế khóa học dài ngày và tình trạng thiếu hụt nhân sự hỗ trợ.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Học viên kẹt ở bước cài đặt môi trường, gặp nhiều lỗi vặt nhưng TA quá tải không hỗ trợ kịp. | Học viên mới, TA | TA phải lặp lại cùng một hướng dẫn nhiều lần; học viên mất 1-2 tiếng chờ đợi chỉ để fix 1 lỗi nhỏ. |
| 2 | Lặp lại | Học viên liên tục hỏi lại các vấn đề về quy định điểm danh, nội quy của khóa học dù đã có thông báo. | Ban tổ chức, TA | Cùng một câu hỏi về nội quy/điểm danh xuất hiện hàng ngày trên các group chat khác nhau. |
| 3 | Pain từ người khác | Học viên bị trôi/lỡ thông báo quan trọng do khóa học sử dụng quá nhiều kênh giao tiếp (Discord, Zalo, Outlook, Teams). | Học viên, Ban tổ chức | Học viên hỏi lại thông tin đã gửi; nộp bài trễ deadline do không thấy thông báo. |
| 4 | AI có thể tốt hơn | TA không thể quan sát và cộng điểm kịp thời cho tất cả các bạn giơ tay hoặc chat trả lời trên Discord cùng một lúc. | TA, Học viên tích cực | TA mất 20-30 phút sau buổi học để dò lại log chat; học viên phàn nàn vì bị sót điểm tương tác. |
| 5 | Tốn thời gian | Học viên không nhận được feedback chi tiết và kịp thời cho bài tập do lượng bài lớn mà số lượng TA thì mỏng. | Học viên, TA | TA mất quá 1 tuần để trả bài; feedback thường dùng template chung chung; học viên lặp lại lỗi sai cũ. |
| 6 | AI có thể tốt hơn | Học viên tụt động lực và rớt nhịp giữa khóa nhưng không có công cụ phát hiện sớm để đốc thúc, động viên. | Học viên, Ban tổ chức | Tỷ lệ nộp bài giảm mạnh ở giữa khóa; nhiều học viên "ghost" (im lặng biến mất) mà BTC không biết lý do. |
| 7 | Pain từ người khác | Tình trạng "gánh team" khi làm dự án nhóm do thiếu sự giám sát tiến độ và mức độ đóng góp của từng cá nhân trong quá trình làm. | Học viên tích cực | Có sự bức xúc nội bộ khi đánh giá chéo; 1-2 người ôm 80% khối lượng code/việc của nhóm 5 người. |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Cộng điểm tương tác (Ca #4) | Workflow cực rõ (Export log chat/Zoom → Dò tên → Đếm điểm). Có baseline thời gian đo được ngay (TA mất 20-30 phút/buổi). AI rất giỏi bóc tách dữ liệu và map tên từ text lộn xộn. | AI có hiểu sai ngữ cảnh chat (ví dụ: học viên chat đùa thay vì trả lời bài) hoặc nhận diện sai tên (gõ không dấu, nick name) không? |
| 2 | Hỗ trợ cài đặt môi trường (Ca #1) | Nỗi đau cực lớn ở tuần đầu (onboarding), là nguyên nhân chính khiến học viên nản sớm. Log lỗi code thường là text rõ ràng, AI đọc và hiểu context lỗi rất tốt. | Biến số môi trường máy cá nhân quá đa dạng (Mac, Win, version cũ mới). Giải pháp dễ biến thành một chatbot "search Google hộ" nếu không thiết kế luồng workflow cẩn thận. |
| 3 | Trả lời nội quy/điểm danh (Ca #2) | Tính lặp lại cực cao hằng ngày. Nguồn dữ liệu (Rule/Document) đã có sẵn, được kiểm soát và cố định. | Scope có thể quá nhỏ, dễ bị giải quyết bằng "Rule-based bot" thông thường thay vì một Workflow AI đúng nghĩa. |

### Vì sao các ca còn lại bị loại khỏi Top 3?

- **Ca #5 (Chấm bài/Feedback):** Mặc dù nỗi đau lớn, nhưng metric "chất lượng feedback" rất khó đo lường khách quan. Rủi ro AI "hallucination" (bịa ra kiến thức) khuyên sai chuyên môn là rủi ro chí mạng không đáng đánh đổi.
- **Ca #3 (Nhiều kênh giao tiếp):** Nỗi đau này thiên về quy trình quản trị (Management) hơn là AI. Giải pháp triệt để là quy định lại chuẩn giao tiếp (vd: gộp mọi thứ về Slack/Discord), thay vì dùng AI để đi gom tin nhắn rác.
- **Ca #6 (Rớt nhịp) & Ca #7 (Gánh team):** Thiếu dữ liệu đầu vào khách quan. AI không thể đánh giá "động lực" hay "thái độ" nếu không có hệ thống log chi tiết của từng cá nhân. Làm ca này dễ rơi vào "bánh vẽ" vì không có data để chạy.

## Problem Card #1 (TOP1)— Chấm và cộng điểm tương tác tự động

**Problem 1 câu:** TA mất rất nhiều thời gian thủ công để rà soát hàng trăm dòng log chat (Zoom/Discord) nhằm ghi nhận điểm phát biểu cho học viên sau mỗi buổi học, dẫn đến việc cập nhật điểm chậm trễ và dễ bị sai sót/bỏ lọt.

**Actor:** Trợ giảng (TA) phụ trách vận hành và chấm điểm, cùng các Học viên tích cực tham gia phát biểu.

**Thời điểm / bối cảnh:** Sau khi kết thúc mỗi buổi học live (Zoom/Teams) hoặc cuối ngày đối với các hoạt động giải bài trên kênh Discord chung.

**Current workflow:**
1. Kết thúc buổi học, TA tải file log chat thô từ Zoom hoặc export từ Discord.
2. Mở file log text và mở file Google Sheets quản lý điểm.
3. Đọc dò tay từng dòng chat để phân loại (đâu là chat chào hỏi/xin phép, đâu là câu trả lời đúng nội dung bài).
4. Đối chiếu tên hiển thị trên ứng dụng chat với tên thật/mã số trong danh sách lớp.
5. Cập nhật số điểm (+) tương ứng vào cột Google Sheets.
6. Đăng thông báo tổng kết điểm lên group lớp.
7. Xử lý khiếu nại nếu học viên nhắn tin báo bị sót điểm.

**Bottleneck:** Bước 3 và 4 — Đọc lọc nội dung từ file log dài hàng trăm dòng và việc đối chiếu tên (do học viên hay để nickname, viết không dấu, viết tắt) cực kỳ tốn sức, mỏi mắt và tốn thời gian.

**Impact:** TA mất khoảng 30-45 phút sau mỗi buổi học chỉ để làm công việc copy-paste và đếm thủ công này. Học viên đôi khi bức xúc vì đóng góp nhưng bị sót tên và phải mất công đi khiếu nại.

**Success metric:** Giảm thời gian tổng hợp điểm từ 30-45 phút xuống dưới 5 phút/buổi. Tỷ lệ học viên khiếu nại sót điểm giảm xuống dưới 5% mỗi tuần.

**Non-AI alternative:** Dùng các tool dạng Quiz (như Slido, Kahoot) để tự thống kê điểm thay vì dùng chat, hoặc yêu cầu học viên đổi tên hiển thị chuẩn cú pháp `[Mã HV] - Tên` kết hợp với viết script RegEx để lọc text. Tuy nhiên, cách này làm mất đi tính tương tác tự nhiên, thảo luận mở của lớp học và script dễ lỗi nếu học viên gõ sai cú pháp.

**AI hypothesis:** TA đẩy toàn bộ file log chat thô cùng danh sách lớp và "đáp án đúng/từ khóa mong muốn" vào một prompt. AI sẽ đóng vai trò cấu trúc dữ liệu: tự động lọc bỏ chat rác, đánh giá câu trả lời hợp lệ, map đúng nickname với tên thật trong danh sách, và trả ra một bảng tổng hợp gọn gàng (Tên - Số lần phát biểu hợp lệ). TA chỉ cần đối chiếu nhanh và dán vào Sheets.

**Quick gut:** Workflow.

### Draft current workflow

```text
CURRENT STATE — Khoảng 45 phút

[1 Tải file log chat: 2']
→ [2 Mở song song log và bảng điểm Sheets: 2']
→ [3 Đọc từng dòng lọc câu trả lời đúng: 15'] <-- bottleneck 1
→ [4 Dò nickname chat với tên thật trong danh sách: 15'] <-- bottleneck 2
→ [5 Nhập điểm vào Sheets: 5']
→ [6 Đăng thông báo: 2']
→ [7 Check tin nhắn và sửa điểm nếu sót: 4']

FUTURE STATE — Khoảng 8 phút

[1 Tải file log chat: 2']
→ [2 Nạp log chat + Danh sách lớp + Đáp án vào prompt: 1']
→ [3 AI bóc tách, map tên và đếm số lần hợp lệ: 1']
→ [4 TA review lướt qua bảng kết quả của AI: 2'] <-- human boundary
→ [5 TA copy bảng kết quả dán vào Sheets: 1']
→ [6 Đăng thông báo: 1']

Fallback: AI map tên sai (do 2 bạn có nickname quá giống nhau) → TA tự dò lại bằng lệnh Ctrl+F cho trường hợp cụ thể đó.
Bottleneck mới: TA phải chuẩn bị đáp án/từ khóa đúng tóm tắt từ buổi học để cung cấp cho AI làm cơ sở chấm điểm.
```
## Problem Card #2 — Hỗ trợ cài đặt môi trường và sửa lỗi Lab

**Problem 1 câu:** Học viên mất rất nhiều thời gian (thường 1-2 tiếng) kẹt ở các lỗi cài đặt môi trường hoặc cấu hình lặt vặt trong Lab do tự mò mẫm sai cách và phải chờ đợi TA phản hồi, làm ảnh hưởng nghiêm trọng đến động lực và tiến độ học.

**Actor:** Học viên (đặc biệt là người mới/chuyển ngành) và Trợ giảng (TA) phụ trách giải đáp.

**Thời điểm / bối cảnh:** Trong các buổi tự làm Lab ở nhà hoặc những tuần đầu tiên (onboarding) khi phải cài đặt công cụ, framework mới.

**Current workflow:**

```text
1. Học viên chạy lệnh/code theo tài liệu hướng dẫn.
2. Màn hình báo lỗi (Terminal/IDE).
3. Học viên tự Google lúng túng nhưng không biết chọn cách sửa nào.
4. Chụp ảnh màn hình lỗi gửi lên kênh Discord hỏi TA.
5. Chờ TA rảnh để đọc tin nhắn.
6. TA hỏi ngược lại để lấy thêm bối cảnh (Dùng Win/Mac? Version bao nhiêu? Copy text log ra sao?).
7. Học viên cung cấp thêm thông tin.
8. TA đưa ra giải pháp step-by-step.
9. Học viên làm theo và sửa được lỗi.

```

**Bottleneck:** Bước 5 và 6 — Thời gian chờ đợi TA rảnh để tiếp nhận ca hỗ trợ và quá trình nhắn tin qua lại (ping-pong) để làm rõ bối cảnh máy tốn rất nhiều thời gian, có thể lên tới hàng giờ nếu hỏi vào ban đêm.

**Impact:** Học viên mất từ 1-2 tiếng chỉ để vượt qua 1 lỗi setup cơ bản, gây ức chế tinh thần. TA mất trung bình 15-20 phút nhắn tin hoặc call 1-1 cho từng ca, dẫn đến quá tải và không còn băng thông để hỗ trợ các bài tập có tư duy logic sâu hơn.

**Success metric:** Giảm thời gian từ lúc phát sinh lỗi đến lúc có hướng dẫn sửa lỗi cụ thể từ mức >60 phút xuống dưới 5 phút. Giảm ít nhất 60% số lượng câu hỏi về lỗi setup/config cơ bản đẩy lên kênh Discord chung.

**Non-AI alternative:** Cung cấp file cài đặt tự động (Bash script, Docker) hoặc một file FAQ/Troubleshooting dài 20 trang tổng hợp sẵn các lỗi. Tuy nhiên, script tự động vẫn thường xuyên vỡ do biến số môi trường máy cá nhân quá đa dạng, và học viên thường lười hoặc không biết cách tra cứu đúng từ khóa trong file FAQ.

**AI hypothesis:** Học viên sử dụng một prompt chuẩn để cung cấp log lỗi thô và thông tin hệ điều hành. AI đối chiếu thông tin này với bộ tài liệu Lab/FAQ chuẩn của ban tổ chức để chẩn đoán nguyên nhân và tự động draft hướng dẫn sửa lỗi (step-by-step). Học viên tự làm theo hướng dẫn này. TA chỉ can thiệp khi AI không giải quyết được.

**Quick gut:** Workflow.

### Draft current workflow

```text
CURRENT STATE — Khoảng 90 phút (tính cả thời gian chờ)

[1 Chạy cài đặt bị lỗi: 5']
→ [2 Tự mò mẫm Google thử sai: 20']
→ [3 Chụp ảnh gửi Discord: 5']
→ [4 Chờ TA phản hồi: 40']  <-- bottleneck 1
→ [5 Giao tiếp ping-pong lấy bối cảnh máy: 10'] <-- bottleneck 2
→ [6 TA đưa giải pháp: 5']
→ [7 Học viên làm theo và fix xong: 5']

```

### Draft future workflow

```text
FUTURE STATE — Khoảng 12 phút

[1 Chạy cài đặt bị lỗi: 2']
→ [2 Học viên paste text log lỗi + HĐH vào prompt chuẩn: 2']
→ [3 AI đối chiếu tài liệu & draft cách sửa (step-by-step): 1']
→ [4 Học viên làm theo hướng dẫn AI: 5'] <-- human boundary
→ [5 Fix xong và tiếp tục học: 2']
```
Fallback:
Nếu làm theo AI 2 lần không được → Học viên forward toàn bộ log chat với AI cho TA để TA xử lý tiếp (TA có sẵn toàn bộ bối cảnh, không cần hỏi lại từ đầu).

Bottleneck mới:
Học viên phải biết cách copy toàn bộ text log lỗi thay vì chỉ chụp màn hình (screenshot). Đây là thói quen cần rèn luyện nhưng hoàn toàn có thể hướng dẫn được bằng rule từ đầu khóa.


## Problem Card #3 — Giải đáp tự động quy định và nội quy khóa học

**Problem 1 câu:** Học viên liên tục hỏi đi hỏi lại những câu hỏi giống nhau về nội quy, điểm danh, lịch học trên group chat chung khiến TA mất nhiều thời gian trả lời lặp lại, đồng thời làm trôi các tin nhắn học thuật quan trọng.

**Actor:** Học viên (thường lười tìm kiếm hoặc quên thông tin lưu trữ), Trợ giảng (TA) và Ban tổ chức (BTC).

**Thời điểm / bối cảnh:** Xảy ra rải rác hằng ngày trên các kênh giao tiếp (Discord, Zalo), bùng nổ nhất là trước các buổi học, trước hạn nộp bài, hoặc khi có sự kiện đặc biệt.

**Current workflow:**

```text
1. BTC đã gửi file nội quy/Syllabus từ đầu khóa.
2. Học viên quên hoặc lười tìm lại link file.
3. Học viên nhắn thẳng lên group chat (VD: "Tối nay điểm danh ở link nào ạ?", "Nghỉ 2 buổi có được thi cuối kỳ không?").
4. Chờ TA rảnh để đọc tin nhắn.
5. TA phải đi lục lại link tài liệu hoặc tự gõ lại câu trả lời theo trí nhớ.
6. TA tag tên học viên để trả lời.

```

**Bottleneck:** Bước 4, 5 và 6 — Công việc lặp lại nhàm chán (copy-paste câu trả lời cũ), tốn công sức của TA và gây nhiễu luồng thông tin chung của lớp học.

**Impact:** TA bị phân tâm, mất trung bình 15-20 phút mỗi ngày chỉ để "làm tổng đài viên" trả lời những thứ đã có sẵn trong tài liệu. Group chat bị loãng, học viên khác dễ bị miss các thông báo quan trọng.

**Success metric:** Giảm 80% thời gian TA phải trực tiếp trả lời các câu hỏi về vận hành/nội quy. Thời gian chờ phản hồi của học viên giảm từ 15-30 phút xuống dưới 1 phút.

**Non-AI alternative:** Gim (Pin) tin nhắn quan trọng, tạo file FAQ chung, hoặc dùng các Chatbot Rule-based (nhấn phím 1 để xem lịch học, phím 2 để xem điểm danh). Tuy nhiên, học viên lười đọc file FAQ, và bot rule-based rất cứng nhắc, không hiểu được câu hỏi tự nhiên (Ví dụ hỏi: "Hôm nay em ốm không đi học được thì phải báo ai?").

**AI hypothesis:** Xây dựng một AI FAQ Assistant (có thể tích hợp trực tiếp vào Discord) được nạp (RAG) toàn bộ tài liệu vận hành, Syllabus, và nội quy. Khi có người hỏi, AI tự động phân tích ý định, trích xuất đúng quy định và trả lời ngay lập tức, kèm theo trích dẫn nguồn. TA không cần can thiệp trừ khi AI báo lỗi hoặc không có dữ liệu.

**Quick gut:** Workflow.

### Draft current workflow

```text
CURRENT STATE — Khoảng 23 phút

[1 Học viên quên thông tin & nhắn hỏi lên group: 2']
→ [2 Chờ TA rảnh để đọc tin nhắn: 15'] <-- bottleneck 1
→ [3 TA nhớ lại hoặc đi tìm lại link quy định: 4'] <-- bottleneck 2
→ [4 TA gõ câu trả lời, tag tên gửi lên group: 2']

```

### Draft future workflow

```text
FUTURE STATE — Khoảng 2 phút

[1 Học viên tag tên Bot AI hỏi trên group: 1']
→ [2 AI đối chiếu Knowledge Base (Nội quy) và sinh câu trả lời: 1']
→ [3 Học viên nhận được đáp án ngay lập tức: 0'] <-- auto step
```

Fallback: AI gặp câu hỏi ngoài rìa (VD: "Hôm nay thầy giáo có vui không?") → Trả lời không biết và tự động tag TA vào hỗ trợ.
Bottleneck mới: BTC phải cập nhật nội quy (Knowledge Base) liên tục cho AI mỗi khi có thay đổi lịch học, nếu không AI sẽ cung cấp thông tin sai (Outdated).

