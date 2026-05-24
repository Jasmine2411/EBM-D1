---
description: Tạo workflow mới từ lịch sử cuộc trò chuyện (Kỹ thuật đảo ngược)
---

1. Phân tích yêu cầu của người dùng và lịch sử cuộc trò chuyện gần đây để hiểu quy trình mong muốn.
2. Xác định các bước lặp lại đã thực hiện (ví dụ: các lệnh gọi tool cụ thể, chỉnh sửa file, lập luận logic).
3. Trừu tượng hóa các bước này thành dạng workflow tổng quát.
4. Tạo file mới tại `.agent/workflows/[tên-workflow].md`.
5. Nội dung phải theo chuẩn định dạng sau:
   ```markdown
   ---
   description: [Mô tả ngắn gọn]
   ---
   
   1. [Bước 1]
   // turbo (tùy chọn)
   2. [Bước 2]
   ```
6. Xác nhận với người dùng trước khi lưu file.
