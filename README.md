<div align="center">

# Arctic Factory Preset
*Bộ command và template tiếng Việt, chuẩn hoá quy trình phát triển tính năng cho các dự án sử dụng [Spec Kit](https://github.com/github-spec-kit/spec-kit).*

[![Spec Kit](https://img.shields.io/badge/Spec_Kit->=0.1.0-blue?style=flat-square)](https://github.com/github-spec-kit/spec-kit)
[![Language](https://img.shields.io/badge/Language-Vietnamese-red?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-MIT-gray?style=flat-square)](LICENSE)

⭐ Nếu bạn thấy bộ Preset này hữu ích, hãy để lại một star trên GitHub nhé!

[Tính năng](#-tính-năng-nổi-bật) • [Cài đặt](#-cài-đặt) • [Commands](#️-danh-sách-commands) • [Phát triển Local](#-dành-cho-phát-triển-thử-nghiệm-local)

</div>

Dự án này mang đến luồng làm việc tự động hoá 100% bằng tiếng Việt dành riêng cho Spec Kit, giúp các nhóm phát triển tại Việt Nam thiết kế và triển khai ứng dụng trơn tru hơn bằng AI Agent.

## 🤔 Yêu cầu hệ thống

- Đã cài đặt công cụ [Spec Kit (Specify CLI)](https://github.com/github/spec-kit) trên hệ thống của bạn.

## ✨ Tính năng nổi bật

- 🎯 **Quy trình chuẩn hóa**: Gồm đầy đủ các vòng đời (Specify → Clarify → Plan → Tasks → Implement → Analyze).
- 🇻🇳 **100% Tiếng Việt**: Prompt, command, template và hướng dẫn cho AI đều được tối ưu hóa cho tiếng Việt.
- 📋 **Checklist thông minh**: Tạo checklist (vai trò như Unit Tests cho Requirements) chất lượng dựa sát theo Specs.
- ⚙️ **Kết nối GitHub**: Hỗ trợ chuyển các đầu mục công việc (tasks) tự động thành GitHub issues có thể theo dõi.

## 🚀 Cài đặt

### Cài đặt qua URL (Khuyên dùng)

> [!TIP]
> Đây là cách nhanh nhất để nhận và đồng bộ trực tiếp phiên bản mới nhất từ kho lưu trữ về ứng dụng của bạn.

```bash
specify preset add --from https://github.com/nShieldSolo/ArcticFactory.Preset.git
```

**Hoặc cài từ một gói Release Github (ví dụ bản v0.0.5):**
```bash
specify preset add --from https://github.com/nShieldSolo/ArcticFactory.Preset/releases/latest/download/arctic-factory-preset-v0.0.5.zip
```

### Kiểm tra cấu hình cài đặt

Sau khi thêm preset, bạn có thể kiểm tra danh sách đã nhận chưa:

```bash
# Kiểm tra preset đã được đăng ký chưa
specify preset list

# Kiểm tra template và lệnh agent ưu tiên phân giải từ preset không
specify preset resolve spec-template
specify preset resolve speckit.specify
```

## 🛠️ Danh sách Commands

Bảng dưới đây liệt kê các lệnh AI Agent (Commands) mà Preset này đã override bằng prompt tiếng Việt cho dự án của bạn:

| Tên Command | Cú pháp AI Agent | Mục đích sử dụng |
|-------------|--------------------|-------------------|
| `speckit.specify` | `/speckit.specify` | Tạo mới hoặc cập nhật đặc tả tính năng dựa trên yêu cầu tự nhiên. |
| `speckit.clarify` | `/speckit.clarify` | Làm rõ đặc tả thông qua chuỗi các câu hỏi có độ ưu tiên cao đối với User. |
| `speckit.plan` | `/speckit.plan` | Xây dựng kế hoạch triển khai dựa trên Blueprint thiết kế. |
| `speckit.tasks` | `/speckit.tasks` | Bóc tách kế hoạch thành các task theo trình tự phụ thuộc cụ thể để Agent xử lý. |
| `speckit.implement` | `/speckit.implement` | Đọc luồng công việc và thi hành code cho các tasks đã lên cấu trúc. |
| `speckit.analyze` | `/speckit.analyze` | Lướt, đánh giá chéo và kiểm tra chất lượng của Specs, Plan, Tasks. |
| `speckit.checklist` | `/speckit.checklist` | Tạo danh sách kiểm tra tùy chỉnh mục tiêu dựa trên ngữ cảnh công việc. |
| `speckit.constitution` | `/speckit.constitution`| Quản lý và liên tục đồng bộ hiến pháp dự án với team phát triển. |
| `speckit.taskstoissues` | `/speckit.taskstoissues` | Đẩy tasks thẳng lên Github Issues trên remote tương ứng. |

## 🕹️ Dành cho phát triển thử nghiệm (Local)

Nếu bạn muốn tùy biến hoặc thử nghiệm preset trực tiếp từ máy cá nhân trước khi release:

```bash
# Thêm tham số --dev và trỏ đường dẫn tới thư mục arctic-factory
specify preset add --dev ./arctic-factory
```

Gỡ bỏ preset khi hoàn tất chu kỳ test:
```bash
specify preset remove arctic-factory
```
