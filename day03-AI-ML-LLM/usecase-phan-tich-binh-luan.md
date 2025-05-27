# Use-case: Phân tích nội dung bình luận mạng xã hội

## Mô tả
Tự động phân tích hàng ngàn bình luận để xác định cảm xúc khách hàng về sản phẩm.

## Pipeline chi tiết
1. Thu thập dữ liệu: Crawl bình luận từ Facebook, TikTok, Shopee...
2. Tiền xử lý dữ liệu: Loại bỏ spam, chuẩn hóa emoji, chuyển về chữ thường
3. Phân tích cảm xúc: Dùng ML (Logistic Regression, SVM) hoặc LLM (BERT, GPT) để phân loại cảm xúc
4. Tổng hợp & trực quan hóa: Thống kê tỷ lệ cảm xúc, vẽ biểu đồ
5. Đề xuất hành động: Nếu nhiều bình luận tiêu cực, cảnh báo cho CSKH

## Vai trò AI/ML/LLM
- **AI:** Tự động hóa toàn bộ quá trình phân tích
- **ML:** Phân loại cảm xúc dựa trên dữ liệu đã gán nhãn
- **LLM:** Hiểu ngữ cảnh sâu hơn, phân tích bình luận phức tạp

## Ví dụ minh họa
- Bình luận: "Sản phẩm giao nhanh, chất lượng tốt, sẽ ủng hộ tiếp!"
- Hệ thống phân loại: **Tích cực** 