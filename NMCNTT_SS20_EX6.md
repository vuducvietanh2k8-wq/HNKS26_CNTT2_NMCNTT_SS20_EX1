XÂY DỰNG QUY TRÌNH BẢO MẬT REPOSITORY GITHUB PUBLIC
1. Thiết kế cấu trúc repository an toàn
Khi đưa mã nguồn dự án thương mại điện tử lên GitHub Public, nhóm cần đảm bảo không công khai API Key, mật khẩu cơ sở dữ liệu, Access Token hoặc thông tin cấu hình nội bộ.
2. Cấu trúc .env.example cho 3 môi trường
# DEVELOPMENT
DEV_PORT=
DEV_DATABASE_URL=
DEV_API_KEY=

# TEST
TEST_PORT=
TEST_DATABASE_URL=
TEST_API_KEY=

# PRODUCTION
PROD_PORT=
PROD_DATABASE_URL=
PROD_API_KEY=
3. Kích hoạt 2FA bắt buộc cho thành viên
1. Đăng nhập GitHub → Settings.
2. Chọn Password and authentication.
3. Vào Two-factor authentication.
4. Kích hoạt bằng Google Authenticator hoặc Security Key.
5. Lưu Recovery Codes ở nơi an toàn.
6. Chủ sở hữu GitHub Organization bật Require two-factor authentication để yêu cầu tất cả thành viên sử dụng 2FA.
4. Báo cáo rủi ro nếu thiếu .gitignore
Rủi ro	Hậu quả
Lộ API Key	Bị sử dụng trái phép, phát sinh chi phí
Lộ mật khẩu Database	Cơ sở dữ liệu bị truy cập trái phép
Lộ Access Token	Tài khoản, dịch vụ có thể bị chiếm quyền
Lộ tệp .env	Rò rỉ thông tin cấu hình
Lộ Private Key	Nguy cơ giả mạo danh tính hệ thống

Biện pháp khắc phục:
- Thu hồi và thay mới các API Key, mật khẩu, Token bị lộ.
- Xóa tệp nhạy cảm khỏi Git và xử lý lịch sử commit.
- Bổ sung .gitignore.
- Quét Secrets trước khi Public repository.
- Bắt buộc toàn bộ thành viên bật 2FA.