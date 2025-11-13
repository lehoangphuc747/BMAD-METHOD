# Hướng Dẫn Nâng Cấp BMad v4 lên v6

## Tổng Quan

BMad v6 là bản viết lại hoàn toàn với nhiều thay đổi lớn về kiến trúc. Tài liệu này giúp bạn chuyển dự án từ v4 sang v6.

---

## Tự Động Phát Hiện v4

Khi bạn chạy `npm run install:bmad` trên dự án có v4, trình cài đặt sẽ tự động phát hiện:

- **Thư mục legacy**: Các thư mục bắt đầu bằng `.bmad`, `bmad` (chữ thường), hoặc `Bmad`
- **Artifact lệnh IDE**: Thư mục bmad cũ trong cấu hình IDE (`.claude/commands/`, `.cursor/commands/`, ...)

### Quá Trình Phát Hiện

1. **Tự động backup module v4**: Tất cả thư mục `.bmad-*` được chuyển vào `v4-backup/` ở gốc dự án
   - Nếu đã có backup, sẽ thêm timestamp để tránh trùng
   - Ví dụ: `.bmad-core` → `v4-backup/.bmad-core`
   - File dự án và dữ liệu của bạn KHÔNG bị ảnh hưởng

2. **Khuyến nghị dọn dẹp lệnh IDE**: Nên xóa thủ công các lệnh IDE cũ
   - Nằm trong thư mục cấu hình IDE: `.claude/commands/`, `.cursor/commands/`, ...
   - Nếu không xóa, các lệnh này vẫn tham chiếu cấu trúc v4
   - Trình cài đặt sẽ cung cấp lệnh terminal copy/paste phù hợp nền tảng
   - Có thể bỏ qua bước này, nhưng xóa giúp tránh nhầm lẫn với lệnh v4

---

## Di Chuyển Module

### Module Đã Ngưng

| Module v4                     | Trạng thái v6                             |
| ----------------------------- | ----------------------------------------- |
| `.bmad-2d-phaser-game-dev`    | Đã tích hợp vào BMM                       |
| `.bmad-2d-unity-game-dev`     | Đã tích hợp vào BMM                       |
| `.bmad-godot-game-dev`        | Đã tích hợp vào BMM                       |
| `.bmad-*-game-dev` (bất kỳ)   | Đã tích hợp vào BMM                       |
| `.bmad-infrastructure-devops` | Ngưng - Sắp có agent devops mới trong BMM |
| `.bmad-creative-writing`      | Chưa chuyển - Sắp ra module mới           |

**Phát triển game**: Tất cả chức năng phát triển game đã được gom về module BMM (BMad Method). Workflow game sẽ tự động thích ứng loại game và engine bạn dùng.

---

## Thay Đổi Kiến Trúc

### Cấu Trúc Thư Mục

**Cấu trúc "Expansion Packs" v4:**

```
your-project/
├── .bmad-core/           # Thực chất là BMad Method
├── .bmad-game-dev/       # Expansion pack riêng
├── .bmad-creative-writing/
└── .bmad-infrastructure-devops/
```

**Cấu trúc hợp nhất v6:**

```
your-project/
└── bmad/                 # Một thư mục cài đặt duy nhất
    ├── core/            # Core framework (dùng cho mọi module)
    ├── bmm/             # BMad Method (dev phần mềm/game)
    ├── bmb/             # BMad Builder (tạo agent/workflow)
    ├── cis/             # Creative Intelligence Suite
    └── _cfg/            # Tuỳ chỉnh của bạn
        └── agents/      # File tuỳ chỉnh agent
```

### Thay Đổi Khái Niệm Chính

- **v4 `.bmad-core`**: Thực chất là BMad Method
- **v6 `bmad/core/`**: Framework core thực sự, dùng chung
- **v6 `bmad/bmm/`**: Module BMad Method
- **Nhận diện module**: Mỗi module đều có file `config.yaml`

---

## Di Chuyển Tiến Độ Dự Án

### Nếu Đã Hoàn Thành Giai Đoạn Lập Kế Hoạch (PRD/Kiến Trúc) với BMad Method:

Sau khi chạy trình cài đặt v6:

1. **Chạy workflow `workflow-init`** để thiết lập hệ thống workflow có hướng dẫn
2. **Chọn cấp độ dự án** khi được hỏi:
   - Nếu bạn đã đi hết workflow v4 (PRD → Kiến trúc → Stories), chọn **Level 3 hoặc 4**
   - Điều này giúp v6 biết bạn đã hoàn thành các giai đoạn lập kế hoạch và giải pháp
3. **Đường dẫn tài liệu**: Giữ nguyên đường dẫn cũ khi cài đặt
   - Vị trí mặc định PRD/Kiến trúc: `docs/`
   - Vị trí mặc định stories: `docs/stories/`
   - **Chấp nhận mặc định** nếu bạn đã dùng như v4

> **Lưu ý**: Workflow v6 xử lý được cả tài liệu sharded và unsharded. Không cần thay đổi cấu trúc file PRD/kiến trúc cũ.

### Nếu Đang Phát Triển (Đã Tạo/Thực Hiện Stories)

1. Cài đặt v6 như trên
2. Chạy `workflow-init` và chọn Level 3 hoặc 4
3. Khi muốn tiếp tục phát triển, chạy workflow **`sprint-planning`** (Giai đoạn 4)

---

## Di Chuyển Tuỳ Chỉnh Agent

### Tuỳ Chỉnh Agent v4

Ở v4, bạn có thể sửa trực tiếp file agent trong thư mục `.bmad-*`.

### Tuỳ Chỉnh Agent v6

**Tất cả tuỳ chỉnh** giờ nằm ở `bmad/_cfg/agents/` qua file customize:

**Ví dụ: Đổi tên agent và phong cách giao tiếp**

File: `bmad/_cfg/agents/bmm-pm.customize.yaml`

```yaml
# Tuỳ chỉnh agent PM
persona:
  name: 'Captain Jack' # Đổi tên agent
  role: 'Product Owner phong cách cướp biển'
  communication_style: |
    - Nói như cướp biển
    - Dùng ẩn dụ hàng hải cho khái niệm phần mềm
    - Luôn vui vẻ, phiêu lưu
```

**Cách hoạt động:**

- Agent gốc: `bmad/bmm/agents/pm.md`
- Tuỳ chỉnh: `bmad/_cfg/agents/bmm-pm.customize.yaml`
- Kết quả: Agent dùng tên/phong cách bạn chọn, update không ghi đè tuỳ chỉnh

---

## Tương Thích Tài Liệu

### Tài Liệu Sharded vs Unsharded

**Tin vui**: Khác v4, workflow v6 **rất linh hoạt** về cấu trúc tài liệu:

- ✅ Tài liệu sharded (chia nhiều file)
- ✅ Tài liệu unsharded (mỗi phần một file)
- ✅ Tuỳ chỉnh section theo loại dự án
- ✅ Kết hợp nhiều cách

Tất cả file workflow được quét tự động. Không cần cấu hình thủ công.

---

## Các Bước Cài Đặt

### 1. Clone Repo

```bash
git clone https://github.com/bmad-code-org/BMAD-METHOD
cd BMAD-METHOD
npm install
```

### 2. Chạy Installer trên Dự Án v4

```bash
npx bmad-method install
```

**Nhập đường dẫn đầy đủ tới dự án v4** khi được hỏi.

### 3. Làm Theo Hướng Dẫn Tương Tác

Trình cài đặt sẽ:

1. Phát hiện v4 và đề xuất backup thư mục `.bmad-*`
2. Đề xuất dọn dẹp (có thể bỏ qua)
3. Chọn module (khuyên dùng: BMM cho dev phần mềm/game)
4. Cấu hình core (tên, ngôn ngữ, ...)
5. Cấu hình tuỳ chọn module
6. Cấu hình tích hợp IDE

### 4. Chấp Nhận Đường Dẫn Mặc Định

Nếu bạn dùng:

- `docs/` cho PRD và kiến trúc
- `docs/stories/` cho file story

**Chấp nhận mặc định** khi cài đặt.

### 5. Khởi Tạo Workflow

Sau khi cài đặt:

1. **Load agent Analyst** - Xem hướng dẫn IDE cụ thể tại [docs/ide-info](./ide-info/) để kích hoạt agent:
   - [Claude Code](./ide-info/claude-code.md)
   - [Cursor](./ide-info/cursor.md)
   - [VS Code/Windsurf](./ide-info/) - Kiểm tra thư mục IDE

2. **Chờ menu agent** hiện ra

3. **Ra lệnh cho agent**: `*workflow-init` - v6 hỗ trợ fuzzy matching ngôn ngữ tự nhiên, bạn có thể gõ "workflow init" hoặc "khởi tạo workflow"

Nếu bạn chuyển từ v4, thường sẽ chọn **Level 3 hoặc 4** khi được hỏi - nếu đã hoàn thành PRD/kiến trúc ở v4.

---

## Checklist Sau Khi Di Chuyển

- [ ] Thư mục v4 đã backup vào `v4-backup/`
- [ ] Đã cài v6 vào thư mục `bmad/`
- [ ] Đã chạy `workflow-init` và chọn đúng cấp độ dự án
- [ ] Đã chuyển tuỳ chỉnh agent sang `bmad/_cfg/agents/` nếu cần
- [ ] Tích hợp IDE hoạt động (test bằng lệnh liệt kê agent)
- [ ] Đang phát triển: đã chạy workflow `sprint-planning`

---

## Hỗ Trợ

- **Discord**: [Tham gia cộng đồng BMad](https://discord.gg/gk8jAdXWmj)
- **Issues**: [GitHub Issue Tracker](https://github.com/bmad-code-org/BMAD-METHOD/issues)
- **Docs**: Xem `bmad/docs/` trong bản cài đặt để biết hướng dẫn IDE cụ thể
