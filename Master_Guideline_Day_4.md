# TỔNG QUAN KHÓA HỌC: EB MASTERCLASS KHOÁ 1

## 🎯 1. BẢN LỀ HOẠT ĐỘNG & NGUYÊN TẮC VẬN HÀNH

- **Tư Duy Vòng Lặp Phản Biện (Critique Loop):** Khác với Ngày 1 (AI sinh kết quả một phát ăn ngay), ở Ngày 4 bạn phải đóng vai một **Vị Giám Khảo Khó Tính**. Không bao giờ được duyệt bản nháp đầu tiên. Buộc AI tự soi chiếu bản nháp với Tiêu chí (Quality Gate) để bắt nó tự tát vào mặt mình và sửa lỗi.
- **Tư Duy Manager (Working Backward):** Mọi công cụ sản xuất (Landing Page, MC Script, Bài đăng Social) đều phải móc xích truy ngược về rễ của nó là Master Plan và Bộ Tiêu chí Chiến lược. Nói "KHÔNG" với lối làm việc chắp vá, tiện đoạn nào gõ prompt đoạn đó.
- **Lễ Bế Mạc & Đóng Gói (Closure Protocol):** Kết thúc mỗi Use Case, học viên BẮT BUỘC phải thực hiện Nghi thức Bế mạc (Viết Report, Lesson Learned) và Trích xuất System Prompt thành "Năng lực Bỏ túi" tái sử dụng suốt vòng đời sự nghiệp.

---

## 🧰 2. NÂNG CẤP AI AGENT: CÀI ĐẶT SKILL & WORKFLOW VÀO WORKSPACE

> Ngày 4 không chỉ dừng ở việc **sử dụng** AI, mà còn dạy bạn cách **dạy lại AI**. Phần này hướng dẫn bạn cài đặt bộ công cụ `Skill Packaging` và Workflow `/buildskill` để biến tri thức cá nhân thành "Năng lực bỏ túi" cho AI Agent tái sử dụng mãi mãi.

### 📚 2.1. Đọc hiểu tài liệu nền tảng (KWSR Modules)

Trước khi cài đặt, hãy đọc **tuần tự** các tài liệu trong thư mục `KWSR_Modules/` để nắm vững hệ sinh thái:

| Thứ tự | File                                        | Nội dung cốt lõi                                                                       |
| :------: | :------------------------------------------ | :---------------------------------------------------------------------------------------- |
|    1    | `00_Mo_dau.md`                            | Tổng quan Framework KWSR (Knowledge – Workflow – Skill – Rule)                        |
|    2    | `03_Skill.md`                             | Hiểu Skill là gì, vai trò trong hệ sinh thái Agent                                  |
|    3    | `02_Workflow.md`                          | Hiểu Workflow là gì, cách nó điều phối Skill                                      |
|    4    | **`S-66_skill-packaging/SKILL.md`** | ⭐ Tài liệu lõi — Quy trình đóng gói Skill chuẩn Antigravity                     |
|    5    | **`W-56_buildskill.md`**            | ⭐ Workflow vận hành — 4 mode: BUILD, OPTIMIZE_TRIGGER, EVALUATE, OPTIMIZE_INSTRUCTION |

> [!IMPORTANT]
> Hai file đánh dấu ⭐ là **tài liệu thực chiến**. Đọc kỹ chúng trước khi cài đặt.

### 🔧 2.2. Cài đặt Skill `skill-packaging` vào workspace

**Skill** là file hướng dẫn mà AI Agent tự động đọc khi nhận diện bạn đang cần chuyên môn đó. Để cài đặt:

**Bước 1 — Xác định thư mục Skills trong workspace:**

Workspace AI Agent của bạn cần có cấu trúc thư mục `.agent/skills/`. Nếu chưa có, tạo mới:

```
Workspace_cua_ban/
└── .agent/
    ├── skills/          ← Nơi chứa các Skill
    └── workflows/       ← Nơi chứa các Workflow
```

**Bước 2 — Copy toàn bộ thư mục Skill:**

Copy thư mục `S-66_skill-packaging/skill-packaging/` vào đường dẫn `.agent/skills/` trong workspace của bạn:

```
.agent/skills/
└── skill-packaging/
    └── SKILL.md         ← File lõi, AI Agent tự nhận diện và đọc
```

> [!TIP]
> Bạn có thể nhờ AI Agent thực hiện việc này bằng prompt:
> *"Hãy copy thư mục `KWSR_Modules/S-66_skill-packaging/skill-packaging/` vào `.agent/skills/` trong workspace của tôi."*

**Bước 3 — Xác nhận cài đặt:**

Hỏi AI Agent: *"Liệt kê tất cả skills hiện có trong workspace."* — Agent sẽ quét thư mục `.agent/skills/` và liệt kê `skill-packaging` nếu cài đặt thành công.

### ⚡ 2.3. Cài đặt Workflow `/buildskill` vào workspace

**Workflow** là quy trình từng bước mà AI Agent tuân theo khi bạn gọi lệnh slash (VD: `/buildskill`). Để cài đặt:

**Bước 1 — Copy file Workflow:**

Copy file `W-56_buildskill.md` vào thư mục `.agent/workflows/` trong workspace:

```
.agent/workflows/
└── buildskill.md        ← Đổi tên bỏ prefix "W-56_" cho gọn
```

> [!NOTE]
> Tên file workflow (không tính `.md`) chính là tên lệnh slash. File `buildskill.md` → lệnh `/buildskill`.

**Bước 2 — Xác nhận cài đặt:**

Gõ `/buildskill` trong chat với AI Agent. Nếu Agent nhận diện và mô tả được 4 modes (BUILD, OPTIMIZE_TRIGGER, EVALUATE, OPTIMIZE_INSTRUCTION) thì cài đặt thành công.

### 🎮 2.4. Sử dụng: Đóng gói Skill đầu tiên của bạn

Sau khi cài đặt xong, hãy thử quy trình đóng gói Skill đầu tiên:

1. **Khởi tạo:** Gọi `/buildskill BUILD` → Agent sẽ hỏi bạn về chuyên môn cần đóng gói rồi tạo thư mục và file `SKILL.md` chuẩn.
2. **Tối ưu Trigger:** Gọi `/buildskill OPTIMIZE_TRIGGER` → Agent thiết kế bộ test để đảm bảo Skill được kích hoạt đúng lúc.
3. **Đánh giá:** Gọi `/buildskill EVALUATE` → Agent so sánh chất lượng có Skill vs. không có Skill.
4. **Tinh chỉnh:** Gọi `/buildskill OPTIMIZE_INSTRUCTION` → Agent phân tích kết quả đánh giá và cải thiện nội dung Skill.

> [!CAUTION]
> Đừng bỏ qua bước EVALUATE. Một Skill chưa qua kiểm định có thể khiến AI Agent hoạt động kém hơn so với không dùng Skill.

---

*Chúc các học viên EB Masterclass Khoá 1 chinh phục thành công Năng lực Quản trị Cấp cao bằng Trí Tuệ Nhân Tạo!*
