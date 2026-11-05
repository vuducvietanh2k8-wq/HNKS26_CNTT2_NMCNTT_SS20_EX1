1. Xác định ký tự lạ trong URL
URL đáng ngờ:

https://githúb.com/login
- Ký tự lạ là ú trong tên miền githúb.com.
- Đây là ký tự Unicode có dấu sắc, khác với chữ u thông thường trong tên miền chính thức github.com.
- Kẻ tấn công lợi dụng sự tương đồng về hình thức giữa các ký tự để tạo tên miền giả mạo. Người dùng nhìn lướt qua có thể tưởng rằng đây là trang GitHub thật và nhập thông tin đăng nhập.
- Đây là hình thức tấn công Homograph Attack, thường được sử dụng trong các chiến dịch Phishing.
Cảnh báo
 Không nhập mật khẩu hoặc Master Password vào URL đáng ngờ này.
2. Quy trình kiểm tra URL trước khi đăng nhập
Bước 1: Kiểm tra tên miền bằng mắt thường
- Đọc kỹ toàn bộ tên miền, đặc biệt là phần đứng trước .com.
- So sánh với địa chỉ chính thức: github.com.
- Chú ý các ký tự có dấu, ký tự Unicode hoặc chữ cái trông gần giống nhau.
- Không tin tưởng chỉ vì trang web có giao diện và logo giống GitHub.
Bước 2: Kiểm tra giao thức HTTPS
- Kiểm tra URL có sử dụng https:// hay không.
- HTTPS giúp mã hóa kết nối nhưng không chứng minh website là chính chủ.
- Website giả mạo vẫn có thể sử dụng HTTPS.
Bước 3: Sử dụng công cụ hỗ trợ
- Punycode: Kiểm tra tên miền Unicode đã được chuyển sang dạng ASCII hay chưa. Các tên miền Unicode có thể hiển thị dưới dạng xn--....
- VirusTotal: Tra cứu URL để kiểm tra xem tên miền có bị các hệ thống bảo mật đánh giá là độc hại hay không.
- Google Safe Browsing: Kiểm tra cảnh báo về website lừa đảo hoặc chứa phần mềm độc hại.
- WHOIS: Kiểm tra thông tin đăng ký và thời gian tạo tên miền nếu cần xác minh thêm.
Bước 4: Truy cập GitHub an toàn
1. Không nhấn vào liên kết trong email hoặc thông báo đáng ngờ.
2. Mở trình duyệt và tự nhập địa chỉ https://github.com.
3. Đăng nhập từ trang chính thức.
4. Nếu cần kiểm tra cảnh báo bảo mật, xem thông báo trong tài khoản GitHub thay vì làm theo liên kết được gửi đến.