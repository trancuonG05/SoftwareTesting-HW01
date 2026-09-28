# Khoa Công nghệ Thông tin (FIT) – Trường Đại học Khoa học Tự nhiên (HCMUS)
**Kiểm chứng Phần mềm (AI-augmented · 2026)**  
**CHÍNH SÁCH AI · BIỂU MẪU — 2026 v1.0**

---

# [AI-02] AI Audit Report — Mẫu 5 mục cho mỗi Artifact

*Phụ lục bắt buộc đính kèm cho mọi bài tập có dùng AI (HW#01–HW#06, Seminar).*  
*Tài liệu được biên soạn lại từ Med Kharbach, PhD (2026) — Mẫu Chính sách Sử dụng AI cho Giáo dục Đại học. Giấy phép CC BY-NC-SA 4.0. Phiên bản này được FIT@HCMUS điều chỉnh cho môn CS423 / CSC15003 Kiểm chứng Phần mềm.*

---

## 1. Thông tin Sinh viên

| Mục | Giá trị |
| :--- | :--- |
| **Họ tên sinh viên (in hoa):** | TRẦN GIA CƯỜNG |
| **MSSV:** | 23120225 |
| **Lớp / Khoá:** | CQ2023/3 |
| **Mã bài tập (ví dụ HW#00, HW#02):** | HW01-AI |
| **Ngày làm bài:** | 27/09/2026 |
| **Công cụ AI đã dùng:** | Gemini 3.8 Flash, Claude 3.5 Sonnet |
| **Có dùng AI trong bài không:** | [x] Có [ ] Không |

---

## 2. Hướng dẫn (đọc trước khi điền)

* Thêm 1 hàng cho mỗi artifact AI sinh (test case, script, checklist, OpenAPI spec, JMeter plan…).
* Dán nguyên văn prompt — **KHÔNG paraphrase**.
* Dán nguyên văn output AI (hoặc kèm screenshot có chú thích trong báo cáo).
* Gắn nhãn: **VALID** / **INVALID** / **INCOMPLETE**.
* Lý do phải dẫn chiếu slide, mục ISTQB, hoặc RFC kỹ thuật.
* Hiển thị bản sửa với phần thay đổi được tô sáng.
* *Hàng mẫu in nghiêng — thay trước khi nộp.*

---

## 3. Bảng Audit — 1 hàng / artifact

| (1) Prompt + Công cụ | (2) Output AI | (3) Verdict | (4) Lý do (ISTQB) | (5) Bản SV sửa |
| :--- | :--- | :---: | :--- | :--- |
| *Mẫu (italic) — thay trước khi nộp:*<br>**Tool:** AI Tool (e.g., ChatGPT, Claude, Gemini)<br>**Thời gian:** 14:32 25/02/2026<br>**Prompt:** *"Sinh test case cho hàm parsePhoneNumberVN…"* | *TC01: parsePhoneNumberVN("0912345678")<br>Kỳ vọng: {prefix:84, number:912345678, valid:true}…* | *INCOMPLETE* | *AI bỏ qua định dạng RFC 3966. ISTQB FL §4.3 Boundary Value Analysis yêu cầu test ranh giới định dạng.* | *Thêm TC: parsePhoneNumberVN("+84-91-234-5678")<br>Kỳ vọng: {prefix:84, number:912345678, valid:true}* |
| **Artifact #1:** Mindmap vai trò QA/QC theo ISTQB<br>**Tool:** Gemini 3.8 Flash<br>**Thời gian:** 23:29 24/09/2026<br>**Prompt:** *"vẽ/mô tả sơ đồ liên kết các vai trò QA/QC vào quy trình kiểm thử chuẩn của ISTQB..."* | Mô tả quy trình gồm 7 giai đoạn. Đưa Automation Engineer vào Test Analysis, thiếu Technical Test Analyst ở Analysis, và đưa "AI Test Agent" vào Test Execution. | **INCOMPLETE** | Sai chuẩn ISTQB FL v4.0: Analysis chỉ do Test Analyst / Technical Test Analyst làm. AI chỉ là công cụ (tool), không phải vai trò (role). | Loại bỏ vai trò "AI Test Agent", đưa Technical Test Analyst vào bước Analysis, chuyển Automation Engineer sang Implementation & Execution. |
| **Artifact #2:** Phân tích sự cố Air Canada Chatbot (Requirement 2)<br>**Tool:** Gemini 3.8 Flash<br>**Thời gian:** 16:50 25/09/2026<br>**Prompt:** *"phân tích hoặc giải thích 1 lỗi trong danh sách 20 lỗi trên."* | Phân tích sự cố Air Canada Chatbot: Khẳng định lỗi do mô hình tự suy diễn sinh quy định (LLM hallucination) và chatbot có kèm link dẫn về trang chính sách tang chế. | **INCOMPLETE** | Đối chiếu bản án *Moffatt v. Air Canada, 2024 BCCRT 149*:<br>1. Thiên kiến diễn giải (Framing bias): Gán hệ thống NLP/rule-based thành lỗi LLM hallucination.<br>2. Ảo giác bịa thêm (Hallucination by addition): Chatbot thực tế không hề gửi link chính sách trong phiên chat. | Bác bỏ nhận định áp đặt về LLM hallucination, đính chính chatbot là hệ thống NLP riêng và không gửi link chính sách tang chế, bổ sung link bản án CRT đối chứng. |
| **Artifact #3:** 15 Test Cases cho Quạt đứng & File TestCases.xlsx (Requirement 3)<br>**Tool:** Gemini 3.8 Flash / Claude 3.5 Sonnet<br>**Thời gian:** 00:25 26/09/2026<br>**Prompt:** *"Hãy thiết kế danh sách test cases kiểm thử chức năng cho thiết bị Quạt đứng cơ học..."* | Danh sách 12 ca kiểm thử chức năng cơ bản theo luồng bình thường (bật số 1-2-3, tắt, tuốc-năng, nâng hạ chiều cao). | **INCOMPLETE** | Thiếu kiểm thử kịch bản biên và kiểm thử lỗi theo ISTQB FL §4.3: AI chỉ sinh ra ca kiểm thử luồng thuận (Happy path), hoàn toàn không nhận diện được các rủi ro vật lý (chập phím, mất điện đột ngột, kẹt cơ khí) cũng như không phản ánh được hiện trạng hư hỏng thực tế của thiết bị vật lý. | Tự thiết kế bổ sung 3 ca Edge Cases vật lý (TC13, TC14, TC15), tiến hành chạy kiểm thử thực tế phát hiện lỗi nút số 2 (TC02: FAIL) và hoàn thiện xuất bản artifact bảng tính [TestCases.xlsx] theo đúng quy cách. |

---

## 4. Tổng kết Độ chính xác AI

*Tổng hợp verdict từ Mục 3 và điền vào bảng dưới.*

| Chỉ số | Số lượng | Tỉ lệ |
| :--- | :---: | :---: |
| **Tổng artifact AI sinh đã audit** | 3 | 100% |
| **VALID (đúng, dùng nguyên)** | 0 | 0% |
| **INVALID (sai; loại bỏ)** | 0 | 0% |
| **INCOMPLETE (chấp nhận sau khi sửa)** | 3 | 100% |

---

## 5. Kết luận — Khi nào nên / không nên dùng AI?

*Viết 80–150 chữ mô tả pattern quan sát được. AI mạnh ở đâu? AI sai ở đâu? Khuyến nghị của bạn cho việc dùng AI trong loại công việc này?*

> *Qua quá trình kiểm định 3 artifacts trong bài tập HW01, tôi nhận thấy model AI thể hiện sức mạnh vượt trội trong việc khởi tạo nhanh cấu trúc cơ bản ban đầu, tổng hợp lý thuyết và liệt kê các testcase theo luồng thuận. Tuy nhiên, AI vẫn bộc lộ những điểm yếu khi đối mặt với dữ kiện thực tế và môi trường vật lý: dễ mắc thiên kiến khi diễn giải (vd: gán ghép sự cố Air Canada thành lỗi LLM hallucination), ảo giác bịa đặt dữ liệu không có thật (thêm thắt link chính sách), và hoàn toàn thiếu nhận thức về các tương tác cơ điện (bỏ sót các trường hợp biên như chập phím hay mất điện đột ngột) hay tồn tại phím lỗi nhưng AI gán là hoạt động được. Một số bài học được đề cập cũng nhắc nhở việc con người mới là cá nhân chịu trách nhiệm pháp lý, AI chỉ là công cụ hỗ trợ do con người sử dụng. Do đó, bài học rút ra là: chỉ nên xem AI như một trợ lý tạo bản nháp để tăng tốc độ khởi tạo; tuyệt đối không sử dụng trực tiếp kết quả AI mà không có kỹ sư con người đối soát chéo với tài liệu kỹ thuật chuẩn mực (Ground Truth).*

---

## 6. Mandatory Disclosure (dán nguyên văn)

> *"Test cases and mindmap draft were initially generated by Gemini 3.8 Flash and Claude 3.5 Sonnet; I reviewed and modified Section 1.3 (QA/QC Roles & ISTQB Mindmap), added edge cases TC13, TC14, TC15 in Section 3.2; Section 1.2 (AI Impact Analysis), all video demonstrations, and photos were produced entirely by me. The detailed AI Audit Report is attached as Appendix A. I confirm I did not use AI to generate any artifact listed in the prohibited category below."*

### Chữ ký xác nhận

| Mục | Chi tiết |
| :--- | :--- |
| **Họ tên sinh viên (in hoa):** | TRẦN GIA CƯỜNG |
| **MSSV:** | 23120225 |
| **Lớp / Khoá:** | CQ2023/3 |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Giảng viên:** | TS. Lâm Quang Vũ / Hồ Tuấn Thanh |
| **Ngày:** | 27/09/2026 |
| **Chữ ký sinh viên:** | Cường |

---

## Tham khảo

1. Kharbach, M. (2026). *AI Use Policy Templates for Higher Education*. CC BY-NC-SA 4.0.  
2. ISTQB Foundation Level Syllabus v4.0 (2023).  
3. Hardman, P. (2025). *A Post-AI Learning Taxonomy*.  
4. Fuster Rabella, M. (2025). *OECD Education Working Paper No. 338*.  
5. Perkins, M., Roe, J., & Furze, L. (2025). *AI Assessment Scale*.  
6. Anthropic (2025). *Building reliable AI test agents — engineering blog*.  
7. DeepEval & Promptfoo documentation — testing frameworks for LLM systems.
