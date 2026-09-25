# Khoa Công nghệ Thông tin (FIT) – Trường Đại học Khoa học Tự nhiên (HCMUS)
**CS423 / CSC13003 – Kiểm chứng Phần mềm (AI-augmented · 2026)**  
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
| **Lớp / Khoá:** | 23CLC02 / K23 |
| **Mã bài tập (ví dụ HW#00, HW#02):** | HW01-AI |
| **Ngày làm bài:** | 25/09/2026 |
| **Công cụ AI đã dùng:** | Gemini 3.8 Flash, ChatGPT |
| **Có dùng AI trong bài không:** | [x] Có &nbsp;&nbsp;&nbsp; [ ] Không |

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
| **Artifact #3:** | | | | |
| **Artifact #4:** | | | | |
| **Artifact #5:** | | | | |
| **Artifact #6:** | | | | |
| **Artifact #7:** | | | | |
| **Artifact #8:** | | | | |
| **Artifact #9:** | | | | |
| **Artifact #10:** | | | | |

---

## 4. Tổng kết Độ chính xác AI

*Tổng hợp verdict từ Mục 3 và điền vào bảng dưới.*

| Chỉ số | Số lượng | Tỉ lệ |
| :--- | :---: | :---: |
| **Tổng artifact AI sinh đã audit** | 2 | 100% |
| **VALID (đúng, dùng nguyên)** | 0 | 0% |
| **INVALID (sai; loại bỏ)** | 0 | 0% |
| **INCOMPLETE (chấp nhận sau khi sửa)** | 2 | 100% |

---

## 5. Kết luận — Khi nào nên / không nên dùng AI?

*Viết 80–150 chữ mô tả pattern quan sát được. AI mạnh ở đâu? AI sai ở đâu? Khuyến nghị của bạn cho việc dùng AI trong loại công việc này?*

> AI có khả năng tổng hợp thông tin và phác thảo cấu trúc khung cực kỳ nhanh chóng (như liệt kê đủ 7 giai đoạn của quy trình kiểm thử ISTQB). Tuy nhiên, AI thường có xu hướng "ảo giác" (hallucination) hoặc tự suy diễn thêm các thuật ngữ thời thượng không chuẩn hóa (như bịa ra vai trò "AI Test Agent" hay đặt Automation Engineer vào khâu phân tích yêu cầu). Vì vậy, chỉ nên dùng AI để lên ý tưởng, dựng dàn ý sơ khởi; tuyệt đối không dùng nguyên văn cho các quy chuẩn kỹ thuật hoặc kiểm thử chính thức mà con người bắt buộc phải kiểm chứng và đối soát lại với tài liệu chuẩn (Ground Truth).

---

## 6. Mandatory Disclosure (dán nguyên văn)

> *"Báo cáo và các artifact này được sinh phiên bản đầu bởi Gemini 3.8 Flash; tôi đã rà soát và chỉnh sửa sơ đồ quy trình kiểm thử, bổ sung các vai trò kỹ thuật chuẩn ISTQB và phát hiện 3 lỗi sai kiến thức; toàn bộ phần đối soát và hoàn thiện do tôi tự thực hiện. AI Audit Report chi tiết đính kèm ở Phụ lục này. Tôi cam đoan không dùng AI để sinh bất kỳ artifact nào thuộc danh mục bị cấm."*

### Chữ ký xác nhận

| Mục | Chi tiết |
| :--- | :--- |
| **Họ tên sinh viên (in hoa):** | TRẦN GIA CƯỜNG |
| **MSSV:** | 23120225 |
| **Lớp / Khoá:** | 23CLC02 / K23 |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Giảng viên:** | ThS. Huỳnh Phước Hải |
| **Ngày:** | 25/09/2026 |
| **Chữ ký:** | *Trần Gia Cường* |

---

## Tham khảo

1. Kharbach, M. (2026). *AI Use Policy Templates for Higher Education*. CC BY-NC-SA 4.0.  
2. ISTQB Foundation Level Syllabus v4.0 (2023).  
3. Hardman, P. (2025). *A Post-AI Learning Taxonomy*.  
4. Fuster Rabella, M. (2025). *OECD Education Working Paper No. 338*.  
5. Perkins, M., Roe, J., & Furze, L. (2025). *AI Assessment Scale*.  
6. Anthropic (2025). *Building reliable AI test agents — engineering blog*.  
7. DeepEval & Promptfoo documentation — testing frameworks for LLM systems.
