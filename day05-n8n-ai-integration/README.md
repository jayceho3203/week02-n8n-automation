# Ngày 5: Tích hợp AI vào n8n

## 1. Sử dụng HTTP request để gọi API OpenAI từ n8n
- Thêm node **HTTP Request** vào workflow.
- **Method**: `POST`
- **URL**: `https://api.openai.com/v1/chat/completions`
- **Headers**:
  - `Content-Type`: `application/json`
  - `Authorization`: `Bearer YOUR_OPENAI_API_KEY`
- **Body** (JSON):
  ```json
  {
    "model": "gpt-3.5-turbo",
    "messages": [
      {"role": "system", "content": "Bạn là trợ lý CSKH."},
      {"role": "user", "content": "{{$json["body"]["message"]}}"}
    ]
  }
  ```

## 2. Xử lý input → gửi prompt → nhận phản hồi → lưu log
- **Input**: Node **Webhook** nhận dữ liệu từ form hoặc API bên ngoài.
- **Prompt**: Node **HTTP Request** gửi prompt tới OpenAI API.
- **Phản hồi**: Output của node HTTP Request là JSON chứa phản hồi từ OpenAI.
- **Log**: Dùng node **Google Sheets** hoặc **Database** để lưu log.

## 3. Thực hành: Flow người dùng nhập → AI trả lời → lưu kết quả
- **Node Webhook** (POST): Nhận dữ liệu từ form hoặc API bên ngoài.
- **Node HTTP Request**: Gọi API OpenAI với prompt từ node Webhook.
- **Node Google Sheets**: Lưu log (input, prompt, phản hồi, timestamp).

## 4. Checklist thực hành
- [ ] Cấu hình node HTTP Request để gọi API OpenAI
- [ ] Xử lý input từ node Webhook
- [ ] Lưu log vào Google Sheets
- [ ] Test workflow với request thực tế

## 5. Tham khảo ví dụ
- [Ví dụ flow tích hợp AI vào n8n](./flow-example.md) 