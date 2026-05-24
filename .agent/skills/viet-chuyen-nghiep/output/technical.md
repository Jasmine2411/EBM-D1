# Technical Guide - Phương Pháp Trình Bày

**Module:** Output  
**Mục đích:** Hướng dẫn chi tiết từng bước, giải thích cách làm và cung cấp giải pháp kỹ thuật rõ ràng, tối ưu cho việc thực hành.

## Khi Nào Sử Dụng

**Load method này khi:**
- ✅ Loại content: Hướng dẫn sử dụng (How-to), Troubleshooting, Tiêu chuẩn vận hành (SOP), Technical Docs, Bước thực hiện Workflow.
- ✅ Mục đích: Chỉ dẫn (Instruct), giải thích cách thức hoạt động hoặc cách làm cụ thể.
- ✅ Độc giả: Mọi level (từ end-user, người mới đến kỹ sư).
- ✅ Platform: Knowledge base, Wiki, Tài liệu Markdown, Internal Docs.
- ✅ Goal: Giúp người đọc thao tác thành công hoặc xử lý gọn gàng một task cụ thể mà không bị nhầm lẫn.

**Không dùng khi:**
- Cần giải thích hàn lâm, lý thuyết sâu, nguyên lý trừu tượng (dùng `technical-academic`).
- Cần truyền cảm hứng hoặc kể chuyện (dùng `storytelling`).
- Cần tóm lược nhanh gọn cho cấp quản lý (dùng `executive`).

---

## Nguyên Tắc Cốt Lõi

**Technical Guide = Clarity (Trực tiếp, Rõ ràng) × Actionability (Khả năng thực thi) × Formatting (Dẫn dắt thị giác)**

Đặc điểm then chốt:
- **Clarity:** Không dùng từ ngữ mơ hồ, không đoán mò ngữ cảnh.
- **Actionability:** Mỗi bước đều là một hành động cụ thể, copy và paste được lệnh nếu có.
- **Formatting:** Tối ưu hóa markdown (dùng list, code block, in đậm) để người đọc quét nhanh qua màn hình vẫn hiểu.

---

## Phần 1: Cấu Trúc Step-by-Step

### 1. Mở đầu bằng bối cảnh ngắn gọn
Trước khi vào hướng dẫn, phải cho người dùng biết:
- File hoặc hệ thống nào đang thao tác.
- Mục tiêu cuối cùng của phần hướng dẫn này là gì.

### 2. Sử dụng Động Từ Chủ Động đầu câu
Các bước thực hiện phải luôn bắt đầu bằng động từ chỉ hành động, không giải thích vòng vo.

✅ **Đúng:**
> 1. **Mở** file `SKILL.md` trong thư mục gốc.
> 2. **Tìm** dòng cấu hình port.
> 3. **Thay đổi** giá trị thành `8080`.

❌ **Sai:**
> 1. Đầu tiên chúng ta cần để ý đến file `SKILL.md`.
> 2. Việc tìm dòng port là cần thiết.
> 3. Sẽ tốt hơn nếu đổi thành 8080.

### 3. Đánh số hợp lý (Numbered Lists vs Bullet Points)
- **Numbered lists (1, 2, 3...):** Chỉ dùng cho chuỗi hành động BẮT BUỘC THEO THỨ TỰ.
- **Bullet points (-, •):** Dùng cho checklist, liệt kê các tùy chọn (Options) không cần theo trình tự.

---

## Phần 2: Kỹ Thuật Viết Formatting

Sử dụng định dạng văn bản để điều hướng mắt người đọc đến các điểm cốt yếu:

**1. In đậm (Bold text):**
- Tên Nút bấm, Menu UI.
- Tên tham số quan trọng.
- Ví dụ: Nhấp vào **Settings** > **Advanced** > **Network**.

**2. Inline Code (Backticks ` ):**
- Tên file, thư mục (`config.json`, `/process/`).
- Function name, biến, hằng số (`start_server()`, `PORT`).
- Keyboard shortcuts (`Ctrl` + `C`).

**3. Code Blocks:**
Dùng cho commands (terminal) hoặc config code. Luôn khai báo ngôn ngữ để hệ thống highlight đúng.
```bash
npm install express
```

**4. Khối Cảnh Báo (Callouts/Blockquotes):**
Dùng blockquotes ( > ) hoặc thẻ cảnh báo nếu có để nhấn mạnh các rủi ro.

> **⚠️ LƯU Ý QUAN TRỌNG:** Luôn backup database trước khi chạy lệnh drop table.

---

## Phần 3: Troubleshooting Format (Khắc Phục Sự Cố)

Khi viết phần xử lý lỗi, hãy dùng cấu trúc Chuẩn Đoán - Khắc Phục rõ ràng:

### Lỗi: [Tên Lỗi hoặc Message Lỗi Cụ Thể]
**Nguyên nhân:** Giải thích gọn trong 1 câu tại sao lỗi xuất hiện.
**Cách khắc phục:** 
1. Bước 1 làm gì.
2. Bước 2 làm gì.
3. Bước 3 xác minh (Verify) như thế nào.

---

## Phần 4: Giọng Văn & Tone

- **Trực tiếp, trung lập:** Xưng "bạn" (người dùng) nếu cần, hoặc bỏ qua nhân xưng và dùng thẳng động từ. 
- **Không lan man cảm xúc:** Bỏ qua các từ như "Thật tuyệt vời", "Đừng lo lắng", "Hi vọng rằng".
- **Tuyệt đối chính xác về path/term:** `/usr/bin/python` thay vì "thư mục python ở đâu đó trong usr".

---

## Phần 5: Checklist

Trước khi xuất bản Technical Guide:
- [ ] Mở đầu có nêu rõ mục đích của guide không?
- [ ] Các bước được đánh số có theo đúng trình tự không?
- [ ] Câu hướng dẫn có bắt đầu bằng Động Từ không?
- [ ] Tên file/phím tắt có được bọc trong `backticks` không?
- [ ] Tên giao diện/Nút bấm có được **in đậm** không?
- [ ] Có cảnh báo những bước dễ sai/rủi ro cao không?
- [ ] Không có câu nào dư thừa cảm xúc hay khen ngợi công cụ?

---

## Integration với IPO Framework

**Technical Guide trong IPO:**

```
INPUT Phase:
├─ Content type: Hướng dẫn, How-to, SOP
├─ Purpose: Chỉ dẫn từng bước để làm một việc gì đó
├─ Audience: Bất cứ ai cần thực thi task
└─ Platform: Dokumentation, Wiki, Internal Repo

PROCESS Phase:
├─ nghien-cuu.md → (Nếu cần tìm hiểu technical terms)
└─ kiem-chung.md → (Xác minh lệnh bash/code có chạy thật không)

OUTPUT Phase:
├─ SKILL.md → Route to technical
├─ quy-tac-viet.md → Vietnamese rules (BẮT BUỘC)
└─ technical.md → Apply framework này
    ↓
    Hướng dẫn chi tiết, copy-paste dễ dàng
```

---

**Token budget:** ~1,800 tokens  
**Độ tự do:** Thấp (Ưu tiên format quy chuẩn strict).  
**Integration:** Có thể kết hợp `kiem-chung.md` để đảm bảo lệnh command chuẩn.  
**Best for:** Developers docs, SOP, Hướng dẫn nội bộ, Troubleshooting guides.
