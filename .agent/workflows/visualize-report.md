---
description: Visualize báo cáo/nội dung bất kỳ thành HTML Slides (interactive) và PDF (để gửi) — áp dụng cho mọi dự án
---

# Workflow: Visualize Báo cáo → HTML Slides + PDF

## Mục đích
Chuyển bất kỳ nội dung báo cáo (Markdown, văn bản, CSV...) thành:
1. **File HTML tương tác** (`*_Presentation.html`) — dùng để trình chiếu trực tiếp
2. **File PDF** (`*_Report_CEO.pdf`) — dùng để gửi email hoặc lưu trữ

---

## Bước 1 — Cung cấp nội dung báo cáo cho EmBot

Gửi nội dung cần visualize, có thể là:
- File `.md` đã có sẵn (dùng @mention)
- Paste nội dung trực tiếp
- Mô tả yêu cầu (EmBot sẽ xây từ đầu)

**Câu lệnh mẫu:**
```
@[đường dẫn tới file báo cáo.md] Em hãy visualize file này thành HTML slides và PDF để chị trình bày với [tên người nhận]
```

---

## Bước 2 — EmBot tạo file HTML Presentation (Interactive Slides)

EmBot sẽ tạo file `TenDuAn_Presentation.html` gồm:
- **5–7 slides** phong cách dark mode chuyên nghiệp
- Điều hướng bằng nút **← / →** hoặc phím mũi tên bàn phím
- Cover slide với KPI nổi bật, các sections rõ ràng

**Tiêu chuẩn thiết kế bắt buộc:**
- Font: Inter (Google Fonts)
- Theme: Dark navy (`#0A1628`) + Cyan/Blue gradient
- Slide size: `1280×720px` (16:9)
- Mỗi slide chứa `justify-content: center`, điều hướng dots ở dưới

---

## Bước 3 — EmBot tạo file HTML Print Version

EmBot tạo file `print_all_slides.html` riêng biệt với:
- Tất cả slides ghép liên tục trong 1 file
- CSS bắt buộc:
  ```css
  @page { size: 1280px 720px; margin: 0; }
  .slide {
    width: 1280px; height: 720px;
    overflow: hidden;
    page-break-after: always;
    display: flex; flex-direction: column;
    justify-content: space-evenly;   /* tránh khoảng đen thừa */
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
  }
  ```

---

## Bước 4 — Xuất PDF bằng Chrome Headless (terminal)

// turbo
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --disable-gpu \
  --print-to-pdf="[ĐƯỜNG_DẪN_OUTPUT].pdf" \
  --no-margins --no-pdf-header-footer \
  --paper-width=13.33 --paper-height=7.5 \
  "file://[ĐƯỜNG_DẪN_print_all_slides.html_ENCODED]"
```

**Tham số quan trọng:**
| Tham số | Giá trị | Lý do |
|---|---|---|
| `--paper-width` | `13.33` | 1280px ÷ 96dpi = 13.33 inch |
| `--paper-height` | `7.5` | 720px ÷ 96dpi = 7.5 inch |
| `--no-margins` | (flag) | Không thêm margin trắng |
| `--no-pdf-header-footer` | (flag) | Không in URL/timestamp |

**Câu lệnh mẫu nhanh** — thay `[TEN_DU_AN]` và `[THU_MUC]`:
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --disable-gpu \
  --print-to-pdf="/Users/huongnguyen/Employer Branding/[THU_MUC]/[TEN_DU_AN]_Report.pdf" \
  --no-margins --no-pdf-header-footer \
  --paper-width=13.33 --paper-height=7.5 \
  "file:///Users/huongnguyen/Employer%20Branding/[THU_MUC]/print_all_slides.html"
```

---

## Bước 5 — Kiểm tra output

EmBot tự kiểm tra bằng browser subagent. Nếu phát hiện:
- **Bị crop nội dung** → tăng `padding`, giảm font size, hoặc giảm số bullet/column
- **Khoảng đen thừa** → đổi `justify-content: center` → `space-evenly`
- **Màu mất** → kiểm tra `print-color-adjust: exact` đã có trong CSS

---

## Bước 5.5 — Rà soát & Đồng bộ (Bắt buộc trước khi giao PDF)

> ⚠️ **Bước này không thể bỏ.** Mọi chỉnh sửa ở `*_Presentation.html` phải được đồng bộ lại vào `print_all_slides.html` trước khi xuất PDF lần cuối.

### Checklist Rà soát Nội dung

| Hạng mục | Phải kiểm tra |
|---|---|
| Logo | Dùng `<img>` tag thật, đúng file logo, **không tự customize** |
| Nền slide | Đồng nhất — trắng hoặc tối tùy brand, **không lẫn lộn** |
| Footer | Không còn thông tin cũ/sai (tên công ty dư, logo text) |
| Bullets | Nội dung khớp giữa `Presentation.html` và `print_all_slides.html` |
| Typography | Thay toàn bộ em-dash `—` bằng `-` (hyphen) trong nội dung tiếng Việt |
| Quotes | Xác nhận với user trước khi giữ lại các câu trích dẫn |
| KPI boxes | Đúng số lượng — không thêm hoặc bỏ sót so với yêu cầu |

### Quy trình Đồng bộ

```
1. Hoàn chỉnh Presentation.html trước (phiên bản interactive)
2. Đối chiếu từng slide với print_all_slides.html
3. Copy/sync các thay đổi nội dung sang print_all_slides.html
4. Chạy lại Chrome headless để xuất PDF mới
5. Xác nhận file size PDF hợp lý (thường 600–1000 KB cho 6 slides)
```

> **Lý do cần bước này:** Sau nhiều vòng chỉnh sửa interactive, `print_all_slides.html` thường bị **lệch nội dung** so với `Presentation.html`. Nếu không đồng bộ, PDF xuất ra sẽ chứa nội dung cũ/sai mặc dù interactive slides đã đúng.

---


## Bộ file output chuẩn

| File | Mục đích |
|---|---|
| `TenBaoCao_Presentation.html` | Trình chiếu trực tiếp với CEO/Ban lãnh đạo |
| `print_all_slides.html` | File trung gian để Chrome in PDF (không cần gửi) |
| `TenBaoCao_Report_CEO.pdf` | Gửi email, lưu trữ, in |

---

## Cú pháp slash command (kích hoạt nhanh)

```
/visualize-report
```

Hoặc yêu cầu bằng ngôn ngữ tự nhiên:
```
"Em visualize báo cáo [tên] thành slide HTML và PDF giúp chị"
```

---

## Lưu ý kỹ thuật

- **Google Fonts** cần kết nối internet khi Chrome render. Nếu offline, thay bằng `font-family: system-ui, sans-serif`
- **Emoji** render khác nhau trên Mac vs Windows PDF viewer — không ảnh hưởng nội dung
- **Chrome headless** chạy trong 5-10 giây tùy số slides
- **Đường dẫn có dấu/khoảng trắng** phải encode URL (`%20` thay space, `%E1%BA%BF` cho ế...) khi dùng trong lệnh `file://`
- **Logo:** Dùng file logo thật qua thẻ `<img>` — chọn đúng phiên bản (logo đỏ/đen cho nền trắng, logo trắng cho nền tối). Tuyệt đối không customize logo bằng CSS.
- **Typography:** Trong nội dung tiếng Việt, dùng `-` (hyphen) thay em-dash `—` để đảm bảo hiển thị đồng nhất trên mọi PDF viewer và OS.
