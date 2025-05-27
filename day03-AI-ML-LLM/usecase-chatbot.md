# Use-case: Chatbot hỗ trợ khách hàng

## Mô tả
Chatbot trả lời tự động các câu hỏi của khách hàng về sản phẩm/dịch vụ trên website.

## Pipeline chi tiết
1. Thu thập dữ liệu: FAQ, lịch sử chat, tài liệu sản phẩm
2. Tiền xử lý dữ liệu: Làm sạch văn bản, chuẩn hóa ngôn ngữ
3. Huấn luyện mô hình: Sử dụng LLM (GPT-3, GPT-4) hoặc fine-tune trên dữ liệu doanh nghiệp
4. Triển khai chatbot: Tích hợp LLM vào website/app
5. Dự đoán/trả lời: LLM sinh câu trả lời tự động
6. Đánh giá & cải tiến: Thu thập phản hồi, cập nhật dữ liệu

## Vai trò AI/ML/LLM
- **AI:** Tổng thể hệ thống tự động hóa trả lời
- **ML:** Phân loại ý định, nhận diện cảm xúc
- **LLM:** Sinh câu trả lời tự nhiên, hiểu ngữ cảnh đa dạng

## Ví dụ minh họa
- Khách hỏi: "Shop có giao hàng cuối tuần không?"
- Chatbot (LLM) trả lời: "Dạ, shop giao hàng tất cả các ngày trong tuần, kể cả cuối tuần ạ!" 