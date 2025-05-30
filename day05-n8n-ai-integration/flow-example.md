# Ví dụ flow tích hợp AI vào n8n

## 1. Node Webhook (POST)
- **URL**: `http://localhost:5678/webhook-test/ai-chat`
- **Input**: JSON từ form hoặc API bên ngoài
  ```json
  {
    "message": "Shop có giao hàng cuối tuần không?"
  }
  ```

## 2. Node HTTP Request
- **Method**: `POST`
- **URL**: `  https://openrouter.ai/api/v1/chat/completions`
- **Headers**:
  - `Content-Type`: `application/json`
  - `Authorization`: `Bearer YOUR_OPENAI_API_KEY`
- **Body**:
  ```json
  {
    "model": "gpt-3.5-turbo",
    "messages": [
      {"role": "system", "content": "Bạn là trợ lý CSKH."},
      {"role": "user", "content": "{{$json["body"]["message"]}}"}
    ]
  }
  ```

## 3. Node Google Sheets
- **Operation**: `Append`
- **Sheet**: `Logs`
- **Values**:
  - Input: `{{$json["body"]["message"]}}`
  - Prompt: `{{$json["body"]["message"]}}`
  - Phản hồi: `{{$json["choices"][0]["message"]["content"]}}`
  - Timestamp: `{{new Date().toLocaleString()}}`

## 4. Test workflow
- Gửi request tới URL webhook với body:
  ```json
  {
    "message": "Shop có giao hàng cuối tuần không?"
  }
  ```
- Kiểm tra Google Sheets đã ghi log chưa. 