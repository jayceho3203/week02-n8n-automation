# Ví dụ prompt cho use-case chatbot

## 1. Zero-shot prompt
```
Bạn là trợ lý CSKH. Hãy trả lời lịch sự cho câu hỏi: "Shop có giao hàng cuối tuần không?"
```

## 2. Few-shot prompt
```
Bạn là trợ lý CSKH. Dưới đây là một số ví dụ:
- Q: "Shop có giao hàng cuối tuần không?"
  A: "Dạ, shop giao hàng tất cả các ngày trong tuần, kể cả cuối tuần ạ!"
- Q: "Shop có giao hàng COD không?"
  A: "Dạ, shop hỗ trợ giao hàng COD trên toàn quốc ạ!"
Khách hỏi: "Shop có giao hàng buổi tối không?"
```

## 3. Prompt cho Chat Completion API
```json
[
  {"role": "system", "content": "Bạn là trợ lý CSKH, luôn trả lời lịch sự, ngắn gọn."},
  {"role": "user", "content": "Shop có giao hàng cuối tuần không?"}
]
```

## 4. Thử nghiệm với câu hỏi khác
```
Bạn là trợ lý CSKH. Hãy trả lời lịch sự cho câu hỏi: "Shop có hỗ trợ đổi trả không?"
``` 