# n8n Google Sheets & Email Workflow Practice

## Checklist

- [ ] Tạo file `form.html` và thay `YOUR_N8N_WEBHOOK_URL` bằng URL webhook thực tế của bạn
- [ ] Tạo workflow trong n8n:
  - [ ] Thêm node Webhook (POST)
  - [ ] Thêm node Google Sheets (Append row)
  - [ ] Thêm node Email (gửi xác nhận về email đã nhập)
  - [ ] Kết nối các node theo thứ tự: Webhook → Google Sheets → Email
- [ ] Test gửi form, kiểm tra Google Sheets và email nhận được

## Hướng dẫn nhanh
1. Mở `form.html` trên trình duyệt, nhập thông tin và gửi.
2. Kiểm tra Google Sheets đã ghi dữ liệu chưa.
3. Kiểm tra email đã nhận được chưa.

> **Lưu ý:**
> - Đảm bảo đã cấu hình credential cho Google Sheets và Email node trong n8n.
> - Nếu dùng Gmail, có thể cần bật App Password hoặc OAuth2. 