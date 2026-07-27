# Group Report — Day 02

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|--------------------|
| 1   | Trương Minh Hoàng | 2A202602004 |                    |
| 2   | Đỗ Nhật Minh | 2A202601085 |                    |
| 3   | Trần Đức Thiện | 2A202602032 |                    |
| 4   | Nguyễn Huy Anh | 2A202601641 |                    |
| 5   | Phạm Trung Kiên | 2A202601986 |                    |
| 6   | Lục Minh Đức | 2A202601918 |                    |
| 7   | Phan Hoàng Long | 2A202601565 |                    |
| 8   | Nguyễn Văn Đại | 2A202601217 |                    |
| 9   | Trần Quang Thành | 2A202601133 |                    |
| 10  | Hoàng Văn Phái | 2A202601575 |                    |
| 11  | Hà Tấn Phong | 2A202601577 |                    |
| 12  | Phạm Nguyên Việt | 2A202601547 |                    |
| 13  | Phạm Bá Thượng Hải | 2A202601797 |                    |


# Group Convergence

## Problem Cards from Individual Scans (1 per member)

| # | Problem Card | Problem 1 câu | Actor | Bottleneck | Impact | Success Metric | Quick Gut | AI Hypothesis |
|---|---|---|---|---|---|---|---|---|
| A | Đọc slide/tài liệu trước Assignment | Sinh viên mất 60–90 phút đọc slide/PDF dài trước mỗi assignment, dễ bỏ sót ý quan trọng | Sinh viên chuẩn bị làm assignment | Đọc hiểu và ghi chú tài liệu mất ~60 phút (bước 3–4) | Mỗi môn mất 60–90 phút; học nhiều môn → mất nhiều giờ, làm assignment sát deadline | Giảm từ 90p xuống < 30p, không bỏ sót nội dung quan trọng | Workflow | AI tóm tắt tài liệu, tạo checklist kiến thức, gợi ý phần cần đọc kỹ trước khi làm assignment |
| B | Kiểm tra bài nộp theo Rubric VinUni | Mỗi buổi lab mất 15–20p kiểm tra thủ công bài nộp trước push GitHub, đối chiếu Rubric bằng mắt tốn nhất, dễ bỏ sót | Học viên AI Thực chiến VinUni (Batch 02) | Bước 3: đọc & đối chiếu thủ công bài với Rubric ~10p, dễ quáng mắt, bỏ sót boundary/metric/fallback | 15–20p/buổi/người; lớp 30 người → 450–600p/buổi; rủi ro trừ 5–10% điểm | Giảm từ 20p xuống < 5p, 100% mục bắt buộc Rubric được quét đủ | Rule / Workflow | AI đọc file bài làm, đối chiếu Rubric VinUni, liệt kê mục chưa đạt/thiếu; học viên tự kiểm tra & chỉnh sửa |
| C | Rà soát lỗi bề mặt vỏ xe (CV) | Rà soát lỗi bề mặt (xước, nứt, sơn) bằng mắt thường tốn thời gian, dễ lọt lỗi do mỏi mắt | Kỹ sư QA/QC dây chuyền (EOL/sau xưởng sơn) | Rà soát & đánh dấu thủ công 3–5p/xe, phụ thuộc 100% sự tỉnh táo con người | Kéo dài takt-time cả dây chuyền; rủi ro lọt hàng lỗi ra thị trường | Giảm xuống < 1p/xe, tỷ lệ sót lỗi < 1% | Workflow | Camera độ phân giải cao + CV Image Segmentation → AI overlay đánh dấu khuyết tật lên ảnh gốc, QA chỉ duyệt xác nhận |
| D | CS trả lời ticket hỗ trợ lặp lại | Team CS mất 150–187p/ngày soạn reply ticket lặp lại, 60–70% đã có KB | 2 CS agents Intercom | Bước 3–4: switch Intercom↔Notion, tìm KB chậm, rewrite context user 5–10p/ticket | 2 CS × 12–13 ticket/ngày × 7.5p = 150–187p/ngày; FRT 15–20p (mong < 5p) → churn, NPS giảm | Xử lý ticket lặp 7.5p → 2–3p; FRT 15p → < 5p; CSAT 4.0 → ≥ 4.2/5 | Workflow | AI đọc ticket + tìm KB → draft reply context user → CS review/edit → gửi (AI không tự gửi) |
| E | Tìm chính sách cho ticket CSKH lặp lại | CSKH mất thời gian tìm câu trả lời chính sách lặp lại do info rải rác nhiều doc/chat, bản cũ/new song song | Nhân viên CSKH helpdesk/chat/email | Bước 2–3: tìm chính sách do tài liệu rải rác, không có tra cứu tập trung, bản cũ/new song song | 3–5p/ticket × 15–20 ticket/ngày/người = 1–1.5h/ngày/người; khách chờ lâu cho câu hỏi đơn giản | Giảm 3–5p → < 1p/ticket; không tăng tỷ lệ trả lời sai (QA review tuần) | Workflow | AI tìm đoạn chính sách liên quan + gợi ý draft trả lời theo ngữ cảnh; nhân viên đọc & chỉnh trước khi gửi |
| F | Cài đặt môi trường AI / CV | Cài môi trường & xử lý lỗi dependency mất nhiều giờ trước khi làm dự án AI/CV mới | Sinh viên AI/CNTT, người mới học CV, Kỹ sư AI mới | Xung đột Python version, thiếu thư viện/sai version, README thiếu, mỗi project cách cài khác; sửa lỗi > thời gian học | 2–6h/mỗi project mới; gặp hầu hết dự án AI | Giảm 2–6h → < 30p; tỷ lệ chạy thành công lần 1 > 90% | Workflow | AI đọc README, phân tích lỗi, đề xuất lệnh cài đặt & hướng dẫn xử lý sự cố tự động hóa setup |
| G | Quản lý chi tiêu ngân hàng cuối tháng | Mỗi tháng mất 20–30p cộng chi tiêu từ ngân hàng/ví/tiền mặt, đối chiếu giao dịch lạ, hay bỏ sót khoản nhỏ | Sinh viên tự quản lý chi tiêu cá nhân | Bước 2–3: dữ liệu rải rác nhiều app, gộp thủ công, bỏ sót < 50k; chiếm ~15p | Không kiểm soát ngân sách, chi vượt mức không biết tới cuối tháng | Giảm 20–30p → < 10p/tháng; khoản chi không rõ nguồn gốc → ~0 | Rule / Workflow | AI đọc/tổng hợp lịch sử giao dịch (export/kết nối), tự phân loại nhóm chi tiêu, cảnh báo bất thường; user xác nhận cuối |
| H | Check Discord sau 1 đêm (Daily Digest) | Mỗi sáng mất ~30p check kênh chia sẻ Discord, scroll đọc bài farm chất lượng thấp để tìm bài hay | Học viên chương trình đào tạo | Phải đọc qua nhiều bài farm để tìm bài hữu ích; tỷ lệ hay/farm thấp | 30p/sáng; mất hứng thú, bỏ lỡ chia sẻ hay bị chìm trong bài farm | Giảm 30p → < 5p; tỷ lệ bài hữu ích được đọc tăng | Workflow / Agent | AI daily digest: phân loại bài, đánh giá chất lượng, tổng hợp top bài hữu ích, gửi digest sáng sớm |

## Shortlist & Score (3 Problem Cards from /problem folder)

| # | Problem Card | Actor | Bottleneck Clarity | Impact (Time/People) | AI Fit (Rule/WF/Agent) | Measurability | Feasibility | Discord Fit* | Total |
|---|--------------|-------|-------------------|---------------------|------------------------|---------------|-------------|--------------|-------|
| 1 | **Discord channel bị ngập bài farm điểm** | Học viên + Mentor | ★★★★★ Rất rõ: scroll đọc 20+ bài, mentor đọc chấm tất cả | ★★★★★ Hàng ngày, cả 2 phía đều mất thời gian lớn | ★★★★★ So sánh tốt Rule (notification/upvote) / Workflow (AI digest) / Agent (auto-filter) | ★★★★★ Time saved, quality ratio, mentor hours | ★★★★★ Dữ liệu Discord có sẵn, text-based | **Chosen** | **48/50** |
| 2 | Tìm chính sách CSKH lặp lại  | Nhân viên CSKH | ★★★★☆ Rõ: tìm doc rải rác, bản cũ/new song song | ★★★★☆ 1-1.5h/ngày/người, team lớn hơn = gấp nhiều lần | ★★★★☆ Workflow phù hợp, Rule (FAQ) có thể đủ 1 phần | ★★★★☆ Time/ticket, error rate | ★★★★☆ Cần tập hợp KB, có thể làm | - | 42/50 |
| 3 | Kiểm tra chất lượng bề mặt vỏ xe  | Kỹ sư QA/QC | ★★★★☆ Rõ: 3-5p/xe, mỏi mắt, phụ thuộc con người | ★★★★☆ Takt-time cả dây chuyền, rủi ro lọt lỗi ra thị trường | ★★★☆☆ Workflow (CV), Agent quá mức, Rule không đủ | ★★★★☆ Time/xe, defect escape rate | ★★★☆☆ Cần camera, infra CV, phức tạp hơn | - | 39/50 |

> **Discord Fit\*:** Criteria đặc thù cho bài tập này — bài toán dựa trên text/channel Discord, dữ liệu sẵn có, phù hợp so sánh 3 mức Rule/Workflow/Agent trong môi trường học tập.

### Decision: Chọn **Problem Card #1 — Discord channel bị ngập bài farm điểm** làm candidate để tiếp tục Quick Validation → Research → Workflow Before/After → Problem Statement v0/v1 → Rule/Workflow/Agent → Final Decision.

---

# Quick Validation (Discord Farm Problem)

| Câu hỏi validation | Câu trả lời / Bằng chứng |
|---|---|
| **Problem có thật không?** | Có. Kênh chia sẻ Discord chương trình đào tạo hằng ngày có hàng chục bài post. Cơ chế chấm điểm theo số lượng → incentive farm. Mentor phải đọc hết để chấm. Học viên lướt 20+ bài để tìm 1-2 bài hay. |
| **Ai chịu đau nhất?** | 1) Học viên: mất 30p/sáng lọc bài. 2) Mentor: đọc chấm tất cả bài (kể cả farm) → thời gian chấm tỷ lệ với số bài. |
| **Workflow hiện tại rõ ràng không?** | Rõ. Học viên: Mở Discord → scroll → đọc từng bài → đánh giá hữu ích → lưu. Mentor: Mở Discord → đọc từng bài → đánh giá chất lượng → cho điểm. Cả 2 đều tuyến tính, lặp lại. |
| **Bottleneck ở đâu?** | Bước "đọc & đánh giá từng bài". Tỷ lệ signal/noise thấp do farm. Không có bước lọc/độ ưu tiên trước khi đọc. |
| **Non-AI alternative đã thử chưa?** | - Thay đổi rubric chấm điểm (chất lượng > số lượng) — cần quy trình duyệt, chậm.<br>- Giới hạn bài/ngày — giảm volume nhưng không giải quyết bài farm vẫn lẫn vào.<br>- Reaction/upvote từ học viên — passive, không ai bấm đều, mentor vẫn phải đọc hết để chấm. |
| **AI có giải quyết được bottleneck không?** | Có. AI có thể: (1) Phân loại bài (farm vs chất lượng) dựa trên độ dài, cấu trúc, có ví dụ/code/link không. (2) Chấm điểm sơ bộ / ranking. (3) Tóm tắt hàng ngày (digest) top bài cho học viên. (4) Pre-screen cho mentor: flag bài farm, ưu tiên chấm bài chất lượng. |
| **Rủi ro lớn nhất?** | False positive: AI đánh giá sai bài hay thành farm (hoặc ngược lại) → mentor bỏ sót bài tốt / học viên bỏ lỡ bài hay trong digest. Cần human-in-the-loop. |
| **Data sẵn có?** | Có. Lịch sử message Discord (text, attachment, reaction, thread), rubric chấm điểm, log điểm cũ. Dễ thu thập để fine-tune / few-shot. |
| **Scope phù hợp bài tập?** | Phù hợp. Text-based, workflow rõ, so sánh được 3 mức Rule/Workflow/Agent, metric đo được, human boundary rõ ràng. |

---

# Research Giải Pháp (Discord Farm Problem)

| Mức độ | Giải pháp | Cơ chế | Ưu điểm | Nhược điểm | Khả thi |
|---|---|---|---|---|---|
| **Rule** | 1. Thay đổi rubric: chấm chất lượng, không chấm số lượng<br>2. Giới hạn 1 bài/ngày/người<br>3. Upvote/reaction từ học viên làm signal lọc | Thay đổi quy tắc chấm điểm / cấu hình channel | - Chi phí 0, triển khai ngay<br>- Giải quyết root cause (incentive) | - Cần consensus giảng viên/mentor<br>- Upvote passive, không đáng tin cậy<br>- Không giảm workload mentor ngay lập tức | ⭐⭐⭐⭐⭐ |
| **Workflow** | AI Daily Digest: <br>1. Mỗi sáng AI quét kênh → phân loại bài (farm/chất lượng)<br>2. Chấm điểm sơ bộ / ranking<br>3. Gửi digest: Top 5 bài hay + summary cho học viên<br>4. Mentor dashboard: flag bài farm, ưu tiên chấm bài quality | Human-in-the-loop: AI pre-process → Human review/decide | - Giữ nguyên rubric hiện tại<br>- Giảm thời gian cả 2 phía ngay<br>- Có fallback rõ ràng<br>- Dữ liệu text sẵn có | - Cần prompt engineering cho phân loại/chấm điểm<br>- False positive/negative cần monitor | ⭐⭐⭐⭐⭐ |
| **Agent** | Discord Bot tự động:<br>1. Listen event message mới<br>2. Phân loại real-time → gán label/thread<br>3. Tự reply reminder nếu bài quá ngắn/không có code/ví dụ<br>4. Tự tổng hợp digest hàng ngày post vào channel #daily-digest<br>5. Mentor chỉ xem channel digest | Fully automated loop: trigger → act → respond | - Real-time, không chờ sáng hôm sau<br>- Có thể can thiệp ngay lúc post (nudge quality) | - Rủi ro cao: bot reply sai → spam/annoy<br>- Cần quyền bot, infra chạy 24/7<br>- Overkill cho bài toán "lọc & tóm tắt" | ⭐⭐☆☆☆ |

---

# Workflow Before / After (Discord Farm Problem)

## CURRENT STATE — Học viên: ~30 phút/sáng | Mentor: ~X phút/ngày (tỷ lệ với số bài)

### Học viên
```text
[1 Mở Discord kênh chia sẻ: 1']
→ [2 Scroll lướt tiêu đề 20-30 bài: 5']
→ [3 Mở & đọc chi tiết từng bài: 20']  <-- BOTTLENECK
→ [4 Đánh giá hữu ích / lưu bài hay: 3']
→ [5 Đóng Discord, bắt đầu học: 1']
```

### Mentor
```text
[1 Mở Discord kênh chia sẻ: 1']
→ [2 Đọc từng bài chia sẻ: 15-30']  <-- BOTTLENECK (tỷ lệ với volume)
→ [3 Đánh giá chất lượng theo rubric: 10-20']
→ [4 Ghi điểm vào sheet/system: 5']
→ [5 Lặp lại cho bài tiếp theo]
```

---

## FUTURE STATE (Workflow - AI Daily Digest) — Học viên: ~5 phút | Mentor: ~50% thời gian

### Học viên (Daily Digest)
```text
[1 Nhận/đọc AI Digest (Top 5 bài hay + tóm tắt 1 câu): 3']
→ [2 Mở chi tiết 1-2 bài quan tâm: 2']  <-- HUMAN BOUNDARY
→ [3 Bắt đầu học: 0']
```
**Fallback:** Digest miss bài hay → Học viên vẫn có thể vào kênh gốc scroll thủ công.

### Mentor (Pre-screen Dashboard)
```text
[1 Mở Mentor Dashboard (AI pre-screened): 1']
→ [2 Xem bài đã flag "Quality" / "Priority": 5-10']
→ [3 Chấm điểm chi tiết chỉ bài quality: 5-10']  <-- HUMAN BOUNDARY
→ [4 Bài "Farm" đã pre-score thấp: 1' confirm/skip]
→ [5 Xuất điểm: 2']
```
**Fallback:** AI đánh giá sai → Mentor override, ghi feedback để retrain prompt.

---

# Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | (1) Học viên chương trình đào tạo AI — cần tìm chia sẻ hữu ích từ kênh Discord hàng ngày. (2) Mentor — cần đọc và chấm điểm các bài chia sẻ. |
| **Workflow** | Học viên: Mở Discord → scroll đọc tiêu đề → mở đọc chi tiết từng bài → đánh giá hữu ích → lưu bài hay. Mentor: Mở Discord → đọc từng bài → đánh giá chất lượng theo rubric → ghi điểm. |
| **Bottleneck** | Bước "đọc & đánh giá từng bài" lặp lại cho tất cả bài post. Tỷ lệ bài farm / bài chất lượng cao (~80/20 hoặc tệ hơn) khiến cả hai phía đều mất thời gian trên bài không có giá trị. Không có bước lọc/ưu tiên trước khi đọc. |
| **Impact** | Học viên: ~30 phút/sáng, mất hứng thú, bỏ lỡ bài hay. Mentor: Thời gian chấm điểm tỷ lệ thuận với tổng số bài (kể cả farm), công sức đọc bài chất lượng thấp không tạo ra giá trị. |
| **Success Metric** | Học viên: Giảm thời gian check Discord từ 30 phút xuống < 5 phút/ngày; Top 5 bài digest có ≥ 80% overlap với bài mentor chấm điểm cao. Mentor: Giảm thời gian chấm điểm ≥ 50%; Zero bài chất lượng cao bị miss (false negative < 5%). |
| **Boundary** | AI chỉ phân loại, chấm điểm sơ bộ, tóm tắt, gợi ý ưu tiên. **Không** tự động chấm điểm cuối cùng, **không** tự xóa/bảo quản bài, **không** tự reply/comment thay mentor/học viên. Human luôn là người quyết định cuối. |

---

# Rule / Workflow / Agent Decision Matrix

| Mức | Phương án cho bài toán Discord Farm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Thay đổi rubric chấm điểm (chất lượng > số lượng), giới hạn 1 bài/ngày/người, dùng reaction/upvote làm signal lọc | Đủ nếu incentive thay đổi khiến người học tự viết bài chất lượng, volume giảm tự nhiên, mentor đọc hết được | Cần consensus giảng viên, thời gian triển khai chính sách lâu, upvote passive không đáng tin cậy, mentor vẫn phải đọc hết trong giai đoạn chuyển đổi | **Không chọn làm chính** (cần làm nền tảng song song) |
| **Workflow** | AI Daily Digest + Mentor Pre-screen: AI quét kênh mỗi sáng → phân loại farm/quality → chấm điểm sơ bộ → ranking → gửi digest cho học viên + dashboard priority cho mentor. Human review/confirm cuối. | Phù hợp vì: workflow cố định (quét → phân loại → ranking → digest), không cần AI tự quyết định hành động tiếp theo, human boundary rõ (học viên chọn đọc gì, mentor chấm bài nào), fallback đơn giản | False positive/negative trong phân loại → học viên bỏ lỡ bài hay / mentor chấm nhầm priority. Cần monitor & retrain prompt. | **CHỌN** |
| **Agent** | Discord Bot tự động: listen real-time → phân loại → gán label/thread → nudge user viết bài tốt hơn (reply bot) → tự post digest → mentor chỉ xem digest | Chỉ cần nếu: muốn can thiệp real-time khi post, tự động nudge quality, scale lên nhiều channel/server, không cần human-in-the-loop cho bước phân loại | Rủi ro cao: bot reply sai → spam/annoy user, cần infra 24/7, quyền bot Discord, overkill cho bài toán "lọc & tóm tắt hàng ngày", human boundary bị mờ | **Không chọn** — bài toán không đủ phức tạp để cần agent tự điều phối |

**Mức chọn: Workflow**

**Vì sao:**
- Bài toán có quy trình cố định hàng ngày (quét → lọc → tổng hợp → gửi), không cần AI tự quyết định bước tiếp theo hay gọi nhiều tool khác nhau.
- Phần khó (phân loại farm vs quality, chấm điểm sơ bộ, tóm tắt) là việc AI ngôn ngữ làm tốt, nhưng vẫn cần human là người quyết định cuối (học viên chọn đọc, mentor chấm điểm) vì liên hệ trực tiếp đến điểm số và trải nghiệm học tập.
- Rule đơn thuần (rubric/upvote) không giải quyết được workload mentor ngay lập tức và không có cơ chế lọc chủ động.
- Agent là quá mức: không cần real-time nudge, không cần tự điều phối nhiều công cụ, rủi ro UX cao nếu bot reply sai.

---

# Problem Statement v1 (Refined after Rule/WF/Agent Analysis)

| Field | Nội dung cập nhật |
|---|---|
| **Actor** | Học viên (cần digest bài hay) & Mentor (cần priority queue chấm điểm). |
| **Workflow** | **AI Daily Digest Workflow:** Mỗi sáng 6:00 → AI fetch messages kênh chia sẻ hôm trước → Phân loại (Rule-based heuristic + LLM): Farm / Quality / Unsure → Chấm điểm sơ bộ theo rubric (0-10) → Ranking → Sinh Digest: Top 5 Quality + 1-sentence summary → Gửi DM/Channel #daily-digest cho học viên. Song song → Mentor Dashboard: danh sách bài đã pre-score, flag "Priority: Quality", "Review: Farm", "Unsure". Mentor chấm chi tiết bài Priority, confirm/skip Farm. |
| **Bottleneck** | Loại bỏ bước "đọc hết tất cả bài" cho cả 2 actor. Thay bằng "xem digest / chấm priority queue". |
| **Impact** | Học viên: 30p → 3-5p/ngày. Mentor: Giảm ≥ 50% thời gian chấm, focus vào bài tạo giá trị. |
| **Success Metric** | 1. Học viên time: < 5 phút/ngày đọc digest. 2. Digest Recall: ≥ 80% bài mentor chấm >7/10 nằm trong Top 5 digest. 3. Mentor time: -50% so với baseline. 4. False Negative Rate: < 5% (bài quality bị gán Farm). 5. False Positive Rate: < 15% (bài farm bị gán Quality — acceptable vì mentor sẽ skip nhanh). |
| **Boundary** | AI: Chỉ pre-score, phân loại, tóm tắt, ranking. **Không** ghi điểm chính thức, **không** xóa/bảo quản bài, **không** reply tự động. Mentor override = ground truth để cải thiện prompt. Human boundary: Học viên chọn đọc chi tiết bài nào; Mentor chấm điểm cuối cùng. |
| **Non-AI Baseline** | Rule-only: Chỉ dùng upvote/reaction + giới hạn bài/ngày. Baseline metric: Không giảm được mentor time, học viên vẫn phải scroll. |
| **AI Hypothesis** | LLM few-shot với rubric chấm điểm + ví dụ farm/quality → đạt ≥ 85% accuracy phân loại binary (farm vs quality) và correlation ≥ 0.7 với mentor score. Prompt versioning + weekly review false cases. |

---

# Final Decision

> **Chọn giải pháp: Workflow — AI Daily Digest + Mentor Pre-screen Dashboard**
>
> **Tóm tắt:** Xây dựng quy trình tự động hóa hàng ngày: AI quét kênh Discord chia sẻ → phân loại farm/quality theo rubric → chấm điểm sơ bộ → ranking → sinh Daily Digest (Top 5 bài hay + tóm tắt) gửi cho học viên + Priority Queue dashboard cho mentor. Human-in-the-loop tại 2 boundary: (1) Học viên quyết định đọc chi tiết bài nào từ digest, (2) Mentor chấm điểm chính thức và override AI pre-score.
>
> **Không chọn Rule** vì không giảm workload mentor ngay lập tức, cần thay đổi chính sách lâu dài.
>
> **Không chọn Agent** vì overkill, rủi ro UX (bot reply sai), infra phức tạp, bài toán không cần real-time autonomous action.
>
> **Next Steps (Implementation Plan):**
> 1. **Data Collection:** Export lịch sử 4-6 tuần message kênh chia sẻ + điểm mentor đã chấm (ground truth).
> 2. **Prompt Engineering:** Few-shot prompt với rubric + 20 ví dụ farm/quality đã gán nhãn. Thử nghiệm 3-4 model (GPT-4o-mini, Claude Haiku, local model).
> 3. **Evaluation:** Đo Accuracy, Precision/Recall (Farm vs Quality), Correlation (Spearman) với mentor score. Target: F1 > 0.85, ρ > 0.7.
> 4. **Prototype Digest:** Script Python + Discord Webhook gửi digest test cho 5 học viên + 2 mentor trong 1 tuần. Thu feedback.
> 5. **Mentor Dashboard:** Simple web UI (Streamlit/Gradio) hiển thị priority queue, cho mentor override, log ground truth.
> 6. **Iterate:** Cập nhật prompt weekly dựa trên false cases. Roll out toàn bộ batch sau 2 tuần pilot.
> 7. **Monitor:** Dashboard metrics hàng tuần (time saved, digest recall, false neg rate).