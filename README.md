# Chuyển Tập Tin "Dưỡng Sinh.DOCX" Thành HTML

**Tác giả:** Dương Tấn Chánh (D.T.Chánh)

---

## 📖 Giới Thiệu

**Chuyển Tập Tin "Dưỡng Sinh.DOCX" Thành HTML** là ứng dụng web Single-Page hỗ trợ chuyển đổi tài liệu Microsoft Word (`.docx`) sang định dạng HTML tương tác nguyên bản, tối ưu cho việc đọc nội dung trên thiết bị di động cũng như máy tính cá nhân.

Ứng dụng xử lý cấu trúc tài liệu một cách thông minh: tự động trích xuất dòng đầu làm tiêu đề `<h1>`, tự động chuyển các mục Heading thành các khối ẩn/hện `<details>/<summary>`, chuẩn hoá thụt lề bullet (mức 1 với `©`, mức 2 với `-`), và loại bỏ các phần mục lục dư thừa từ file Word gốc.

---

## ✨ Tính Năng Nổi Bật

- 📁 **Mở Tập Tin Linh Hoạt**:
  - Nhấp nút bấm chọn tập tin từ thiết bị.
  - Kéo và thả tập tin `.docx` trực tiếp vào khung ứng dụng.
  - Dán tập tin đã sao chép (`Ctrl+V` / `Cmd+V`) trực tiếp từ bộ nhớ tạm.
- ✂️ **Xử Lý Tiêu Đề & Mục Lục Thông Minh**:
  - Tự động lấy dòng đầu tiên của tài liệu làm tiêu đề chính `<h1>`.
  - Tự động phát hiện và loại bỏ các khối Mục Lục Word (Table of Contents) dư thừa.
- 📂 **Cấu Trúc Cây Phân Cấp `<details>`**:
  - Các mục Heading (H2, H3, H4, H5...) tự động bao bọc trong thẻ `<details>` có thể thu gọn/mở rộng.
  - Cung cấp nút điều khiển "Mở tất cả" / "Thu gọn tất cả" nhanh chóng.
- 📌 **Chuẩn Hoá Bullet & Ký Hiệu**:
  - Tự động phân loại bullet mức 1 (ký hiệu `©`) và bullet mức 2 (dấu `-`).
  - Tự động làm sạch các dấu gạch hoặc ký hiệu trùng lặp ở đầu câu.
- 🔗 **Liên Kết Tham Chiếu Nội Bộ**:
  - Tự động chuyển các câu tham chiếu nội bộ ("xem trang...", "xem mục...") thành liên kết neo thông minh.
- 💾 **Xuất Tập Tin Nhanh Dễ Dàng**:
  - Tải file HTML kết quả chỉ với một cú nhấp chuột.
  - Tự động đặt tên tập tin đầu ra khớp với tên tập tin `.docx` nhập vào.
- ⚡ **Tối Ưu Hiệu Năng & Offline**:
  - Viết bằng Vanilla JS sạch sẽ, bắt lỗi đầy đủ.
  - Sử dụng phông chữ hệ thống (`system-ui`), không tải phông từ liên kết ngoài, hỗ trợ chạy offline tốc độ cao.
  - Thiết kế giao diện phẳng, tối giản (tối đa 4 màu chính), tương thích mọi thiết bị từ điện thoại cấu hình thấp đến máy vi tính.

---

## 🛠️ Cấu Trúc Dự Án

```
.
├── index.html        # File giao diện và mã nguồn ứng dụng chính (HTML/CSS/JS)
├── js/               # Thư mục chứa thư viện JavaScript cục bộ (JSZip)
│   └── jszip.min.js  # Thư viện giải nén tập tin DOCX offline
├── metadata.json     # Thông tin cấu hình ứng dụng
├── package.json      # Khai báo phụ thuộc và các câu lệnh
├── tsconfig.json     # Cấu hình TypeScript
└── README.md         # Tài liệu hướng dẫn sử dụng
```

---

## 🚀 Hướng Dẫn Khởi Chạy

### Khởi chạy môi trường phát triển (Development):

```bash
npm install
npm run dev
```

Trình duyệt sẽ mở ứng dụng tại địa chỉ `http://localhost:3000`.

### Kiểm tra mã nguồn (Lint) & Đóng gói (Build):

```bash
npm run lint
npm run build
```

---

## 🎨 Quy Chuẩn Giao Diện & Mã Nguồn

- **Mã hóa chuỗi**: Chuẩn mã hóa UTF-8, hỗ trợ hiển thị tiếng Việt hoàn chỉnh.
- **Biến CSS (`:root`)**: Quản lý màu sắc, khoảng cách, viền và phông chữ tập trung.
- **Typography**: Đơn vị đo `rem` linh hoạt, viền sử dụng đơn vị `px` tối thiểu 2px.
- **Tác giả**: Dương Tấn Chánh (`D.T.Chánh`).

---

## 📄 Giấy Phép & Bản Quyền

Bản quyền © 2026 **Dương Tấn Chánh**. Tất cả các quyền được bảo lưu.
