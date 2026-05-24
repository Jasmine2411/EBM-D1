# Data Report - Phương Pháp Trình Bày

**Module:** Output  
**Mục đích:** Xử lý và trình bày dữ liệu thô thành các insights kinh doanh/hoạt động dễ hiểu, logic, phục vụ cho quá trình đánh giá hoặc theo dõi.

## Khi Nào Sử Dụng

**Load method này khi:**
- ✅ Loại content: Báo cáo kinh doanh, báo cáo hiệu suất (performance), phân tích khảo sát, báo cáo marketing/tài chính.
- ✅ Mục đích: Cung cấp thông tin (Inform), Phân tích (Analyze), và hỗ trợ ra quyết định (Decision-Support).
- ✅ Độc giả: Business professionals, Data Analysts, Quản lý cấp trung (Manager).
- ✅ Platform: Reports, Email dài, Word/PDF, Docs nội bộ.
- ✅ Goal: Biến đống số liệu khô khan thành một câu chuyện có logic (Data Storytelling for Business).

**Không dùng khi:**
- Cần tóm lược cực ngắn để CEO duyệt nhanh (dùng `executive`).
- Bài viết blog gợi cảm xúc (dùng `storytelling`).
- Sách học thuật hoặc quy trình IT (dùng `technical-academic` hoặc `technical`).

---

## Nguyên Tắc Cốt Lõi

**Data Report = Accuracy (Chính xác) × Insight (Góc nhìn sâu) × Visual/Logical Flow (Mạch logic & Trình bày)**

Đặc điểm then chốt:
- **Accuracy:** Tuyệt đối không tự bịa số liệu, giữ nguyên bản chất dữ liệu nguồn.
- **Insight:** Không chỉ liệt kê "Có 50 người mua", mà phải nói "Tăng 15% so với tháng trước do chiến dịch X."
- **Logical Flow:** Đi từ Bức tranh toàn cảnh (Macro) đến Chi tiết (Micro).

---

## Phần 1: Cấu Trúc Data Report

Một báo cáo dữ liệu tốt luôn tuân theo phễu phân tích (Funnel):

### 1. Overview (Tổng quan kết quả)
- Tóm tắt rất nhanh trong 1-2 đoạn. 
- Trả lời câu hỏi: Tóm lại dữ liệu này báo hiệu tốt hay xấu? Xu hướng chính là gì?

### 2. Key Insights (Các phát hiện quan trọng nhất)
- Lấy 3-4 điểm nổi bật nhất.
- Sử dụng bullet points. Mỗi điểm dùng cấu trúc: `[Phát hiện] + [Data chứng minh]`.

### 3. Deep Dive (Phân tích chi tiết)
- Chia ra theo các chiều phân tích (Dimensions): Theo Kênh, Theo Nhóm Tuổi, Theo Sản Phẩm, v.v.
- Áp dụng kỹ thuật: **What -> So What -> Now What**.

### 4. Recommendations / Next Steps (Khuyến nghị)
- Dựa trên data, đề xuất các hành động tiếp theo.

---

## Phần 2: Trình Bày Số Liệu & Bảng Biểu

### 1. Số liệu không bao giờ đứng một mình
Một con số độc lập không có ý nghĩa. Phải luôn có context so sánh:
❌ **Tuyệt đối không:** "Doanh thu là 500 triệu."
✅ **Phải viết:** "Doanh thu là 500 triệu, **đạt 110% target** và **tăng 20% so với tháng trước**."

### 2. Định dạng số
- Thống nhất đơn vị đo lường xuyên suốt (VND hay USD, % hay phần nghìn).
- Format dễ nhìn: `1.500.000` thay vì `1500000`.

### 3. Cấu trúc Bảng Markdown (Markdown Tables)
- Khi có > 3 thông số so sánh, hãy dùng bảng markdown.
- **ĐẶC BIỆT:** Hãy biến tiêu đề bảng thành kết luận chính của bảng đó để người đọc khỏi phải dịch thông số.

✅ **Đúng (Tiêu đề có insight):**
**Bảng 1: Lượt chuyển đổi tăng mạnh ở người dùng Mobile trong Q3**
| Nhóm Thiết Bị | Lượt Truy Cập | Chuyển Đổi (%) | Tăng trưởng (MoM) |
| ------------- | ------------- | -------------- | ----------------- |
| Mobile        | 50,000        | 4.5%           | +25%              |
| Desktop       | 15,000        | 2.1%           | -5%               |

---

## Phần 3: Kỹ Thuật Đào Sâu (What -> So What -> Now What)

Khi phân tích chi tiết ở phần **Deep Dive**, bạn phải dẫn dắt tư duy người đọc qua 3 tầng:

1. **What (Rốt cuộc số liệu là gì):** Ghi nhận thực tế.
   *Ví dụ: "Tỷ lệ thoát (Bounce rate) trang thanh toán ở mức cao (65%)."*
2. **So What (Thì sao / Ý nghĩa của nó):** Tại sao hiện tượng đó quan trọng. 2 tầng nhân quả.
   *Ví dụ: "Điều này cho thấy có rào cản lớn ngăn cản user chốt đơn, tập trung vào nhóm khách lạ, nghi ngờ do form điền thông tin quá dài."*
3. **Now What (Làm gì tiếp theo):** Đề xuất giải pháp khắc phục hay phát huy.
   *Ví dụ: "Cần test thử rút gọn form từ 7 trường xuống 3 trường bắt buộc, hoặc tích hợp đăng nhập qua Google."*

---

## Phần 4: Giọng Văn & Tone

- **Khách quan, phân tích:** Tránh dùng cảm xúc chủ quan ("Rất đáng tiếc", "Thật vui mừng"). Thay vào đó dùng các từ tính chất ("Đáng lưu ý", "Suy giảm mạnh", "Tăng trưởng đột biến").
- **Dựa hoàn toàn vào Data:** Luôn dùng câu "Theo dữ liệu...", "Kết quả cho thấy...", "Chỉ số hiện tại chỉ định...".

---

## Phần 5: Checklist

Trước khi hoàn tất Data Report:
- [ ] Báo cáo có bắt đầu bằng kết luận tổng quan (Overview) không?
- [ ] Các con số quan trọng đều có tham chiếu so sánh (MoM, YoY, vs Target) chưa?
- [ ] Báo cáo có mô hình What -> So What -> Now What không?
- [ ] Nếu có nhiều thông số, đã gom vào Bảng Markdown cho gọn mắt chưa?
- [ ] Tiêu đề bảng có chứa sẵn insight chưa?
- [ ] Giọng văn hoàn toàn trung lập/khách quan không?

---

## Lỗi Thường Gặp
- **Data Vomiting (Nôn mửa dữ liệu):** Nhồi nhét hàng chục con số vào 1 đoạn văn khiến người đọc mù mờ. *-> Hãy dùng bảng, hoặc chỉ trích rút Insight quan trọng nhất.*
- **Kết luận thiếu bằng chứng:** Rút insight mà không trích dẫn con số nào trong câu.
- **Thiếu "Now What":** Báo cáo chỉ chỉ ra lỗi/thực trạng mà thiếu vắng đề xuất.

---

## Integration với IPO Framework

**Data Report trong IPO:**

```
INPUT Phase:
├─ Content type: Báo cáo, dữ liệu thô Excel/CSV, Raw Metrics
├─ Purpose: Tóm lược ý nghĩa của dữ liệu, Inform & Analyze
├─ Audience: Managers, Analysts, Business audience
└─ Platform: Report Docs, Slack Analytics Update

PROCESS Phase:
├─ phan-tich.md → Bắt buộc phải chạy (Để chuyển Data Thô -> Insight)
└─ kiem-chung.md → (Verify chéo dữ liệu)

OUTPUT Phase:
├─ SKILL.md → Route to data-report
├─ quy-tac-viet.md → Vietnamese rules (BẮT BUỘC)
└─ data-report.md → Apply framework này
    ↓
    Báo cáo rõ ràng, dễ hiểu, logic sắc bén
```

---

**Token budget:** ~1,800 tokens  
**Độ tự do:** Thấp-Trung bình (Nội dung phải bám strict vào Input Data).  
**Integration:** Kết hợp chặt chẽ với `process/phan-tich.md`.  
**Best for:** Báo cáo Marketing, Sales, Product Performance, Nghiên cứu thị trường.
