// turbo-all
---
trigger: always_on
---

# Quy tắc về Ngôn ngữ & Văn phong

1. **Ngôn ngữ bắt buộc:** Luôn trả lời trong Chat và tạo nội dung văn bản (Artifacts, Files) bằng **Tiếng Việt**.
2. **Ngoại lệ:** Giữ nguyên các thuật ngữ chuyên ngành tiếng Anh phổ biến (Marketing, Sales, CEO, AI, Automation PM...) nếu không có từ tiếng Việt tương đương súc tích.
3. **Văn phong:** Chuyên nghiệp, gãy gọn, phù hợp môi trường doanh nghiệp.
4. **Đánh số thứ tự Form Khảo sát (Global Rule):** Khi tạo mới hoặc chỉnh sửa các biểu mẫu khảo sát (Survey Forms), luôn đánh số thứ tự câu hỏi tăng dần một cách tuần tự (VD: Câu 1, Câu 2, Câu 3...). Tuyệt đối KHÔNG sử dụng các đánh số rẽ nhánh chứa chữ cái (như Câu 2b, Câu 4c...).
5. **Continuous Learning & Logging (Global Rule):** Sau mỗi phiên làm việc hoặc chuỗi tác vụ, LUÔN LUÔN ghi lại nhật ký công việc (Log), đúc kết và rút kinh nghiệm (Lessons Learned), sau đó tự động cập nhật các kinh nghiệm này vào hệ thống (Rules, Skills, Workflows) để cải tiến liên tục.
6. **HTML Presentation Sync (Global Rule):** Khi tạo hoặc chỉnh sửa bộ file HTML presentation (`*_Presentation.html` + `print_all_slides.html`), mọi thay đổi nội dung/thiết kế trong file interactive **PHẢI** được đồng bộ sang file print version trước khi xuất PDF. Không giao file PDF nếu chưa hoàn thành bước đồng bộ này.
7. **Logo & Typography (Global Rule):** Khi thiết kế tài liệu HTML có logo thương hiệu: (a) Luôn dùng thẻ `<img>` với file logo thật — không dùng CSS text thay thế. (b) Chọn đúng phiên bản logo phù hợp với nền slide (logo đỏ/đen cho nền trắng, logo trắng cho nền tối). (c) Trong nội dung tiếng Việt, sử dụng dấu gạch ngang ngắn `-` thay vì em-dash `—` để tránh lỗi hiển thị và đảm bảo nhất quán.
8. **Auto-Accept (Global Rule):** Luôn ưu tiên bật `SafeToAutoRun: true` cho các câu lệnh an toàn (không gây hại, không xóa dữ liệu quan trọng) để tối ưu hóa quy trình làm việc mà không cần chờ xác nhận thủ công từ người dùng.
9. **Sync Project Docs (Global Rule):** Khi nhận được yêu cầu cập nhật/đồng bộ thông tin mới xuyên suốt một dự án, LUÔN thực hiện "Logic over Execution" đầu tiên: phân tích phản biện để lọc bỏ các kỳ vọng phi thực tế hoặc hứa hẹn quá mức trước khi cập nhật. Để đảm bảo tốc độ tối ưu, LUÔN dùng công cụ quét nhanh (`grep_search`) để định vị file và chỉnh sửa cục bộ (`replace_file_content`), tuyệt đối không ghi lại toàn bộ nội dung file (overwrite whole file) trừ khi bị bắt buộc.