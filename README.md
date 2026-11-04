# My-CV — Portfolio cá nhân

## 1. Tên dự án

**My-CV** — website portfolio/CV cá nhân của Phan Hoàng Minh.

## 2. Mô tả

My-CV là website tĩnh giới thiệu cá nhân, kỹ năng và một số trò chơi yêu thích. Trang có thiết kế responsive, thanh điều hướng đến từng phần nội dung và sử dụng hình ảnh được lưu trong dự án.

Website chỉ sử dụng HTML và CSS để hiển thị nội dung. Dự án không có backend, cơ sở dữ liệu, API hoặc bước build; không cần cài npm hay JavaScript để chạy.

## 3. Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Trình bày các kỹ năng.
- Hiển thị các trò chơi yêu thích: Free Fire, PUBG, Liên Quân và Minecraft.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị email, GitHub và liên kết quay lại đầu trang.
- Tự điều chỉnh bố cục cho màn hình điện thoại, máy tính bảng và máy tính.

> Các liên kết “Xem chi tiết” trong thẻ trò chơi hiện là liên kết mẫu. Hãy cập nhật URL nếu muốn sử dụng chúng.

## 4. Công nghệ

- **HTML5:** cấu trúc và nội dung trang.
- **CSS3:** giao diện, bố cục responsive, Flexbox và CSS Grid.
- **Nginx trên Docker (tùy chọn):** phục vụ website tĩnh trong container.

## 5. Yêu cầu môi trường

Để mở website:

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.

Để tải mã nguồn và chạy máy chủ cục bộ (tùy chọn):

- Git, nếu tải dự án bằng lệnh `git clone`.
- Python 3, nếu muốn chạy máy chủ HTTP cục bộ.

Để chạy bằng Docker (tùy chọn):

- Docker Desktop trên Windows hoặc macOS, hay Docker Engine trên Linux.
- Docker cần được cài đặt và khởi động trước khi chạy lệnh.

Không cần cài Node.js, trình quản lý gói, cơ sở dữ liệu hoặc backend.

## 6. Cài đặt

### Tải mã nguồn bằng Git

Mở PowerShell trên Windows hoặc Terminal trên macOS/Linux, rồi chạy:

```bash
git clone https://github.com/hoangminhphan1408-ctrl/My-CV.git
cd My-CV
```

Nếu không dùng Git, tải mã nguồn dưới dạng ZIP và giải nén. Khi di chuyển hoặc triển khai dự án, giữ nguyên cấu trúc thư mục `assets/css/` và `assets/img/` để trang tải được CSS và hình ảnh.

## 7. Cấu hình và tùy chỉnh

Không cần tạo file cấu hình riêng. Có thể chỉnh sửa trực tiếp:

- `index.html`: tiêu đề, phần giới thiệu, kỹ năng, danh sách trò chơi và thông tin liên hệ.
- `assets/css/styles.css`: màu sắc, kiểu chữ, khoảng cách và bố cục responsive.
- `assets/img/`: ảnh đại diện và ảnh minh họa.

Nếu thay hình ảnh, hãy cập nhật đường dẫn ảnh tương ứng trong `index.html`. Trước khi xuất bản, kiểm tra và thay email, liên kết GitHub, nội dung giới thiệu và các liên kết mẫu bằng thông tin mong muốn công khai.

## 8. Chạy thử

### Mở trực tiếp

Có thể mở `index.html` bằng trình duyệt. Nếu muốn truy cập qua HTTP như một website thông thường, hãy chạy máy chủ cục bộ theo hướng dẫn của hệ điều hành bên dưới.

### Windows

1. Cài Python 3 nếu máy chưa có. Có thể tải từ [python.org](https://www.python.org/downloads/windows/) và chọn tùy chọn thêm Python vào `PATH` khi cài đặt.
2. Mở PowerShell tại thư mục dự án. Ví dụ:

   ```powershell
   cd "D:\duong-dan\toi\My-CV"
   ```

3. Khởi động máy chủ:

   ```powershell
   py -m http.server 8000
   ```

   Nếu lệnh `py` không có sẵn, thử:

   ```powershell
   python -m http.server 8000
   ```

### macOS

1. Mở Terminal tại thư mục dự án. Nếu chưa cài Python 3, cài từ [python.org](https://www.python.org/downloads/macos/) hoặc dùng trình quản lý gói phù hợp.
2. Chạy:

   ```bash
   cd /duong-dan/toi/My-CV
   python3 -m http.server 8000
   ```

### Linux

1. Mở Terminal tại thư mục dự án. Nếu chưa cài Python 3, cài Python 3 bằng trình quản lý gói của bản phân phối.
2. Chạy:

   ```bash
   cd /duong-dan/toi/My-CV
   python3 -m http.server 8000
   ```

### Truy cập website

Sau khi máy chủ khởi động, mở **http://localhost:8000** trong trình duyệt. Dừng máy chủ bằng `Ctrl+C` trong cửa sổ Terminal/PowerShell.

### Chạy bằng Docker

Đảm bảo Docker đã được cài đặt và đang chạy. Mở PowerShell hoặc Terminal tại thư mục gốc dự án, rồi chạy lệnh tương ứng:

**Windows (PowerShell):**

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS / Linux (Terminal):**

```bash
docker run --rm -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở **http://localhost:8080** để xem website. Container chạy ở cửa sổ hiện tại; nhấn `Ctrl+C` để dừng và tự xóa container. Nếu cổng `8080` đang được sử dụng, đổi `8080` ở phía trái của `-p` sang một cổng khác, chẳng hạn `8081`, rồi truy cập cổng mới đó.

## 9. Thông tin liên hệ

- **Tác giả:** Phan Hoàng Minh
- **Email:** [hoangminhphan1408@gmail.com](mailto:hoangminhphan1408@gmail.com)
- **GitHub:** [hoangminhphan1408-ctrl](https://github.com/hoangminhphan1408-ctrl)
