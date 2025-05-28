# Ngày 4: Prompt Engineering cơ bản

## 1. Cấu trúc prompt: role + context + instruction
- **Role:** Định nghĩa vai trò của AI (VD: "Bạn là trợ lý CSKH").
- **Context:** Bối cảnh, thông tin nền (VD: "Khách hỏi về chính sách giao hàng").
- **Instruction:** Chỉ dẫn cụ thể (VD: "Hãy trả lời ngắn gọn, lịch sự").

**Ví dụ:**
```
Bạn là trợ lý CSKH.
Khách hỏi: "Shop có giao hàng cuối tuần không?"
Hãy trả lời ngắn gọn, lịch sự.
```

## 2. Zero-shot, few-shot prompt
- **Zero-shot:** Chỉ đưa instruction, không có ví dụ mẫu.
- **Few-shot:** Có thêm 1 hoặc vài ví dụ mẫu để AI học theo cách trả lời.

## 3. Prompt cho Chat Completion API
- Prompt là mảng các message, mỗi message gồm:
  - `role`: "system", "user", "assistant"
  - `content`: nội dung

**Ví dụ:**
```
[
  {"role": "system", "content": "Bạn là trợ lý CSKH."},
  {"role": "user", "content": "Shop có giao hàng cuối tuần không?"}
]
```

## 4. Checklist thực hành
- [ ] Viết prompt zero-shot cho chatbot
- [ ] Viết prompt few-shot cho chatbot
- [ ] Viết prompt dạng message cho Chat Completion API
- [ ] Thử nghiệm prompt với các câu hỏi khác nhau

## 5. Tham khảo ví dụ
- [Ví dụ prompt cho use-case chatbot](./prompt-chatbot-examples.md) 