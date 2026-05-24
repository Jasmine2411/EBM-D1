# Rule: Ghi nhận yêu cầu hội thoại (Request Logging)

## Mục đích
Đảm bảo AI luôn nắm bắt và hiển thị đầy đủ các yêu cầu của người dùng trong phiên hội thoại, giúp duy trì bối cảnh và tính minh bạch trong quá trình thực hiện task.

## Quy tắc thực hiện
1. **Luôn hiển thị danh sách**: Trước khi thực hiện bất kỳ lệnh mới nào hoặc trả lời yêu cầu mới, AI PHẢI liệt kê lại danh sách các yêu cầu đã nhận được trong phiên hội thoại hiện tại (tối đa 5-10 yêu cầu gần nhất).
2. **Định dạng danh sách**:
   - Sử dụng danh sách có thứ tự (Ordered List).
   - Đánh dấu trạng thái cho mỗi yêu cầu: `[Đang thực hiện]`, `[Đã hoàn thành]`, `[Chờ xử lý]`.
3. **Cập nhật liên tục**: Danh sách này phải được cập nhật ngay khi có yêu cầu mới hoặc khi một yêu cầu vừa hoàn thành.

## Ví dụ
**User**: "Tạo file A và sau đó tóm tắt file B."

**AI**:
"Tôi đã nhận được các yêu cầu sau:
1. [Đang thực hiện] Tạo file A.
2. [Chờ xử lý] Tóm tắt file B.

Bắt đầu thực hiện tạo file A..."

---
*Lưu ý: Luôn tuân thủ quy tắc xưng hô và ngôn ngữ đã được quy định trong các Rule khác.*
