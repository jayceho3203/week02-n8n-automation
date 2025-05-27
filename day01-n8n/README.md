# 📅 Week 02 – Day 01: Làm quen với n8n và tạo workflow đầu tiên

## 📌 Mục tiêu
- Làm quen với giao diện và cách hoạt động của n8n
- Hiểu khái niệm **workflow** và **trigger**
- Tạo workflow đầu tiên với **Webhook trigger** và **HTTP Request**

---

## ✅ Nội dung đã thực hiện

### 1. Cài đặt và truy cập n8n
- Khởi chạy n8n bằng Docker trên `localhost:5678`
- Truy cập giao diện qua trình duyệt

### 2. Tạo workflow đầu tiên
- Tạo workflow mới có 2 node:
  - **Receive Webhook (Trigger)**: dạng GET, dùng để khởi động flow khi có HTTP request đến
  - **HTTP Request**: gửi yêu cầu đến API mẫu `https://jsonplaceholder.typicode.com/todos/1`

### 3. Kiểm thử workflow
- Nhấn nút **Test workflow**
- Copy URL webhook
- Gửi thử request bằng trình duyệt → kiểm tra kết quả trả về từ API

---

## 💡 Kết quả
- Workflow hoạt động tốt: nhận request và gửi được dữ liệu từ API
- Hiểu được luồng xử lý cơ bản của n8n: Trigger → Node xử lý → Trả kết quả

---


## 📚 Kiến thức học được

| Nội dung | Mô tả |
|---------|-------|
| **Trigger** | Node khởi động workflow khi có sự kiện xảy ra |
| **Webhook** | Một loại trigger phổ biến, lắng nghe request từ bên ngoài |
| **HTTP Request node** | Dùng để gửi yêu cầu đến các API khác |
| **Test workflow** | Chạy thử flow trong môi trường kiểm thử |

---

## 🔍 Ghi chú
- Cần bật “Active” để chạy production webhook
- Có thể tích hợp thêm Google Sheet hoặc gửi dữ liệu đi sau bước này

---

## 📅 Kế hoạch tiếp theo (Day 2)
- Làm quen biến (`variables`) và cấu trúc dữ liệu trong n8n
- Ghi dữ liệu vào Google Sheet
- Kết hợp form → ghi → gửi thông báo

