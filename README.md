# Arctic Factory Preset

Bộ skill và template **speckit** tiếng Việt, chuẩn hoá quy trình phát triển tính năng cho các dự án sử dụng [Spec Kit](https://github.com/github-spec-kit/spec-kit).

## Yêu cầu

- [Spec Kit (Specify CLI)](https://github.com/github/spec-kit) đã được cài đặt

## Cài đặt

### Cài từ GitHub Release (khuyên dùng)

```bash
specify preset add --from https://github.com/nShieldSolo/ArcticFactory.Preset/releases/latest/download/arctic-factory-preset-v0.0.3.zip
```

### Cài từ repository GitHub

```bash
specify preset add --from https://github.com/nShieldSolo/ArcticFactory.Preset.git
```

### Xác nhận cài đặt thành công

```bash
# Kiểm tra preset đã được đăng ký
specify preset list

# Kiểm tra template phân giải đúng
specify preset resolve spec-template

# Kiểm tra skill phân giải đúng
specify preset resolve speckit-specify
```

### Gỡ cài đặt

```bash
specify preset remove arctic-factory
```

## Nội dung Preset

### Templates

| Tên | Loại | Mô tả |
|-----|------|--------|
| `spec-template` | template | Template đặc tả tính năng tùy chỉnh |

### Skills (Lệnh AI Agent)

| Tên Skill | Lệnh | Mô tả |
|-----------|------|--------|
| `speckit-specify` | `/speckit.specify` | Tạo mới hoặc cập nhật đặc tả tính năng |
| `speckit-clarify` | `/speckit.clarify` | Làm rõ đặc tả bằng câu hỏi có chọn lọc |
| `speckit-plan` | `/speckit.plan` | Lập kế hoạch triển khai |
| `speckit-tasks` | `/speckit.tasks` | Tạo tasks.md có thể thực thi |
| `speckit-implement` | `/speckit.implement` | Thực thi toàn bộ tasks.md |
| `speckit-analyze` | `/speckit.analyze` | Phân tích chất lượng chéo spec/plan/tasks |
| `speckit-checklist` | `/speckit.checklist` | Tạo checklist tùy chỉnh |
| `speckit-constitution` | `/speckit.constitution` | Tạo/cập nhật hiến pháp dự án |
| `speckit-taskstoissues` | `/speckit.taskstoissues` | Chuyển tasks thành GitHub Issues |

## Phát triển & Test

```bash
# Cài local để test (trỏ thẳng vào thư mục preset)
specify preset add --dev ./arctic-factory

# Kiểm tra độ phân giải template
specify preset resolve spec-template

# Kiểm tra skill
specify preset resolve speckit-specify

# Gỡ cài đặt khi xong test
specify preset remove arctic-factory
```

## Manifest Reference (`preset.yml`)

| Trường | Mô tả |
|--------|--------|
| `schema_version` | Luôn là `"1.0"` |
| `preset.id` | Chữ thường, dấu gạch ngang |
| `preset.version` | Semantic version (vd: `1.0.0`) |
| `requires.speckit_version` | Ràng buộc phiên bản (vd: `>=0.1.0`) |
| `provides.templates` | Danh sách template override |
| `provides.skills` | Danh sách skill override |

## License

MIT
