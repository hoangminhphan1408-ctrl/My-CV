# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Giá trị |
|---|---|
| Tên dự án | My-CV — Website portfolio cá nhân |
| Phiên bản | v1.0.0 |
| Ngày kiểm thử/đánh giá | 05/11/2026 |
| Người thực hiện/đánh giá | [Điền tên người kiểm thử] |
| Phạm vi đánh giá | Rà soát mã nguồn HTML/CSS và tài liệu bàn giao trong repository |
| Môi trường kiểm thử | Microsoft Edge headless; website mở cục bộ từ `index.html` |
| Viewport chụp ảnh | Mobile 390 × 844 px; tablet 768 × 1024 px; desktop 1440 × 900 px |
| Phương pháp | Rà soát mã nguồn/README và chụp màn hình tại các viewport mô phỏng; không sử dụng thiết bị vật lý |

> **Lưu ý:** Ảnh responsive là ảnh chụp trình duyệt tại viewport mô phỏng, không phải ảnh chụp từ điện thoại hoặc máy tính bảng vật lý. Các nội dung yêu cầu kiểm tra thiết bị thực tế hoặc triển khai được đánh dấu cần kiểm thử bổ sung.

## 2. Quy ước trạng thái

- **Đạt:** Có thể xác nhận hạng mục từ bằng chứng đã rà soát.
- **Chưa đạt:** Đã phát hiện lỗi hoặc thiếu sót cụ thể so với kỳ vọng bàn giao.
- **Cần cải thiện:** Chưa có đủ bằng chứng để kết luận, hoặc cần kiểm thử/hoàn thiện thêm.

## 3. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các mục nội dung và điều hướng chính hiện diện; liên kết GitHub và liên kết chi tiết trò chơi chưa được cấu hình đích. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Chưa đạt | Đã chụp ảnh ở ba viewport; tại mobile 390 px, nội dung đoạn giới thiệu bị cắt ở mép phải. Chưa kiểm thử thiết bị vật lý/trình duyệt khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Website tĩnh, không có backend; chưa có kết quả chạy thử, kiểm tra tải tài nguyên hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Phạm vi xử lý dữ liệu có vẻ hạn chế; chưa có đánh giá bảo mật hoặc xác nhận chính thức về việc công khai thông tin liên hệ. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có README, release note và cấu trúc tài nguyên; phát hiện markup thừa tại phần Liên hệ cần sửa. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã có ảnh responsive mobile/tablet/desktop; chưa có biên bản kiểm thử đầy đủ hoặc kết quả triển khai trên môi trường bàn giao. |

## 4. Chi tiết kiểm tra

### 4.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có nội dung giới thiệu cá nhân và định hướng nghề nghiệp | Đạt | Nội dung giới thiệu và vai trò Frontend Developer có trong `index.html`. |
| Có phần kỹ năng và danh sách trò chơi | Đạt | Có các mục Kỹ năng và Dự án; bốn thẻ trò chơi được khai báo trong `index.html`. |
| Điều hướng đến các phần chính của trang | Đạt | Các liên kết Giới thiệu, Kỹ năng, Dự án, Liên hệ trỏ đến các ID tương ứng trong trang. Xác nhận tĩnh từ `index.html`; chưa kiểm tra tương tác trên trình duyệt. |
| Liên kết email mở đúng địa chỉ | Cần cải thiện | Có liên kết `mailto:` trong phần Liên hệ; chưa thực hiện thao tác nhấp để xác nhận trên trình duyệt. |
| Các liên kết “Xem chi tiết” hoạt động đúng mục đích | Chưa đạt | Bốn thẻ trò chơi dùng `href="#"`, chưa trỏ đến trang hoặc nội dung chi tiết. |
| Liên kết GitHub mở đúng hồ sơ | Chưa đạt | Nội dung hiển thị URL GitHub nhưng thuộc tính liên kết là `href="#"`. |

### 4.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có quy tắc bố cục responsive | Đạt | `assets/css/styles.css` khai báo breakpoint tại 768px và 1280px. Đây là xác nhận từ mã nguồn, chưa phải kết quả kiểm thử trên thiết bị. |
| Hình ảnh có giới hạn kích thước để tránh tràn bố cục | Đạt | CSS có quy tắc giới hạn chiều rộng hình ảnh; một số hình ảnh trong HTML có thuộc tính kích thước và văn bản thay thế. |
| Điều hướng hỗ trợ trạng thái focus nhìn thấy được | Đạt | CSS có `:focus-visible` cho liên kết/điều khiển. Chưa kiểm thử thao tác bàn phím thực tế. |
| Kiểm tra giao diện ở điện thoại, tablet và desktop | Chưa đạt | Đã chụp tại các viewport mô phỏng; ảnh mobile cho thấy đoạn giới thiệu bị cắt ngang. Xem minh chứng bên dưới. |
| Kiểm tra trên các trình duyệt mục tiêu | Cần cải thiện | README nêu trình duyệt hiện đại nhưng chưa có biên bản kiểm tra Chrome, Firefox, Edge hoặc Safari. |
| Kiểm tra độ dễ đọc, tương phản màu và khả năng tiếp cận | Cần cải thiện | Chưa có đánh giá tương phản, phóng to nội dung, trình đọc màn hình hoặc kiểm tra accessibility tự động/thủ công. |

#### Minh chứng responsive

Ảnh chụp bằng Microsoft Edge headless tại các viewport nêu trong phần Thông tin chung:

| Thiết bị mô phỏng | Kích thước viewport | Ảnh chụp |
|---|---:|---|
| Mobile | 390 × 844 px | [responsive-mobile.png](screenshots/responsive-mobile.png) |
| Tablet | 768 × 1024 px | [responsive-tablet.png](screenshots/responsive-tablet.png) |
| Desktop | 1440 × 900 px | [responsive-desktop.png](screenshots/responsive-desktop.png) |

**Phát hiện:** Ở viewport mobile, một phần văn bản giới thiệu không xuống dòng vừa khung và bị cắt ở cạnh phải. Cần khắc phục và chụp lại minh chứng sau khi sửa.

### 4.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Website không phụ thuộc backend để hiển thị nội dung | Đạt | README mô tả website tĩnh sử dụng HTML/CSS, không có backend, API hoặc cơ sở dữ liệu. |
| Tài nguyên cục bộ được tham chiếu đúng | Cần cải thiện | HTML tham chiếu CSS và hình ảnh trong `assets/`; chưa chạy website để xác nhận mọi yêu cầu tài nguyên trả về thành công. |
| Xử lý lỗi khi thiếu hình ảnh hoặc CSS | Cần cải thiện | Chưa có kiểm thử mô phỏng tài nguyên bị thiếu hoặc đường dẫn sai. |
| Tốc độ tải và dung lượng tài nguyên | Cần cải thiện | Chưa đo thời gian tải, kích thước ảnh thực tế, chỉ số hiệu năng hoặc trải nghiệm mạng chậm. |
| Kiểm tra lỗi hiển thị và lỗi console | Cần cải thiện | Chưa có kết quả kiểm tra DevTools/console sau khi chạy website. |

### 4.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Kiểm tra thông tin bí mật trong mã nguồn và cấu hình | Cần cải thiện | Rà soát phạm vi tài liệu/mã nguồn được dùng để lập báo cáo không ghi nhận cấu hình backend; chưa thực hiện quy trình quét secrets chuyên dụng trên toàn bộ lịch sử repository. |
| Xác định dữ liệu người dùng được thu thập/lưu trữ | Đạt | Theo README, dự án không có backend, cơ sở dữ liệu hoặc API; chưa thấy chức năng biểu mẫu trong trang được rà soát. |
| Xác nhận quyền công khai thông tin cá nhân | Cần cải thiện | Trang hiển thị email và thông tin hồ sơ GitHub. Chủ sở hữu cần xác nhận các thông tin này được phép công khai trước khi xuất bản. |
| Rà soát phụ thuộc bên thứ ba và cấu hình triển khai | Cần cải thiện | Repository được mô tả không cần trình quản lý gói; chưa kiểm tra môi trường triển khai thực tế, cấu hình máy chủ hoặc header bảo mật. |
| Kiểm tra hành vi liên kết ra ngoài | Cần cải thiện | Liên kết GitHub chưa cấu hình URL đích; chưa có kiểm thử các liên kết bên ngoài sau khi cập nhật. |

### 4.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc mã nguồn và tài nguyên dễ nhận biết | Đạt | Có `index.html`, `assets/css/` và `assets/img/`; README hướng dẫn giữ nguyên cấu trúc khi triển khai. |
| Có hướng dẫn cài đặt/chạy dự án | Đạt | README có hướng dẫn mở trực tiếp, chạy máy chủ HTTP cục bộ và chạy bằng Docker. |
| Có tài liệu phát hành | Đạt | `docs/RELEASENOTE.md` ghi phiên bản v1.0.0, chức năng và hạn chế đã biết. |
| HTML không có thẻ đóng thừa hoặc sai cấu trúc | Chưa đạt | Rà soát `index.html` thấy chuỗi đóng `</a></li>` thừa trong phần Liên hệ, ngay trước mục GitHub; cần sửa và kiểm tra lại HTML. |
| Mã nguồn có kiểm tra tự động/lint phù hợp | Cần cải thiện | Chưa thấy kết quả lint/validator hoặc bộ kiểm thử tự động được cung cấp trong tài liệu bàn giao. |
| Nội dung và liên kết mẫu đã được thay bằng dữ liệu bàn giao chính thức | Chưa đạt | README xác nhận liên kết chi tiết là liên kết mẫu; liên kết GitHub trong trang cũng chưa có đích thực tế. |

### 4.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn triển khai/chạy cục bộ | Đạt | README hướng dẫn chạy bằng Python HTTP server và Docker/Nginx. |
| Xác nhận quy trình triển khai hoạt động trên môi trường bàn giao | Cần cải thiện | Có hướng dẫn nhưng chưa có biên bản thực thi trên môi trường đích. |
| Có test case và kết quả kiểm thử chức năng | Cần cải thiện | Báo cáo này là checklist đối chiếu; chưa có log thực thi test case trên trình duyệt. |
| Có ảnh chụp hoặc minh chứng kiểm thử | Đạt | Đã lưu ảnh responsive tại `docs/screenshots/`; chưa có video, log console hoặc báo cáo đo hiệu năng. |
| Có xác nhận sau khi sửa các lỗi phát hiện | Cần cải thiện | Cần chạy lại các mục chưa đạt sau khi sửa liên kết và markup. |

## 5. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm có phạm vi phù hợp với một website portfolio tĩnh: nội dung chính, điều hướng nội bộ, tài nguyên CSS/hình ảnh và hướng dẫn chạy dự án đã được cung cấp. Tuy nhiên, mức độ sẵn sàng bàn giao hiện tại **chưa được xác nhận đầy đủ** vì chưa có kiểm thử runtime trên trình duyệt/thiết bị và chưa có minh chứng triển khai. Một số liên kết hiển thị trên trang chưa hoạt động đúng mục đích; mã HTML phần Liên hệ có thẻ đóng thừa.

### Vấn đề cần khắc phục trước khi bàn giao

1. Cấu hình URL đích thật cho liên kết GitHub và các liên kết “Xem chi tiết”, hoặc bỏ các liên kết chưa có nội dung đích.
2. Sửa markup thừa trong phần Liên hệ của `index.html`, sau đó chạy HTML validator hoặc công cụ kiểm tra tương đương.
3. Sửa lỗi văn bản giới thiệu bị cắt ở viewport mobile, rồi chụp lại ảnh responsive để xác nhận.
4. Chạy thử website qua hướng dẫn README; xác nhận CSS và tất cả hình ảnh tải thành công, không có lỗi console.
5. Kiểm tra điều hướng, email, bàn phím và bố cục trên thiết bị/trình duyệt mục tiêu; lưu ảnh chụp/minh chứng.
6. Xác nhận chủ sở hữu đồng ý công khai email và thông tin hồ sơ; rà soát cấu hình môi trường triển khai trước khi xuất bản.

### Điều kiện đề xuất để xác nhận bàn giao

- Không còn lỗi chức năng mức nghiêm trọng; các liên kết hiển thị dẫn đến đích hợp lệ.
- Markup được xác thực và website hiển thị đúng trên các viewport mục tiêu.
- Có kết quả kiểm thử thực tế và minh chứng tối thiểu (môi trường, trình duyệt, kết quả, ảnh chụp hoặc log).
- Các thông tin cá nhân và cấu hình triển khai đã được chủ sở hữu xác nhận.

**Kết luận:** Chưa nên xác nhận hoàn tất bàn giao cho đến khi xử lý các mục **Chưa đạt** và bổ sung minh chứng cho các mục **Cần cải thiện** nêu trên.