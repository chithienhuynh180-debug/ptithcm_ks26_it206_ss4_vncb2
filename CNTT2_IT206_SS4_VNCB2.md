# Khắc phục lỗi khai báo biến số trong prompt mẫu

## Prompt lỗi

```
Hãy viết một bài chia sẻ về Kỹ thuật Prompting Nâng cao (Logic & Chuỗi) bằng ngôn ngữ [language]. Dành cho đối tượng {audience}.
```

## Bước 1: Phân tích lỗi

- Dùng lẫn 2 loại ngoặc `[language]` và `{audience}` nên không có quy tắc chung. Công cụ tự động thay thế thường chỉ tìm 1 kiểu ký hiệu, nên sẽ bỏ sót biến còn lại.
- AI không biết đó là chỗ trống cần điền hay chỉ là chữ bình thường, nên có thể giữ nguyên hoặc tự đoán.
- Tên biến viết thường, không nổi bật, dễ lẫn vào câu văn.
- Khi có nhiều biến thì khó kiểm tra, khó sửa, dễ sót.

## Bước 2: Prompt đã đồng bộ biến số

```
Hãy viết một bài chia sẻ về Kỹ thuật Prompting Nâng cao (Logic & Chuỗi) bằng ngôn ngữ [NGÔN_NGỮ]. Dành cho đối tượng [ĐỐI_TƯỢNG].
```

## Kết quả chạy thử

Điền dữ liệu thực tế:

- [NGÔN_NGỮ] = tiếng Việt
- [ĐỐI_TƯỢNG] = sinh viên năm nhất

Prompt sau khi điền:

```
Hãy viết một bài chia sẻ về Kỹ thuật Prompting Nâng cao (Logic & Chuỗi) bằng ngôn ngữ tiếng Việt. Dành cho đối tượng sinh viên năm nhất.
```

Phản hồi của AI:

> **Kỹ thuật Prompting nâng cao cho sinh viên năm nhất**
>
> Prompting là cách mình viết yêu cầu để AI trả lời đúng ý. Có 2 kỹ thuật dễ dùng:
>
> - **Chain-of-Thought (suy luận từng bước):** bảo AI giải thích từng bước trước khi đưa đáp án. Cách này hợp với bài toán, bài logic, giúp kết quả chính xác hơn.
> - **Prompt Chaining (chuỗi prompt):** chia việc lớn thành nhiều prompt nhỏ, kết quả prompt trước làm đầu vào cho prompt sau. Ví dụ: prompt 1 lập dàn ý, prompt 2 viết bài, prompt 3 sửa lỗi.
>
> Nếu một bước bị lỗi thì kiểm tra lại đầu ra của bước đó rồi thử lại, không cần làm lại từ đầu.
>
> Mẹo: viết prompt rõ ràng, có định dạng cụ thể thì AI trả lời gọn và đúng hơn.