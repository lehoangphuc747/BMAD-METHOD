# BMad CORE + BMad Method

[![Stable Version](https://img.shields.io/npm/v/bmad-method?color=blue&label=stable)](https://www.npmjs.com/package/bmad-method)
[![Alpha Version](https://img.shields.io/npm/v/bmad-method/alpha?color=orange&label=alpha)](https://www.npmjs.com/package/bmad-method)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen)](https://nodejs.org)
[![Discord](https://img.shields.io/badge/Discord-Join%20Community-7289da?logo=discord&logoColor=white)](https://discord.gg/gk8jAdXWmj)
[![Language](https://img.shields.io/badge/English-blue)](./README.md)
[![Tiếng Việt](https://img.shields.io/badge/Tiếng%20Việt-red)](./README.vi.md)

> **🚨 Thông Báo Phiên Bản Alpha**
>
> v6-alpha có chất lượng gần như beta—ổn định và được cải thiện đáng kể so với v4, nhưng tài liệu vẫn đang được hoàn thiện. Video mới sắp ra mắt trên [kênh YouTube BMadCode](https://www.youtube.com/@BMadCode)—đăng ký để nhận cập nhật!
>
> **Bắt Đầu:**
>
> - **Cài đặt v6 Alpha:** `npx bmad-method@alpha install`
> - **Cài đặt v4 ổn định:** `npx bmad-method install`
> - **Không chắc nên làm gì?** Tải bất kỳ agent nào và chạy `*workflow-init` để thiết lập hướng dẫn
> - **Người dùng v4:** [Xem tài liệu v4](https://github.com/bmad-code-org/BMAD-METHOD/tree/V4) hoặc [hướng dẫn nâng cấp](./docs/v4-to-v6-upgrade.md)

## Nền Tảng Hợp Tác Con Người-AI Toàn Cầu

**BMad-CORE** (**C**ollaboration **O**ptimized **R**eflection **E**ngine - Công Cụ Phản Tư Tối Ưu Hợp Tác) khuếch đại tiềm năng con người thông qua các AI agent chuyên biệt. Không giống như các công cụ thay thế tư duy, BMad-CORE hướng dẫn các quy trình làm việc phản tư giúp khai thác những ý tưởng tốt nhất của bạn và khả năng đầy đủ của AI.

**BMad-CORE** cung cấp năng lượng cho **BMad Method** (có lẽ đây là lý do bạn ở đây!), nhưng bạn cũng có thể sử dụng **BMad Builder** để tạo các agent, quy trình làm việc và module tùy chỉnh cho bất kỳ lĩnh vực nào—phát triển phần mềm, chiến lược kinh doanh, sáng tạo, học tập, và hơn thế nữa.

**🎯 Khuếch Đại Con Người** • **🎨 Không Phụ Thuộc Lĩnh Vực** • **⚡ Được Cung Cấp Bởi Agent**

## Mục Lục

- [BMad CORE + BMad Method](#bmad-core--bmad-method)
  - [Nền Tảng Hợp Tác Con Người-AI Toàn Cầu](#nền-tảng-hợp-tác-con-người-ai-toàn-cầu)
  - [Mục Lục](#mục-lục)
  - [BMad-CORE là gì?](#bmad-core-là-gì)
    - [Các Cải Tiến Core v6](#các-cải-tiến-core-v6)
    - [Triết Lý C.O.R.E.](#triết-lý-core)
  - [Các Module](#các-module)
    - [BMad Method (BMM) - Phát Triển Agile Được Điều Khiển Bởi AI](#bmad-method-bmm---phát-triển-agile-được-điều-khiển-bởi-ai)
      - [Điểm Nổi Bật v6](#điểm-nổi-bật-v6)
  - [🚀 Bắt Đầu Nhanh](#-bắt-đầu-nhanh)
    - [BMad Builder (BMB) - Tạo Giải Pháp Tùy Chỉnh](#bmad-builder-bmb---tạo-giải-pháp-tùy-chỉnh)
    - [Creative Intelligence Suite (CIS) - Đổi Mới & Sáng Tạo](#creative-intelligence-suite-cis---đổi-mới--sáng-tạo)
  - [Cài Đặt](#cài-đặt)
  - [🎯 Làm Việc Với Agents & Lệnh](#-làm-việc-với-agents--lệnh)
    - [Phương Pháp 1: Menu Agent (Khuyến Nghị Cho Người Mới)](#phương-pháp-1-menu-agent-khuyến-nghị-cho-người-mới)
    - [Phương Pháp 2: Lệnh Slash Trực Tiếp](#phương-pháp-2-lệnh-slash-trực-tiếp)
    - [Phương Pháp 3: Thực Thi Chế Độ Party](#phương-pháp-3-thực-thi-chế-độ-party)
  - [Tính Năng Chính](#tính-năng-chính)
    - [🎨 Tùy Chỉnh An Toàn Khi Cập Nhật](#-tùy-chỉnh-an-toàn-khi-cập-nhật)
    - [🚀 Cài Đặt Thông Minh](#-cài-đặt-thông-minh)
    - [📁 Kiến Trúc Sạch](#-kiến-trúc-sạch)
    - [📄 Chia Nhỏ Tài Liệu (Nâng Cao)](#-chia-nhỏ-tài-liệu-nâng-cao)
  - [Tài Liệu](#tài-liệu)
  - [Cộng Đồng & Hỗ Trợ](#cộng-đồng--hỗ-trợ)
  - [Phát Triển & Kiểm Tra Chất Lượng](#phát-triển--kiểm-tra-chất-lượng)
    - [Kiểm Thử & Xác Thực](#kiểm-thử--xác-thực)
    - [Chất Lượng Code](#chất-lượng-code)
    - [Build & Phát Triển](#build--phát-triển)
  - [Đóng Góp](#đóng-góp)
  - [Giấy Phép](#giấy-phép)

---

## BMad-CORE là gì?

Framework nền tảng cung cấp năng lượng cho tất cả các module BMad:

- **Điều Phối Agent** - Các nhân cách AI chuyên biệt với chuyên môn lĩnh vực
- **Công Cụ Workflow** - Quy trình nhiều bước được hướng dẫn với các thực hành tốt nhất tích hợp sẵn
- **Kiến Trúc Module** - Mở rộng với các module theo lĩnh vực (BMM, BMB, CIS, tùy chỉnh)
- **Tích Hợp IDE** - Hoạt động với Claude Code, Cursor, Windsurf, VS Code, và nhiều hơn nữa
- **Tùy Chỉnh An Toàn Khi Cập Nhật** - Cấu hình của bạn tồn tại qua tất cả các cập nhật

### Các Cải Tiến Core v6

- **🎨 Tùy Chỉnh Agent** - Chỉnh sửa tên, vai trò, tính cách qua `bmad/_cfg/agents/` **[→ Hướng Dẫn Tùy Chỉnh](./docs/agent-customization-guide.md)**
- **🌐 Đa Ngôn Ngữ** - Cài đặt ngôn ngữ độc lập cho giao tiếp và đầu ra
- **👤 Cá Nhân Hóa** - Agents thích ứng với tên, trình độ kỹ năng và sở thích của bạn
- **🔄 Cấu Hình Bền Vững** - Tùy chỉnh tồn tại qua các cập nhật module
- **⚙️ Cài Đặt Linh Hoạt** - Cấu hình theo module hoặc toàn cục
- **📦 Web Bundles** - Chia sẻ agents trong Gemini Gems và Custom GPTs **[→ Hướng Dẫn Web Bundles](./docs/web-bundles-gemini-gpt-guide.md)**

### Triết Lý C.O.R.E.

- **C**ollaboration (Hợp Tác): Đối tác con người-AI tận dụng các điểm mạnh bổ sung
- **O**ptimized (Tối Ưu): Quy trình được kiểm chứng trong thực tế để đạt hiệu quả tối đa
- **R**eflection (Phản Tư): Câu hỏi chiến lược mở khóa các giải pháp đột phá
- **E**ngine (Công Cụ): Framework điều phối 19+ agent chuyên biệt và 50+ workflow

BMad-CORE không cho bạn câu trả lời—nó giúp bạn **khám phá giải pháp tốt hơn** thông qua phản tư có hướng dẫn.

## Các Module

### BMad Method (BMM) - Phát Triển Agile Được Điều Khiển Bởi AI

Framework agile được điều khiển bởi AI mang tính cách mạng cho phát triển phần mềm và game. Tự động thích ứng từ sửa lỗi đơn lẻ đến hệ thống quy mô doanh nghiệp.

#### Điểm Nổi Bật v6

**🎯 Trí Tuệ Thích Ứng Quy Mô (3 Track Lập Kế Hoạch)**

Tự động điều chỉnh độ sâu lập kế hoạch và tài liệu dựa trên nhu cầu dự án:

- **Quick Flow Track:** Triển khai nhanh (chỉ tech-spec) - sửa lỗi, tính năng nhỏ, phạm vi rõ ràng
- **BMad Method Track:** Lập kế hoạch đầy đủ (PRD + Architecture + UX) - sản phẩm, nền tảng, tính năng phức tạp
- **Enterprise Method Track:** Lập kế hoạch mở rộng (BMad Method + Security/DevOps/Test) - yêu cầu doanh nghiệp, tuân thủ

**🏗️ Phương Pháp Bốn Giai Đoạn**

1. **Giai Đoạn 1: Phân Tích** (Tùy chọn) - Brainstorming, nghiên cứu, brief sản phẩm
2. **Giai Đoạn 2: Lập Kế Hoạch** (Bắt buộc) - PRD/tech-spec/GDD thích ứng quy mô
3. **Giai Đoạn 3: Giải Pháp** (Phụ thuộc track) - Kiến trúc, (Sắp ra mắt: bảo mật, DevOps, chiến lược kiểm thử)
4. **Giai Đoạn 4: Triển Khai** (Lặp lại) - Phát triển tập trung vào story với ngữ cảnh vừa đủ

**🤖 12 Agent Chuyên Biệt**

PM • Analyst • Architect • Scrum Master • Developer • Test Architect (TEA) • UX Designer • Technical Writer • Game Designer • Game Developer • Game Architect • BMad Master (Điều Phối Viên)

**📚 Tài Liệu**

- **[Trung Tâm Tài Liệu Đầy Đủ](./src/modules/bmm/docs/README.md)** - Bắt đầu tại đây cho tất cả hướng dẫn BMM
- **[Hướng Dẫn Bắt Đầu Nhanh](./src/modules/bmm/docs/quick-start.md)** - Bắt đầu xây dựng trong 15 phút
- **[Hướng Dẫn Agents](./src/modules/bmm/docs/agents-guide.md)** - Gặp gỡ tất cả 12 agents (đọc 45 phút)
- **[34 Hướng Dẫn Workflow](./src/modules/bmm/docs/README.md#-workflow-guides)** - Tham khảo đầy đủ theo từng giai đoạn
- **[Tổng Quan Module BMM](./src/modules/bmm/README.md)** - Cấu trúc module và liên kết nhanh

---

## 🚀 Bắt Đầu Nhanh

**Sau khi cài đặt** (xem [Cài Đặt](#cài-đặt) bên dưới), chọn đường dẫn của bạn:

**Ba Track Lập Kế Hoạch:**

1. **⚡ Quick Flow Track** - Sửa lỗi và tính năng nhỏ
   - 🐛 Sửa lỗi trong vài phút
   - ✨ Tính năng nhỏ (2-3 thay đổi liên quan)
   - 🚀 Tạo mẫu nhanh
   - **[→ Hướng Dẫn Quick Spec Flow](./src/modules/bmm/docs/quick-spec-flow.md)**

2. **📋 BMad Method Track** - Sản phẩm và nền tảng
   - Lập kế hoạch đầy đủ (PRD/GDD)
   - Quyết định kiến trúc
   - Triển khai tập trung vào story
   - **[→ Hướng Dẫn Bắt Đầu Nhanh Đầy Đủ](./src/modules/bmm/docs/quick-start.md)**

3. **🏢 Dự Án Brownfield** - Thêm vào codebase hiện có
   - Tài liệu hóa code hiện có trước
   - Sau đó chọn Quick Flow hoặc BMad Method
   - **[→ Hướng Dẫn Brownfield](./src/modules/bmm/docs/brownfield-guide.md)**

**Không chắc chọn đường dẫn nào?** Chạy `*workflow-init` và để BMM phân tích mục tiêu dự án của bạn và đề xuất track phù hợp.

**[📚 Tìm Hiểu Thêm: Hệ Thống Thích Ứng Quy Mô](./src/modules/bmm/docs/scale-adaptive-system.md)** - Cách BMM thích ứng qua ba track lập kế hoạch

---

### BMad Builder (BMB) - Tạo Giải Pháp Tùy Chỉnh

Xây dựng agents, workflows và modules của riêng bạn sử dụng framework BMad-CORE.

**Những Gì Bạn Có Thể Xây Dựng:**

- **Custom Agents** - Chuyên gia lĩnh vực với kiến thức chuyên biệt
- **Guided Workflows** - Quy trình nhiều bước cho bất kỳ tác vụ nào
- **Complete Modules** - Giải pháp đầy đủ cho các lĩnh vực cụ thể
- **Ba Loại Agent** - Module đầy đủ, hybrid, hoặc độc lập

**Hoàn Hảo Cho:** Tạo giải pháp theo lĩnh vực (pháp lý, y tế, tài chính, giáo dục, sáng tạo, v.v.) hoặc mở rộng BMM với workflows phát triển tùy chỉnh.

**Tài Liệu:**

- **[Tổng Quan Module BMB](./src/modules/bmb/README.md)** - Tham khảo đầy đủ
- **[Workflow Tạo Agent](./src/modules/bmb/workflows/create-agent/README.md)** - Xây dựng custom agents
- **[Tạo Workflow](./src/modules/bmb/workflows/create-workflow/README.md)** - Thiết kế quy trình có hướng dẫn
- **[Tạo Module](./src/modules/bmb/workflows/create-module/README.md)** - Đóng gói giải pháp đầy đủ

### Creative Intelligence Suite (CIS) - Đổi Mới & Sáng Tạo

Hỗ trợ sáng tạo được cung cấp bởi AI sử dụng phương pháp và kỹ thuật đã được chứng minh.

**5 Workflow Tương Tác:**

- **Brainstorming** - Tạo và tinh chỉnh ý tưởng với 30+ kỹ thuật
- **Design Thinking** - Giải quyết vấn đề tập trung vào con người
- **Problem Solving** - Kỹ thuật đột phá có hệ thống
- **Innovation Strategy** - Tư duy mô hình kinh doanh đột phá
- **Storytelling** - Framework kể chuyện hấp dẫn

**5 Agent Chuyên Biệt:** Mỗi agent có phong cách hỗ trợ và chuyên môn lĩnh vực độc đáo

**Tài Nguyên Chia Sẻ:** Workflows CIS được sử dụng bởi các module khác (BMM's `brainstorm-project` sử dụng brainstorming của CIS)

**Tài Liệu:**

- **[Tổng Quan Module CIS](./src/modules/cis/README.md)** - Tham khảo đầy đủ
- **[Hướng Dẫn Workflows CIS](./src/modules/cis/workflows/README.md)** - Tất cả 5 workflow sáng tạo

---

## Cài Đặt

**Yêu Cầu:** Node.js v20+ ([Tải xuống](https://nodejs.org))

```bash
# v6 Alpha (khuyến nghị cho dự án mới)
npx bmad-method@alpha install

# v4 ổn định (sản xuất)
npx bmad-method install
```

Trình cài đặt cung cấp:

1. **Lựa Chọn Module** - Chọn BMM, BMB, CIS (hoặc tất cả)
2. **Cấu Hình** - Tên của bạn, tùy chọn ngôn ngữ, tùy chọn game dev
3. **Tích Hợp IDE** - Thiết lập tự động cho IDE của bạn

**Cài đặt tạo:**

```
your-project/
└── bmad/
    ├── core/         # Core framework + BMad Master agent
    ├── bmm/          # BMad Method (12 agents, 34 workflows)
    ├── bmb/          # BMad Builder (1 agent, 7 workflows)
    ├── cis/          # Creative Intelligence (5 agents, 5 workflows)
    └── _cfg/         # Tùy chỉnh của bạn (tồn tại qua cập nhật)
        └── agents/   # Các file tùy chỉnh agent
```

**Bước Tiếp Theo:**

1. Tải bất kỳ agent nào trong IDE của bạn
2. Chạy `*workflow-init` để thiết lập đường dẫn workflow dự án của bạn
3. Làm theo hướng dẫn [Bắt Đầu Nhanh](#-bắt-đầu-nhanh) ở trên để chọn track lập kế hoạch của bạn

**Thay Thế:** [**Web Bundles**](./docs/USING_WEB_BUNDLES.md) - Sử dụng agents BMAD trong Claude Projects, ChatGPT, hoặc Gemini mà không cần cài đặt

---

## 🎯 Làm Việc Với Agents & Lệnh

**Nhiều Cách Thực Thi Workflows:**

BMad linh hoạt - bạn có thể thực thi workflows theo nhiều cách tùy thuộc vào sở thích và IDE của bạn:

### Phương Pháp 1: Menu Agent (Khuyến Nghị Cho Người Mới)

1. **Tải một agent** trong IDE của bạn (xem [hướng dẫn theo IDE](./docs/ide-info/))
2. **Chờ menu** xuất hiện hiển thị các workflows có sẵn
3. **Nói với agent** cần chạy gì bằng ngôn ngữ tự nhiên hoặc phím tắt:
   - Tự nhiên: "Run workflow-init"
   - Phím tắt: `*workflow-init`
   - Số menu: "Run option 2"

### Phương Pháp 2: Lệnh Slash Trực Tiếp

**Thực thi workflows trực tiếp** sử dụng lệnh slash:

```
/bmad:bmm:workflows:workflow-init
/bmad:bmm:workflows:prd
/bmad:bmm:workflows:dev-story
```

**Mẹo:** Mặc dù bạn có thể chạy những lệnh này mà không cần tải agent trước, **vẫn khuyến nghị tải agent** - nó có thể tạo sự khác biệt với một số workflows.

**Lợi Ích:**

- ✅ Kết hợp bất kỳ agent nào với bất kỳ workflow nào
- ✅ Chạy workflows không có trong menu của agent đã tải
- ✅ Truy cập nhanh hơn cho người dùng có kinh nghiệm biết tên lệnh

### Phương Pháp 3: Thực Thi Chế Độ Party

**Chạy workflows với hợp tác multi-agent:**

1. Bắt đầu chế độ party: `/bmad:core:workflows:party-mode`
2. Thực thi bất kỳ workflow nào - **toàn bộ nhóm hợp tác trên đó**
3. Nhận các góc nhìn đa dạng từ nhiều agent chuyên biệt

**Hoàn hảo cho:** Quyết định chiến lược, workflows phức tạp, tác vụ liên chức năng

---

> **📌 Lưu Ý Theo IDE:**
>
> Định dạng lệnh slash khác nhau tùy theo IDE:
>
> - **Claude Code:** `/bmad:bmm:workflows:prd`
> - **Cursor/Windsurf:** Có thể sử dụng cú pháp khác - kiểm tra [tài liệu](./docs/ide-info/) của IDE bạn
> - **VS Code với Copilot Chat:** Cú pháp có thể khác
>
> Xem **[Hướng Dẫn Tích Hợp IDE](./docs/ide-info/)** cho định dạng lệnh của IDE cụ thể của bạn.

---

## Tính Năng Chính

### 🎨 Tùy Chỉnh An Toàn Khi Cập Nhật

Chỉnh sửa agents mà không chạm vào các file core:

- Ghi đè tên, tính cách, chuyên môn của agent qua `bmad/_cfg/agents/`
- Tùy chỉnh tồn tại qua tất cả các cập nhật
- Hỗ trợ đa ngôn ngữ (giao tiếp + đầu ra)
- Cấu hình theo module hoặc toàn cục

### 🚀 Cài Đặt Thông Minh

Thiết lập thông minh thích ứng với môi trường của bạn:

- Tự động phát hiện cài đặt v4 để nâng cấp mượt mà
- Cấu hình tích hợp IDE (Claude Code, Cursor, Windsurf, VS Code)
- Giải quyết phụ thuộc cross-module
- Tạo manifests agent/workflow thống nhất

### 📁 Kiến Trúc Sạch

Mọi thứ ở một nơi:

- Thư mục `bmad/` duy nhất (không có file rải rác)
- Modules tồn tại song song (core, bmm, bmb, cis)
- Cấu hình của bạn trong `_cfg/` (tồn tại qua cập nhật)
- Dễ dàng kiểm soát phiên bản hoặc loại trừ

### 📄 Chia Nhỏ Tài Liệu (Nâng Cao)

Tối ưu hóa tùy chọn cho dự án lớn (BMad Method và Enterprise tracks):

- **Tiết Kiệm Token Lớn** - Workflows Giai đoạn 4 chỉ tải các phần cần thiết (giảm 90%+)
- **Hỗ Trợ Tự Động** - Tất cả workflows xử lý tài liệu nguyên vẹn hoặc đã chia nhỏ một cách liền mạch
- **Thiết Lập Dễ Dàng** - Công cụ tích hợp chia tài liệu theo tiêu đề
- **Phát Hiện Thông Minh** - Workflows tự động phát hiện định dạng

**[→ Hướng Dẫn Chia Nhỏ Tài Liệu](./docs/document-sharding-guide.md)**

---

## Tài Liệu

**Tài Liệu Module:**

- **[Trung Tâm Tài Liệu BMM Đầy Đủ](./src/modules/bmm/docs/README.md)** - Tất cả hướng dẫn BMM, FAQs, xử lý sự cố
- **[Tham Khảo Module BMB](./src/modules/bmb/README.md)** - Xây dựng custom agents và workflows
- **[Hướng Dẫn Workflows CIS](./src/modules/cis/workflows/README.md)** - Workflows hỗ trợ sáng tạo

**Tùy Chỉnh & Chia Sẻ:**

- **[Hướng Dẫn Tùy Chỉnh Agent](./docs/agent-customization-guide.md)** - Tùy chỉnh tên, nhân cách và hành vi của agent
- **[Web Bundles cho Gemini & GPT](./docs/web-bundles-gemini-gpt-guide.md)** - Sử dụng agents BMad trong Gemini Gems và Custom GPTs

**Tài Nguyên Bổ Sung:**

- **[Mục Lục Tài Liệu](./docs/index.md)** - Tất cả tài liệu dự án
- **[Hướng Dẫn Nâng Cấp v4 sang v6](./docs/v4-to-v6-upgrade.md)** - Hướng dẫn di chuyển
- **[Hướng Dẫn Công Cụ CLI](./tools/cli/README.md)** - Tham khảo trình cài đặt và công cụ build
- **[Hướng Dẫn Đóng Góp](./CONTRIBUTING.md)** - Cách đóng góp

---

## Cộng Đồng & Hỗ Trợ

- 💬 **[Cộng Đồng Discord](https://discord.gg/gk8jAdXWmj)** - Nhận trợ giúp, chia sẻ dự án (#general-dev, #bugs-issues)
- 🐛 **[GitHub Issues](https://github.com/bmad-code-org/BMAD-METHOD/issues)** - Báo cáo lỗi, yêu cầu tính năng
- 🎥 **[Kênh YouTube](https://www.youtube.com/@BMadCode)** - Video hướng dẫn và walkthrough
- ⭐ **[Star repo này](https://github.com/bmad-code-org/BMAD-METHOD)** - Cập nhật về các bản phát hành

---

## Phát Triển & Kiểm Tra Chất Lượng

**Cho người đóng góp làm việc trên codebase BMAD:**

**Yêu Cầu:** Node.js 22+ (xem `.nvmrc`). Chạy `nvm use` để chuyển sang phiên bản đúng.

### Kiểm Thử & Xác Thực

```bash
# Chạy tất cả kiểm tra chất lượng (toàn diện - sử dụng trước khi push)
npm test

# Các bộ kiểm thử riêng lẻ
npm run test:schemas     # Xác thực schema agent (dựa trên fixture)
npm run test:install     # Kiểm thử component cài đặt (biên dịch)
npm run validate:schemas # Xác thực schema YAML
npm run validate:bundles # Tính toàn vẹn web bundle
```

### Chất Lượng Code

```bash
# Kiểm tra lint
npm run lint

# Tự động sửa các vấn đề linting
npm run lint:fix

# Kiểm tra format
npm run format:check

# Tự động format tất cả các file
npm run format:fix
```

### Build & Phát Triển

```bash
# Bundle cho triển khai web
npm run bundle

# Kiểm tra cài đặt cục bộ
npm run install:bmad
```

**Pre-commit Hook:** Tự động sửa các file đã thay đổi (lint-staged) + xác thực mọi thứ (npm test)
**CI:** GitHub Actions chạy tất cả kiểm tra chất lượng song song trên mọi PR

---

## Đóng Góp

Chúng tôi hoan nghênh đóng góp! Xem **[CONTRIBUTING.md](CONTRIBUTING.md)** để biết:

- Hướng dẫn đóng góp code
- Cải thiện tài liệu
- Phát triển module
- Báo cáo vấn đề

---

## Giấy Phép

**Giấy Phép MIT** - Xem [LICENSE](LICENSE) để biết chi tiết

**Thương Hiệu:** BMAD™ và BMAD-METHOD™ là thương hiệu của BMad Code, LLC.

---

[![Contributors](https://contrib.rocks/image?repo=bmad-code-org/BMAD-METHOD)](https://github.com/bmad-code-org/BMAD-METHOD/graphs/contributors)

<sub>Được xây dựng bằng ❤️ cho cộng đồng hợp tác con người-AI</sub>

