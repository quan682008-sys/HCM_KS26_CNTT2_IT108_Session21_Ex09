# HCM_KS26_CNTT2_IT108_Session21_Ex09
# Bài 9: Xây Dựng Prompt 3 Thành Phần Giải Mã Thông Báo Lỗi Trạm Sạc Cùng Trợ Lý AI

## Phần 1

1. Câu hỏi quá cụt, không có thiết bị, hệ điều hành hay lỗi cụ thể nên AI phải đoán mò, thấy hỏng thì đoán lỗi phần cứng. Đó là ảo giác AI.

2. Prompt 3 thành phần:

[Context] Tôi trực trạm sạc VoltCharge số 04, máy chạy Windows 11, trụ đang sạc xe taxi điện thì dừng và hiện lỗi dưới đây.

[Raw Error] `System.UnauthorizedAccessException: Access to the path 'C:\Program Files\VoltCharge\data\session.log' is denied. Process terminated with exit code 5.`

[Instruction] Giải thích lỗi bằng tiếng Việt dễ hiểu và đưa ra 3 bước khắc phục.

## Phần 2

3. Phần mềm muốn ghi file `session.log` vào thư mục Program Files nhưng không có quyền admin nên Windows chặn, phần mềm không chạy được. Đây là lỗi phân quyền, không phải hỏng phần cứng.

4. Ba bước khắc phục:

- Bước 1: Chuột phải phần mềm VoltCharge, chọn Run as administrator.
- Bước 2: Chuột phải thư mục `data`, Properties, Security, Edit, cho tài khoản chạy phần mềm quyền Write và Modify, bấm Apply.
- Bước 3: Mở lại phần mềm và kiểm tra trụ 04 sạc lại được chưa.

5. Phải xóa hoặc thay bằng `[HIDDEN]` trước khi dán. Vì API key là bí mật, gửi lên AI có thể bị lộ rồi bị người khác dùng hệ thống.
   
