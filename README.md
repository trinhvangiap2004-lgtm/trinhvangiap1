🛒 Tìm kiếm sản phẩm từ nhiều nền tảng (Python Project)
📌 Giới thiệu

Đây là bài tập thực hành Python với mục tiêu xây dựng một hệ thống tìm kiếm sản phẩm từ nhiều nguồn khác nhau như Shopee, Tiki hoặc TikTok Shop.
Dự án sử dụng mô hình tách module rõ ràng (app – scrapers – templates) giúp mở rộng và bảo trì dễ dàng.

🧩 Chức năng chính
✔️ 1. Tìm kiếm sản phẩm theo từ khóa

Người dùng nhập từ khóa → hệ thống sẽ gọi các scraper tương ứng để lấy dữ liệu từ từng nền tảng.

✔️ 2. Thu thập thông tin sản phẩm

Mỗi scraper có nhiệm vụ:

Gửi request đến API/HTML của sàn

Parse dữ liệu

Trả về các thông tin:

Tên sản phẩm

Giá

Link

Ảnh

Đánh giá 

✔️ 3. Giao diện web đơn giản

Hệ thống sử dụng thư mục templates/ để hiển thị kết quả tìm kiếm dưới dạng HTML thân thiện.

✔️ 4. Chạy bằng Flask (hoặc framework tương tự)

File run.py dùng để khởi động server.
Người dùng có thể truy cập qua trình duyệt và thực hiện tìm kiếm.

✔️ 5. Hỗ trợ chạy qua CLI

File cli.py cho phép chạy tìm kiếm bằng terminal — phù hợp kiểm thử nhanh.

✔️ 6. Tách scraper theo từng nền tảng

Thư mục scrapers/ gồm các module riêng biệt cho từng trang.
Điều này giúp dễ dàng thêm nguồn mới mà không ảnh hưởng mã cũ.

📂 Cấu trúc thư mục
TimkiemSanpham/
│
├── app/                # Xử lý logic ứng dụng
├── scrapers/           # Bộ thu thập dữ liệu từng nền tảng
├── templates/          # Giao diện HTML hiển thị kết quả
│
├── run.py              # Chạy ứng dụng web
├── cli.py              # Chạy tìm kiếm bằng command-line
├── test_tiktok.py      # File test thử scraper TikTok
├── requirements.txt    # Danh sách thư viện cần cài
└── README.md           # Mô tả dự án



📝 Ghi chú

Một số scraper cần xử lý User-Agent hoặc cookies để tránh chặn request.

Có thể mở rộng để thêm nhiều nguồn khác (Lazada, Sendo...).

test_tiktok.py dùng để kiểm thử việc lấy dữ liệu từ TikTok Shop.
