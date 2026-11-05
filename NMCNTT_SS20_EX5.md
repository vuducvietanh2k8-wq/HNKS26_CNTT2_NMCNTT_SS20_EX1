dùng chữ để trình bày
THIẾT KẾ QUY TRÌNH ĐĂNG NHẬP CRYPTO WALLET BẰNG MFA VÀ TOTP
1. Thiết kế kiến trúc bảo mật
Ứng dụng Crypto Wallet sử dụng mô hình MFA (Multi-Factor Authentication) kết hợp với thuật toán TOTP (Time-based One-Time Password) để xác thực người dùng qua 3 lớp bảo vệ.
1.2. Giải thích 3 lớp bảo vệ
Lớp 1: Mật khẩu (Something You Know)
- Người dùng nhập mật khẩu để xác minh danh tính.
- Hệ thống kiểm tra mật khẩu đã được lưu dưới dạng mã băm an toàn.
- Nếu mật khẩu sai, hệ thống từ chối đăng nhập.
- Có giới hạn số lần nhập sai để hạn chế tấn công dò mật khẩu.
Lớp 2: Mã TOTP (Something You Have)
- Người dùng sử dụng ứng dụng Google Authenticator hoặc Microsoft Authenticator để tạo mã OTP gồm 6 chữ số.
- Mã OTP thường thay đổi sau mỗi 30 giây.
- Hệ thống xác minh mã OTP dựa trên khóa bí mật đã đăng ký và thời gian hiện tại.
- Mã OTP chỉ có hiệu lực trong một khoảng thời gian ngắn.
Lớp 3: Sinh trắc học (Something You Are)
- Người dùng xác thực bằng vân tay hoặc nhận diện khuôn mặt.
- Sinh trắc học giúp xác nhận người đang sử dụng thiết bị là chủ tài khoản.
- Ưu tiên xử lý sinh trắc học ngay trên thiết bị, không gửi dữ liệu sinh trắc học thô lên máy chủ.
2. Xử lý tình huống Edge Case: Người dùng ở trên máy bay
Tình huống: Người dùng đang ở trên máy bay, không có Internet hoặc sóng điện thoại nhưng cần lấy mã OTP để xác thực.

Giải pháp: Sử dụng ứng dụng tạo mã TOTP ngoại tuyến.
- TOTP được tạo dựa trên khóa bí mật đã lưu trong ứng dụng xác thực và thời gian trên thiết bị.
- Ứng dụng như Google Authenticator có thể tạo mã OTP mà không cần Internet hoặc sóng điện thoại.
- Mã OTP thường có hiệu lực trong khoảng 30 giây.
- Người dùng chỉ cần mở ứng dụng xác thực và nhập mã OTP vào hệ thống.
Quy trình thực hiện:
1. Trước chuyến bay, người dùng cài đặt ứng dụng Google Authenticator và liên kết với tài khoản Crypto Wallet.
2. Khi ở trên máy bay, người dùng mở ứng dụng xác thực.
3. Ứng dụng tự tạo mã OTP 6 chữ số dựa trên thời gian và khóa bí mật đã lưu.
4. Người dùng nhập mã OTP để xác thực.
5. Khi có kết nối Internet trở lại, hệ thống tiếp tục xử lý yêu cầu giao dịch nếu các dịch vụ cần thiết hoạt động bình thường.