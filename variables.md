# Biến trong Workflow n8n

## 1. Biến là gì?
Biến trong n8n là các giá trị tạm được lưu và truyền giữa các node trong một workflow. Biến giúp bạn truy xuất dữ liệu đầu ra của node trước hoặc định nghĩa giá trị tùy chỉnh trong quá trình xử lý.

## 2. Các loại biến trong n8n

| Loại biến | Giải thích |
|-----------|------------|
| `{{$json}}` | Truy cập dữ liệu JSON đầu ra của node trước đó |
| `{{$node["Tên node"].json}}` | Truy xuất dữ liệu từ node bất kỳ |
| `{{$parameter}}` | Truy cập giá trị từ các trường đã cấu hình trong node |
| `{{$env}}` | Lấy biến môi trường (environment variables) |
| `{{$workflow}}` | Truy cập thông tin workflow hiện tại (ID, tên, v.v.) |
| `{{$now}}` | Lấy thời gian hiện tại |
| `{{$item}}` | Dữ liệu đang xử lý tại vòng lặp hiện tại |
| `{{$binary}}` | Truy cập dữ liệu nhị phân (file, image,...) |

## 3. Biến toàn cục và biến cục bộ

| Loại biến | Phạm vi | Ví dụ |
|-----------|--------|-------|
| Biến cục bộ | Trong 1 node | `{{$json["name"]}}` |
| Biến toàn cục | Truy cập từ mọi node | `{{$node["Webhook"].json["email"]}}` |

## 4. Đặt giá trị biến tùy chỉnh

Dùng node `Set` để tạo hoặc chỉnh sửa biến:

```json
{
  "name": "John",
  "age": 25
}
```