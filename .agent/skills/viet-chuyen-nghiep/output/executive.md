# Executive Brief - Phương Pháp Trình Bày

**Module:** Output  
**Mục đích:** Cung cấp thông tin và tóm tắt cực kỳ ngắn gọn, đi thẳng vào cốt lõi để C-level hoặc Senior Management ra quyết định chỉ trong vài phút.

## Khi Nào Sử Dụng

**Load method này khi:**
- ✅ Loại content: Executive Summary, Pitch Brief, Memo, Update tình hình dự án nhanh (Flash update).
- ✅ Mục đích: Yêu cầu phê duyệt, Báo cáo rủi ro cực gắt, Đề xuất hành động chiến lược.
- ✅ Độc giả: C-Level (CEO, CTO), VPs, Founders, Directors (những người có rất ít thời gian đọc).
- ✅ Platform: Slack channel của Ban Giám Đốc, Email ngắn, 1-pager proposal.
- ✅ Goal: Trình bày bối cảnh siêu tốc và lấy được quyết định/Chỉ đạo mà không gây mất thời gian.

**Không dùng khi:**
- Độc giả là team sản xuất cần tài liệu technical dài dòng (dùng `technical-academic`).
- Trình bày một báo cáo data đồ sộ phân tích chi tiết (dùng `data-report`).
- Cần kể một câu chuyện truyền thụ văn hóa (dùng `storytelling`).

---

## Nguyên Tắc Cốt Lõi

**Executive Brief = BLUF (Bottom-Line Up Front) × Brutal Brevity (Ngắn gọn tuyệt đối) × Action (Kêu gọi hành động rõ ràng)**

Đặc điểm then chốt:
- **BLUF:** Kết luận/Vấn đề quan trọng nhất nằm ngay ở CÂU ĐẦU TIÊN. Không có dạo đầu vòng vo.
- **Brutal Brevity:** Xóa bỏ mọi từ ngữ trang trí, cắt bớt jargon kỹ thuật không cần thiết. Viết như thể bạn đang trả tiền cho mỗi từ.
- **Action:** Sếp đọc xong phải biết mình cần "Phê duyệt (Approve)", "Cho ý kiến", hay chỉ là "Để biết (FYI)".

---

## Phần 1: Cấu Trúc Báo Cáo Siêu Tốc (The BLUF Format)

Mọi bản Executive Brief phải theo thứ tự sau:

### 1. TL;DR (Kết luận / Nhu cầu chính)
- 1 đến 2 câu.
- Xin X tiền / Báo rủi ro Y / Đề xuất làm Z.
- Mẫu: *"Dự án A đang trễ 2 tuần do lỗi server. Đề xuất cấp ngân sách $500 để thuê cloud ngoài xử lý tức thì."*

### 2. Context (Bối cảnh Tối Giản)
- Trả lời nhanh gọn: Chuyện gì đang xảy ra? Tại sao sếp phải quan tâm?
- Nếu tác động đến: **Doanh thu, Chi phí, Rủi ro pháp lý, Thị phần**, hãy bôi đậm.

### 3. Vấn đề cốt lõi / Options (Chìa khóa quyết định)
- Nêu rõ hiện chúng ta có những Option nào.
- So sánh các phương án (Dùng bullet point định list ra pros/cons cực gọn).

### 4. Recommendation (Khuyến nghị từ bạn)
- Ý kiến của team chuyên môn là chọn Option nào, vì sao.

### 5. Next Steps / Call to Action (Sếp cần làm gì)
- Đóng ván bài: "Chờ [Người X] phê duyệt Option A để khởi chạy vào thứ Sáu tuần này."

---

## Phần 2: Kỹ Thuật Trình Bày Ép Kiểu (Brutal Formatting)

- **Không dùng đoạn văn:** Đoạn văn là kẻ thù của C-Level. Dụng tối đa Bullet Points.
- **Rules of 3:** Bộ não người nhớ số 3. Nếu đưa lý do / option, cố gắng cô đọng thành 3 gạch đầu dòng mạnh nhất.
- **In Đậm Keywords (Bolding Index):** Bôi đậm những con số, tên người, deadline. Sếp có xu hướng đọc lướt các chữ đậm trước để nắm ý.

✅ **Đúng (Scannable text):**
> **TL;DR:** Cần phê duyệt **2.000 USD** để chạy chiến dịch Ads dự phòng, bù đắp **-15% hụt target** trong tháng 3.

❌ **Sai (Wall of text):**
> Kính gửi Ban Giám đốc, trong tháng 3 vừa qua chúng ta đã gặp khó khăn trong việc vận hành dẫn đến việc không đạt được mức doanh thu như kỳ vọng, hụt khoảng 15%. Do đó team đề xuất chúng ta cần bổ sung ngân sách là 2.000 đô-la Mỹ...

---

## Phần 3: Bộ Lọc (The Executive Filter)

Trước khi viết bất cứ câu nào vào bản mộc, hãy test qua bộ lọc:
1. Sếp có quan tâm đến thuật toán cụ thể bằng React/Java không? -> **KHÔNG**. Loại bỏ.
2. Sếp có quan tâm nó làm chậm tiến độ 3 ngày không? -> **CÓ**. Viết to lên.
3. Sếp có cần biết quá trình team thức đêm làm không? -> **KHÔNG**. Bỏ.

**Chỉ giữ lại:** 
- Tác động Doanh Thu (Tăng/giảm bao nhiêu tiền?)
- Tác động Tiến Độ (Kéo dài/thu hẹp bao nhiêu thời gian?)
- Khẩu vị Rủi Ro (Low, Med, High risk?)
- Tác động Nguồn Lực (Cần bao nhiêu người làm?)

---

## Phần 4: Giọng Văn & Tone

- **Quyệt đoán, chắc chắn:** Tránh dùng "Có thể", "Hình như", "Em nghĩ là". Dùng "Dữ liệu cho thấy", "Đề xuất chọn", "Xác nhận".
- **Respectful nhưng bình đẳng:** Không nịnh nọt dài dòng. Tôn trọng sếp bằng cách dùng ít thời gian của sếp nhất có thể.

---

## Phần 5: Checklist

Trước khi Gửi / Xuất bản Executive Brief:
- [ ] Câu kết luận lõi (BLUF) đã ở đầu tiên chưa?
- [ ] Văn bản dài quá 1 trang A4 (hoặc quá 2 cuộn chuột màn hình) không? (Nếu có -> Cắt ngắn lại).
- [ ] Gạch bỏ hoàn toàn các Jargon kỹ thuật / Quy trình tiểu tiết chưa?
- [ ] Con số quan trọng, Target Date, Money metrics đã được **in đậm** chưa?
- [ ] Đã có lời Kêu gọi hành động (Call to action) cụ thể để sếp Yes/No chưa?

---

## Lỗi Thường Gặp
- **Giữ hồi hộp (Bury the lead):** Dẫn dắt nguyên nhân lịch sử xong mới báo kết quả cuối cùng ở dưới cùng của trang -> Sếp sẽ tự động bỏ lỡ thông tin.
- **Cung cấp vấn đề nhưng bắt sếp nghĩ giải pháp:** "Dự án A chậm rồi sếp ạ, sếp xem xử lý thế nào" -> Phải là "Dự án A chậm, đề xuất Option 1 hoặc 2. Nên chọn 2".
- **Over-explaining:** Giải thích quá nhiều về kỹ thuật và quá trình thay vì business outcome (hậu quả kinh doanh).

---

## Integration với IPO Framework

**Executive Brief trong IPO:**

```
INPUT Phase:
├─ Content type: Tóm tắt, Báo cáo rủi ro, Xin phê duyệt, Memo
├─ Purpose: Quyết định nhanh (Fast Decision), Inform at top level
├─ Audience: C-Level, VP, Director
└─ Platform: Email, Trello, Slack, Brief Doc

PROCESS Phase:
├─ phan-tich.md → (Giúp tổng hợp từ mớ data hỗn độn ra 1 core insight)
└─ kiem-chung.md → (Đảm bảo số tiền / số liệu báo sếp tuyệt đối không sai)

OUTPUT Phase:
├─ SKILL.md → Route to executive
├─ quy-tac-viet.md → Vietnamese rules (BẮT BUỘC)
└─ executive.md → Apply framework này
    ↓
    Brief cực ngắn, rõ ràng, định hướng rủi ro/kinh doanh
```

---

**Token budget:** ~1,500 tokens  
**Độ tự do:** Rất thấp (Cực gắt về độ cô đọng, cấm lan man).  
**Integration:** Kết hợp tốt với `phan-tich.md` để rút insight.  
**Best for:** Email nội bộ cấp cao, Report hàng tuần cho Founder, Tóm tắt dự án.
