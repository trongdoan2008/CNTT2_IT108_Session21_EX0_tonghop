# Phần 1 – Googling đúng cách

### 1. Vì sao Bad Query kém hiệu quả?

Câu hỏi quá dài và lang mang, không có từ khóa kỹ thuật và không báo lỗi cụ thể nên Google khó tìm đúng

### 2. Bóc tách lỗi

| Thành phần| Nộidung |
| :-- | :-- |
| Tên phần mềm / Hệ điều hành | Node.js / Windows 11 |
| Mã lỗi nguyên văn | `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Thao tác đang làm           | Gõ `npm -v` trong Terminal VS Code để kiểm tra phiên bản npm.                                 |

### 3. Ba câu truy vấn Google

1. `site:stackoverflow.com npm not recognized Windows 11`
2. `"npm is not recognized as an internal or external command"`
3. `npm not recognized Windows PATH -windows-xp`

# Phần 2 – Thẩm định StackOverflow

### 1. So sánh hai câu trả lời

| Tiêu chí | Câu trả lời A | Câu trả lời B |
| :-- | -- | -- |
| Vote & Tích xanh | +186, có tích xanh | +2, không tích xanh |
| Thời gian đăng   | 2 năm trước | 9 năm trước |
| Tags | node.js, windows, npm | node.js, windows-xp |

### 2. Kết luận

Chọn  A vì có nhiều lượt bình chọn, có tích xanh và đúng hệ điều hành.

 B có thể là bẫy nguy hiểm vì hướng dẫn cài driver mạng cho Windows XP, không liên quan đến lỗi npm trên Windows 11.

### 3. Quy trình 30 giây đọc lướt

1. Xem tiêu đề câu hỏi.
2. Kiểm tra Tags.
3. Xem Accepted Answer.
4. Kiểm tra Upvotes.
5. Xem ngày đăng.
6. Đọc nội dung giải pháp.

# Phần 3 – Hỏi AI đúng cách và nhận diện rủi ro

### 1. Prompt 3 thành phần

**Context**

Tôi vừa cài Node.js trên laptop Windows 11 và sử dụng Terminal trong VS Code. Tôi đã thử thêm đường dẫn Node.js vào biến môi trường PATH và mở Terminal mới nhưng lỗi vẫn xuất hiện.

**Raw Error**

```
'npm' is not recognized as an internal or external command, operable program or batch file.
```

**Instruction**

Hãy giải thích nguyên nhân bằng tiếng Việt dễ hiểu và đưa ra 3 bước kiểm tra, khắc phục an toàn
### 2. Đánh giá câu trả lời AI

Không an toàn

- Nguyên tắc 1: Lệnh `del /f /s /q C:\Windows\System32\*` có thể xóa các tệp quan trọng của Windows.
- Nguyên tắc 2: AI đoán rằng xóa cache sẽ sửa được lỗi PATH, nhưng không có căn cứ.
- Nguyên tắc 3: Không cung cấp mật khẩu, API Key hoặc thông tin bí mật cho AI.

### 3. Phản hồi lại AI

"Giải thích giúp tôi lệnh trên thực hiện những gì, có nguy cơ xóa tệp hệ thống không? Hãy đưa ra cách kiểm tra và sửa biến PATH an toàn mà không xóa dữ liệu Windows."
# Phần 4 – Viết Bug Report chuẩn

### 1. Tin nhắn kém

"Thầy ơi máy em bị lỗi npm, thầy sửa giúp em với ạ!"

### 2. Tin nhắn chuẩn

Em chào thầy, em đang gặp lỗi khi kiểm tra npm trên Windows 11.

**1. Context:** Em đã cài Node.js và sử dụng Terminal trong VS Code.

**2. Expected:** Gõ `npm -v` và hiển thị phiên bản npm.

**3. Actual:** Terminal báo lỗi:

```
'npm' is not recognized as an internal or external command, operable program or batch file.
```

**4. Log & Screenshot:** Em đã làm theo hướng dẫn thêm đường dẫn Node.js vào PATH và mở Terminal mới nhưng lỗi vẫn còn.

### 3. Phím tắt chụp màn hình và lưu ý

-  `Windows + Shift + S`.
- Che thông tin cá nhân, mật khẩu và API Key trước khi gửi ảnh cho người khác.