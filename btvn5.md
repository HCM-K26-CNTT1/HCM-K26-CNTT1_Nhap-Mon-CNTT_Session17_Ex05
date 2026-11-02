# Bài 5: Xây Dựng Bộ Tiện Ích Trình Duyệt Cho Doanh Nghiệp

## Phần 1. Thiết kế kiến trúc Extensions

### 1. Danh sách 5 tiện ích trọng tâm

Đề xuất sử dụng tối đa 5 tiện ích mở rộng trên Google Chrome, phục vụ ba nhóm: Dev Suite, Productivity và Security.

| Nhóm | Extension | Vai trò và ứng dụng trong dự án LMS |
|---|---|---|
| Dev Suite | JSON Viewer | Hiển thị dữ liệu JSON có cấu trúc rõ ràng, dễ đọc khi kiểm tra API của hệ thống LMS. |
| Dev Suite | Wappalyzer | Nhận diện các công nghệ website sử dụng như ngôn ngữ lập trình, framework và hệ quản trị nội dung. |
| Productivity | Bitwarden | Quản lý mật khẩu tập trung, tạo mật khẩu mạnh và hỗ trợ tự động điền thông tin đăng nhập. |
| Security | uBlock Origin Lite | Chặn quảng cáo và một số nội dung theo dõi hoặc tài nguyên độc hại theo bộ lọc được hỗ trợ. |
| Security | VirusTotal | Hỗ trợ kiểm tra độ an toàn của URL hoặc tệp tin đáng ngờ trước khi truy cập hoặc tải xuống. |

### 2. Phân tích vai trò từng nhóm

**a. Nhóm Dev Suite**

- **JSON Viewer:** Giúp lập trình viên đọc dữ liệu JSON dễ dàng hơn, đặc biệt khi kiểm tra API trả về thông tin sinh viên, khóa học và điểm số trên LMS.
- **Wappalyzer:** Giúp nhận biết công nghệ được sử dụng trên website, hỗ trợ tìm hiểu cấu trúc và môi trường phát triển của dự án.

**b. Nhóm Productivity**

- **Bitwarden:** Lưu trữ và quản lý mật khẩu trong một kho bảo mật, hạn chế việc sử dụng một mật khẩu cho nhiều tài khoản.
- Hỗ trợ tạo mật khẩu mạnh và tự động điền thông tin đăng nhập.
- Giúp quản lý riêng tài khoản cá nhân và tài khoản phục vụ học tập.

**c. Nhóm Security**

- **uBlock Origin Lite:** Hạn chế quảng cáo, trình theo dõi và một số nội dung có nguy cơ gây mất an toàn khi duyệt web.
- **VirusTotal:** Hỗ trợ kiểm tra URL và tệp tin đáng ngờ thông qua nhiều công cụ bảo mật, giúp phát hiện nguy cơ trước khi sử dụng.

## Phần 2. Sản phẩm hoàn chỉnh

### 3. Quy trình 4 bước tối ưu RAM và bảo mật

**Bước 1. Kiểm tra và loại bỏ Extensions không cần thiết**

- Mở Google Chrome.
- Nhập `chrome://extensions` vào thanh địa chỉ.
- Kiểm tra danh sách tiện ích đang được cài đặt.
- Gỡ bỏ những tiện ích không sử dụng hoặc không rõ nguồn gốc.
- Chỉ giữ lại tối đa 5 Extensions đã lựa chọn.

**Kết quả:** Giảm số lượng tiện ích chạy nền, hạn chế tiêu tốn RAM và giảm nguy cơ cài phải tiện ích độc hại.

**Bước 2. Cài đặt 5 Extensions cần thiết**

- Truy cập Chrome Web Store.
- Tìm kiếm từng tiện ích theo tên.
- Kiểm tra nhà phát triển, đánh giá và quyền truy cập trước khi cài đặt.
- Chọn Add to Chrome để cài đặt.
- Chỉ cài phiên bản chính thức từ nhà phát triển đáng tin cậy.

**Kết quả:** Trình duyệt có đủ công cụ phục vụ lập trình, quản lý mật khẩu và bảo mật.

**Bước 3. Thiết lập quyền Site Access (On click)**

Site Access là tính năng cho phép người dùng kiểm soát website mà Extensions được quyền truy cập.

Cách thiết lập:

1. Mở `chrome://extensions`.
2. Chọn tiện ích cần quản lý.
3. Chọn Details.
4. Tìm mục Site access.
5. Chọn On click nếu tiện ích hỗ trợ tùy chọn này.

**Ý nghĩa của On click:**

- Tiện ích chỉ được cấp quyền truy cập website khi người dùng chủ động nhấn vào biểu tượng của tiện ích.
- Hạn chế việc tiện ích tự động đọc nội dung website khi không cần thiết.
- Giảm nguy cơ tiện ích tiếp cận dữ liệu nhạy cảm trên các trang đăng nhập hoặc tài liệu học tập.

Ví dụ: Không cần cho Wappalyzer hoặc VirusTotal truy cập mọi website liên tục. Người dùng có thể chủ động kích hoạt khi cần kiểm tra.

**Lưu ý:** On click không bảo đảm tiện ích hoàn toàn an toàn. Cần kiểm tra quyền truy cập và chỉ cài đặt tiện ích đáng tin cậy. Một số tiện ích có thể cần quyền truy cập rộng hơn để hoạt động đúng chức năng.

**Bước 4. Kiểm tra và quản lý hiệu suất trình duyệt**

- Mở Chrome Task Manager bằng tổ hợp phím `Shift + Esc`.
- Kiểm tra mức sử dụng RAM của từng tab và tiện ích.
- Tắt hoặc gỡ bỏ những tiện ích không cần thiết.
- Không mở quá nhiều tab cùng lúc.
- Cập nhật Chrome và Extensions thường xuyên.
- Kiểm tra lại quyền truy cập sau mỗi lần cài đặt tiện ích mới.

**Kết quả:** Trình duyệt hoạt động ổn định hơn, giảm tình trạng quá tải RAM và hạn chế nguy cơ rò rỉ dữ liệu.

## Tổng kết cuối bài

Bộ 5 Extensions gồm JSON Viewer, Wappalyzer, Bitwarden, uBlock Origin Lite và VirusTotal giúp xây dựng môi trường trình duyệt phục vụ học tập và phát triển dự án LMS.

Việc phân chia thành ba nhóm Dev Suite, Productivity và Security giúp quản lý tiện ích khoa học. Bên cạnh đó, loại bỏ Extensions không cần thiết, kiểm soát quyền Site Access bằng On click và thường xuyên kiểm tra RAM giúp trình duyệt hoạt động hiệu quả và an toàn hơn.