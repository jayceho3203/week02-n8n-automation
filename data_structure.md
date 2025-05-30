# Cấu trúc Dữ liệu trong n8n

## 1. Định dạng dữ liệu chuẩn

Dữ liệu giữa các node truyền với nhau ở dạng mảng các object JSON:

```json
[
  {
    "json": {
      "id": 1,
      "name": "Alice"
    }
  },
  {
    "json": {
      "id": 2,
      "name": "Bob"
    }
  }
]
```

## 2. Các phần chính trong dữ liệu node

| Trường | Ý nghĩa |
|--------|---------|
| `json` | Dữ liệu chính của mỗi item |
| `binary` | Dữ liệu nhị phân (nếu có) |
| `pairedItem` | Trỏ về item gốc nếu xử lý song song |
| `context` | Dữ liệu ngữ cảnh nội bộ (ít dùng) |

## 3. Các node ảnh hưởng đến dữ liệu

| Node | Mô tả |
|------|------|
| `Set` | Tạo hoặc chỉnh sửa dữ liệu JSON |
| `Function` | Viết script JavaScript tùy biến dữ liệu |
| `IF`, `Switch` | Phân nhánh logic theo điều kiện |
| `Merge` | Gộp dữ liệu từ nhiều nguồn |
| `SplitInBatches` | Chia nhỏ dữ liệu để xử lý tuần tự |

## 4. Duyệt và xử lý từng item

- n8n xử lý mỗi item trong mảng một cách độc lập.
- Có thể dùng `{{$json}}`, `{{$item}}` trong mỗi lần lặp.

## 5. Dữ liệu giữa các node

Ví dụ node `A` trả về 3 item → node `B` nhận 3 item.

Trong node `Function`, bạn có thể xử lý như sau:

```js
return items.map(item => {
  item.json.total = item.json.price * item.json.quantity;
  return item;
});
```