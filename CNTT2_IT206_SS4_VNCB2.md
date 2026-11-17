# Sửa prompt thiếu ràng buộc định dạng

## Prompt lỗi

```
Hãy giải thích ngắn gọn các nội dung của Chain-of-Thought, Prompt Chaining, xử lý đứt gãy.
```

## Bước 1: Phân tích lỗi

3 phần thừa trong câu trả lời cũ của AI:

1. Lời chào mở đầu, ví dụ: "Chào bạn, rất vui được giúp bạn tìm hiểu về Kỹ thuật Prompting nhé!"
2. Câu dẫn dắt lòng vòng trước khi vào nội dung, ví dụ: "Trước khi đi vào từng phần, mình xin giới thiệu sơ qua về bối cảnh của prompting..."
3. Lời kết xã giao ở cuối, ví dụ: "Hy vọng giải thích trên hữu ích với bạn, nếu cần thêm thông tin cứ hỏi mình nhé!"

Nguyên nhân: prompt cũ chỉ nói "ngắn gọn" chung chung, không ràng buộc định dạng, không cấm lời chào và lời kết, nên AI trả lời theo kiểu hội thoại.

## Bước 2: Prompt tối ưu (đã sửa)

```
Giải thích các nội dung sau: Chain-of-Thought, Prompt Chaining, xử lý đứt gãy.

Yêu cầu bắt buộc:
- Trình bày bằng gạch đầu dòng, mỗi nội dung 1 mục.
- Mỗi mục tối đa 2 gạch đầu dòng con, mỗi gạch tối đa 20 từ.
- Cấm viết lời chào, câu dẫn dắt ở đầu.
- Cấm viết lời kết, lời mời hỏi thêm ở cuối.
- Bắt đầu thẳng bằng nội dung đầu tiên.
```

## Kết quả phản hồi của AI

- **Chain-of-Thought**
  - Yêu cầu AI suy luận từng bước trước khi đưa ra đáp án cuối.
  - Giúp tăng độ chính xác với bài toán logic, tính toán nhiều bước.
- **Prompt Chaining**
  - Chia việc lớn thành nhiều prompt nhỏ, kết quả prompt trước làm đầu vào cho prompt sau.
  - Dễ kiểm soát, dễ kiểm tra và sửa từng bước.
- **Xử lý đứt gãy**
  - Là cách xử lý khi một bước trong chuỗi bị lỗi, đầu ra sai hoặc thiếu.
  - Kiểm tra đầu ra từng bước, thử lại hoặc dùng phương án dự phòng.
