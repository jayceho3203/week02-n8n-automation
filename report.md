# Phân biệt AI – ML – DL – LLM và Use Case thực tế

## I. Phân biệt khái niệm

### 1. Artificial Intelligence (AI) – Trí tuệ nhân tạo
- **Định nghĩa:** Là ngành khoa học mô phỏng trí thông minh con người bằng máy móc, cho phép chúng thực hiện các tác vụ như suy luận, học hỏi, và ra quyết định.
- **Phạm vi:** Bao gồm nhiều nhánh như Machine Learning, Computer Vision, Robotics, Natural Language Processing.

### 2. Machine Learning (ML) – Học máy
- **Định nghĩa:** Một nhánh con của AI cho phép hệ thống học từ dữ liệu để cải thiện hiệu suất mà không cần lập trình rõ ràng.
- **Ví dụ:** Dự đoán doanh thu, nhận diện chữ viết tay, phân loại email spam.

### 3. Deep Learning (DL) – Học sâu
- **Định nghĩa:** Nhánh con của ML sử dụng mạng nơ-ron nhân tạo nhiều tầng (deep neural networks) để mô hình hóa các biểu diễn dữ liệu phức tạp.
- **Ứng dụng:** Nhận diện hình ảnh, xử lý giọng nói, dịch máy.

### 4. Large Language Models (LLM) – Mô hình ngôn ngữ lớn
- **Định nghĩa:** Các mô hình học sâu đặc biệt lớn được huấn luyện trên lượng văn bản khổng lồ để sinh văn bản tự nhiên, hiểu ngữ cảnh và hỗ trợ hội thoại.
- **Ví dụ:** ChatGPT, Claude, Gemini, LLaMA, Mistral.

---

## II. Mối quan hệ phân cấp

AI
└── ML
└── DL
└── LLM


- **AI** là cấp độ rộng nhất, bao phủ tất cả.
- **ML** là công cụ giúp AI học từ dữ liệu.
- **DL** là kỹ thuật mạnh mẽ trong ML, đặc biệt với dữ liệu phi cấu trúc.
- **LLM** là ứng dụng cụ thể của DL cho xử lý ngôn ngữ tự nhiên (NLP).

---

## III. Use case thực tế: Chatbot AI hỗ trợ khách hàng

| Thành phần | Vai trò |
|------------|--------|
| **AI** | Tổng thể hệ thống hoạt động thông minh, hỗ trợ hội thoại tự động |
| **ML** | Học từ lịch sử câu hỏi để hiểu và đoán nhu cầu người dùng |
| **DL** | Dùng mô hình Transformer để hiểu cấu trúc câu, ngữ nghĩa sâu |
| **LLM** | Tạo phản hồi tự nhiên, giống người thật, dựa trên prompt đầu vào |

Ví dụ: Người dùng hỏi “Tôi có thể giao hàng vào thứ bảy không?”, hệ thống dùng LLM để sinh ra câu trả lời phù hợp và ML để cải thiện phản hồi theo thời gian.

---

## IV. Kết luận

- AI là nền tảng rộng bao gồm nhiều kỹ thuật.
- ML giúp hệ thống học tự động từ dữ liệu.
- DL cung cấp khả năng học sâu hơn, hiệu quả hơn với dữ liệu phức tạp.
- LLM là ứng dụng tiên tiến giúp AI hiểu và tạo ngôn ngữ giống con người.

## Use Case: Hệ thống Chatbot hỗ trợ khách hàng tích hợp AI – ML – DL – LLM

### Mô tả bài toán

Một công ty thương mại điện tử muốn xây dựng một chatbot thông minh có khả năng:
- Trả lời tự động các câu hỏi thường gặp từ khách hàng
- Hiểu ngôn ngữ tự nhiên, cả chính tả sai hoặc ngữ pháp thiếu
- Học hỏi từ các cuộc hội thoại trước để cải thiện dần
- Sinh câu trả lời tự nhiên, giống người thật

---

### Vai trò của từng thành phần

| Thành phần | Vai trò trong hệ thống |
|------------|------------------------|
| **AI**     | Điều phối toàn bộ hệ thống và định hướng tự động hóa hành vi như con người. |
| **ML**     | Phân tích lịch sử hội thoại, phân loại ý định (intent), và điều chỉnh phản hồi dựa trên dữ liệu người dùng. |
| **DL**     | Áp dụng các mô hình học sâu như Transformer để hiểu ngữ cảnh và mối quan hệ giữa các từ/phần của câu. |
| **LLM**    | Sinh văn bản phản hồi tự nhiên, logic, sử dụng ngữ cảnh và kiến thức huấn luyện trước đó (như ChatGPT). |

---

### Dòng xử lý dữ liệu của chatbot

1. **Người dùng** gửi câu hỏi:  
   *“Shop có giao hàng vào cuối tuần không?”*

2. **NLP (LLM)** hiểu và tách câu thành ngữ nghĩa:  
   → nhận biết đây là một câu hỏi về thời gian giao hàng

3. **ML module** xác định intent là:  
   → `"hỏi chính sách giao hàng"` → map tới câu trả lời tương ứng hoặc prompt thích hợp

4. **LLM (GPT/Claude)** sinh ra câu trả lời hoàn chỉnh:
   → *“Dạ, shop hỗ trợ giao hàng vào tất cả các ngày trong tuần, kể cả cuối tuần ạ!”*

5. **DL (Transformer)** giúp hiểu ngữ cảnh mơ hồ, hoặc câu hỏi viết sai chính tả:
   → *“có giao hàng cuôi tuan ko?”* vẫn được hiểu đúng

6. **ML** ghi nhận và học từ phản hồi này (ví dụ: đánh giá tích cực của khách hàng) để cải thiện phản hồi sau

---

### Tích hợp thực tế bằng n8n

- Sử dụng Webhook để nhận câu hỏi từ frontend
- Gọi API OpenAI (hoặc LLM khác) qua HTTP Request node
- Lưu phản hồi vào Google Sheets hoặc database
- Trả kết quả về giao diện người dùng

---

### Kết quả đạt được

- Giảm 60–80% khối lượng công việc CSKH thủ công
- Tăng trải nghiệm người dùng nhờ phản hồi nhanh, mượt
- Học hỏi từ dữ liệu thực tế để ngày càng cải thiện phản hồi


