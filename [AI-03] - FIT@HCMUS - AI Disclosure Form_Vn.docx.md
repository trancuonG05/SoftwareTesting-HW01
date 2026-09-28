# Khoa Công nghệ Thông tin (FIT) – Trường Đại học Khoa học Tự nhiên (HCMUS)
**Kiểm chứng Phần mềm (AI-augmented · 2026)**  
**CHÍNH SÁCH AI · BIỂU MẪU — 2026 v1.0**

---

# [AI-03] AI Disclosure Form — Biểu mẫu Khai báo Sử dụng AI

*Đính kèm bắt buộc cho mọi bài tập có dùng AI ở bất kỳ mức nào (HW#01–HW#06, Seminar, Đồ án).*  
*Tài liệu được biên soạn lại từ Med Kharbach, PhD (2026) — Mẫu Chính sách Sử dụng AI cho Giáo dục Đại học. Giấy phép CC BY-NC-SA 4.0. Phiên bản này được FIT@HCMUS điều chỉnh cho môn CS423 / CSC13003 Kiểm chứng Phần mềm.*

---

## 1. Thông tin Môn học & Sinh viên

| Mục | Giá trị |
| :--- | :--- |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Mã bài tập:** | HW01 |
| **Tên bài tập:** | QA/QC Jobs · 20 Defects · Test a Physical Product |
| **Cấp độ AI (1–5):** | Cấp 3 (AI-Assisted Drafting with Human Verification) |
| **Ngày:** | 27/09/2026 |
| **Họ tên sinh viên (in hoa):** | TRẦN GIA CƯỜNG |
| **MSSV:** | 23120225 |
| **Lớp / Khoá:** | CQ2023/3 |
| **Giảng viên:** | TS. Lâm Quang Vũ / Hồ Tuấn Thanh |

---

## 2. Câu hỏi Khai báo

### 1. Công cụ AI đã dùng:
*Liệt kê mọi công cụ AI dùng cho bài tập này:*
- **Gemini 3.8 Flash** (Google)
- **Claude 3.5 Sonnet** (Anthropic)

---

### 2. Giai đoạn nào của bài tập có dùng AI:
*Tick chọn tất cả các giai đoạn có áp dụng:*
- [x] Brainstorm (Lên ý tưởng ban đầu)
- [x] Outline (Dựng khung cấu trúc sườn)
- [x] Viết nháp (Drafting test cases và nội dung phân tích ban đầu)
- [ ] Phản hồi
- [x] Sửa chữa (Hỗ trợ định dạng bảng biểu Markdown)
- [ ] Code
- [ ] Phân tích dữ liệu
- [ ] Thiết kế đồ hoạ
- [ ] Khác

---

### 3. Prompt / nhiệm vụ chính cho AI:
*Dán nguyên văn 2–3 prompt quan trọng nhất (Chi tiết toàn bộ prompt log có timestamp đính kèm tại `prompt_log.md`):*

1. **Prompt #01 (Requirement 1 - Quy trình ISTQB):**
   ```text
   vẽ/mô tả sơ đồ liên kết các vai trò QA/QC vào quy trình kiểm thử chuẩn của ISTQB (Planning, Monitoring & Control, Analysis, Design, Implementation, Execution, Completion).
   ```
2. **Prompt #02.2 (Requirement 2 - Phân tích lỗi phần mềm):**
   ```text
   phân tích hoặc giải thích 1 lỗi trong danh sách 20 lỗi trên.
   ```
3. **Prompt #03 (Requirement 3 - Gợi ý Test Cases quạt đứng):**
   ```text
   Hãy thiết kế danh sách test cases kiểm thử chức năng cho thiết bị Quạt đứng cơ học (không có hẹn giờ, gồm các nút bấm số 0, 1, 2, 3, tuốc-năng đảo hướng, khớp ngửa cúi và khóa nâng hạ chiều cao) theo chuẩn: Test ID, Objective, Precondition, Input, Steps, Expected Result.
   ```

---

### 4. Phần cụ thể AI đóng góp:
* **Phần AI đóng góp:**
  - Khởi tạo khung sơ đồ phân chia vai trò QA/QC theo quy trình ISTQB (Mục 1.3).
  - Soạn thảo bản giải thích sơ khởi về sự cố Air Canada Chatbot bịa đặt chính sách hoàn vé (Mục 2.3).
  - Gợi ý danh sách 12 ca kiểm thử chức năng cơ bản theo luồng thuận (Happy path: TC01–TC12) cho thiết bị quạt đứng (Mục 3.2).
* **Phần sinh viên tự thực hiện 100% (AI KHÔNG tham gia):**
  - **Mục 1.1 & 1.2:** Tìm kiếm, thu thập 10 tin tuyển dụng thực tế $\le$ 60 ngày, chụp ảnh màn hình có tài khoản chính chủ, và tự viết toàn bộ đoạn phân tích tác động của AI (AI Impact Analysis).
  - **Mục 1.3:** Rà soát, bắt 3 lỗi sai kiến thức của AI so với chuẩn ISTQB Foundation Level v4.0 và vẽ lại sơ đồ mindmap chuẩn hóa (`mindmap.png`).
  - **Mục 2.1 & 2.2:** Tìm kiếm, tổng hợp 20 sự cố phần mềm thực tế (2022–2026), kiểm tra link dẫn chứng sống (HTTP 200 OK).
  - **Mục 2.3:** Đối soát bản án thực tế để bắt 2 lỗi thiên kiến và ảo giác của AI.
  - **Mục 3.1, 3.2 & 3.3:** Chụp ảnh thiết bị kèm Thẻ sinh viên; tự thiết kế 3 ca kiểm thử biên vật lý (Edge Cases: TC13, TC14, TC15); hoàn thiện bảng tính chuẩn hóa và xuất file [TestCases.xlsx]; trực tiếp thao tác thực tế ghi nhận lỗi phần cứng tại TC02 và quay 5 video demo thực thi có giọng nói thuyết minh chính chủ.
  - **Mục 4:** Viết toàn bộ bài phản biện AI Critique, kết luận kiểm định và các cam kết liêm chính học thuật.

---

### 5. Cách tôi rà soát / chỉnh sửa / xác minh đầu ra AI:
1. **Đối chiếu chuẩn mực kiến thức (Syllabus Verification):** Đối chiếu sơ đồ phân vai của AI với tài liệu *ISTQB Certified Tester Foundation Level Syllabus v4.0* (§1.4) để phát hiện và loại bỏ các lỗi sai vai trò (bỏ "AI Test Agent", chuyển Automation Tester sang khâu Implementation/Execution).
2. **Kiểm chứng án lệ và nguồn tin gốc (Fact & Legal Verification):** Tra cứu trực tiếp bản án chính thức *Moffatt v. Air Canada, 2024 BCCRT 149* của Tòa án Dân sự British Columbia để phản biện lại các suy diễn gán ghép lỗi LLM và ảo giác bịa thêm chi tiết của AI.
3. **Thực nghiệm trên thiết bị cơ điện thực tế (Physical Testing):** Vận hành trực tiếp trên chiếc quạt đứng tại phòng để kiểm tra độ tin cậy của 12 ca test do AI gợi ý, đồng thời tự phát hiện các rủi ro vận hành cơ học (chập phím bấm đồng thời, mất điện đột ngột, kẹt cơ khí) mà AI bỏ sót để bổ sung các ca kiểm thử biên.

---

### 6. Trích dẫn (Phong cách IEEE):
1. Google, "Gemini 3.8 Flash Large Language Model," *Google AI*, 2026. [Online]. Available: https://gemini.google.com
2. Anthropic, "Claude 3.5 Sonnet Large Language Model," *Anthropic AI*, 2026. [Online]. Available: https://claude.ai
3. International Software Testing Qualifications Board (ISTQB), *Certified Tester Foundation Level Syllabus v4.0*, ISTQB, 2023.
4. Civil Resolution Tribunal, "Moffatt v. Air Canada, 2024 BCCRT 149," *CanLII / CRT Decisions*, Feb. 2024. [Online]. Available: https://decisions.civilresolutionbc.ca/crt/crtd/en/item/525448/index.do

---

## 3. Cam đoan Trung thực

Bằng việc ký tên dưới đây, tôi cam đoan thông tin khai báo ở trên là chính xác và đầy đủ. Tôi hiểu rằng việc không khai báo hoặc khai báo sai lệch về việc dùng AI sẽ bị coi là vi phạm liêm chính học thuật và có thể dẫn đến điểm 0 cho bài tập cùng việc bị chuyển lên hội đồng kỷ luật.

### Chữ ký xác nhận

| Mục | Chi tiết |
| :--- | :--- |
| **Họ tên sinh viên (in hoa):** | TRẦN GIA CƯỜNG |
| **MSSV:** | 23120225 |
| **Lớp / Khoá:** | CQ2023/3 |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Giảng viên:** | TS. Lâm Quang Vũ / Hồ Tuấn Thanh |
| **Ngày:** | 27/09/2026 |
| **Chữ ký:** | *Cường* |

---

## Tham khảo

1. Kharbach, M. (2026). *AI Use Policy Templates for Higher Education*. CC BY-NC-SA 4.0.  
2. ISTQB Foundation Level Syllabus (v4.0, 2023).  
3. Hardman, P. (2025). *A Post-AI Learning Taxonomy*.  
4. Fuster Rabella, M. (2025). *OECD Education Working Paper No. 338*.  
5. Perkins, M., Roe, J., & Furze, L. (2025). *AI Assessment Scale*.  
