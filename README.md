# Chuyển Tập Tin "Dưỡng Sinh.DOCX" Thành HTML

**Tác giả:** Dương Tấn Chánh

---

## 📖 Giới Thiệu

**Chuyển Tập Tin "Dưỡng Sinh.DOCX" Thành HTML** là ứng dụng web Single-Page hỗ trợ chuyển đổi tài liệu Microsoft Word (`.docx`) sang định dạng HTML tương tác nguyên bản, tối ưu cho việc đọc nội dung trên thiết bị di động cũng như máy tính cá nhân.

Ứng dụng xử lý cấu trúc tài liệu một cách thông minh: tự động trích xuất dòng đầu làm tiêu đề `<h1>`, tự động chuyển các mục Heading thành các khối ẩn/hiện `<details>/<summary>` với màu sắc nhận diện trực quan cho từng cấp (H2-H5), trình bày khối văn bản tràn ngang tối đa kèm khung viền đồng màu để đọc thoải mái nhất trên điện thoại, chuẩn hoá thụt lề bullet theo quy ước chuẩn Markdown, và loại bỏ các phần mục lục dư thừa từ file Word gốc.

---

## ✨ Tính Năng Nổi Bật

- 📁 **Mở Tập Tin Linh Hoạt**:
  - Nhấp nút bấm chọn tập tin từ thiết bị.
  - Kéo và thả tập tin `.docx` trực tiếp vào khung ứng dụng.
  - Dán tập tin đã sao chép (`Ctrl+V` / `Cmd+V`) trực tiếp từ bộ nhớ tạm.
- ✂️ **Xử Lý Tiêu Đề & Mục Lục Thông Minh**:
  - Tự động lấy dòng đầu tiên của tài liệu làm tiêu đề chính `<h1>`.
  - Tự động phát hiện và loại bỏ các khối Mục Lục Word (Table of Contents) dư thừa.
- 🎨 **Màu Sắc & Phân Cấp Heading (H1-H5)**:
  - **Tiêu Đề Chính (H1)**: Tím mận sẫm (`#4A154B`), đồng màu với Heading 2.
  - **Heading Cấp 1 (H2)**: Tím mận sẫm (`#4A154B`), căn lề chuẩn (`margin-left: 0`).
  - **Heading Cấp 2 (H3)**: Nâu đỏ sẫm (`#782813`), thụt lề cấp 2 (`margin-left: 0.8rem`).
  - **Heading Cấp 3 (H4)**: Nâu vàng hổ phách (`#9E6510`), thụt lề cấp 3 (`margin-left: 1.6rem`).
  - **Heading Cấp 4 (H5)**: Xanh lục rêu sẫm (`#365E14`), thụt lề cấp 4 (`margin-left: 2.4rem`).
  - Mỗi mục Heading có biểu tượng tam giác `▶` xoay chuyển mượt mà 90 độ xuống dưới khi mở rộng nội dung.
- 📱 **Khung Viền 3px Đồng Màu & Trải Rộng Tối Đa Cho Điện Thoại**:
  - Toàn bộ khối văn bản và danh sách con (kể cả khối nội dung trực tiếp dưới Heading 1) được mở rộng bề rộng tối đa theo chiều ngang (`width: 100%`, không thụt lề thân bài) giúp trải nghiệm đọc trên điện thoại luôn thoáng đãng.
  - Bao viền dày 3px rõ nét tương ứng với mã màu của từng cấp Heading cha (Nội dung dưới H1 & H2 mang viền tím mận sẫm `#4A154B`, H3 mang viền nâu đỏ sẫm `#782813`, H4 mang viền nâu vàng hổ phách `#9E6510`, H5 mang viền xanh lục rêu sẫm `#365E14`).
- 📂 **Cấu Trúc Cây Phân Cấp `<details>`**:
  - Các mục Heading tự động bao bọc trong thẻ `<details>` mặc định thu gọn, nhấp để mở rộng.
  - Cung cấp nút điều khiển "Mở tất cả" / "Thu gọn tất cả" canh giữa trang, nền xám `#808080`, chữ trắng `#FFFFFF`, không viền trang nhã.
- 📌 **Chuẩn Hoá Bullet Theo Quy Ước Markdown**:
  - Tự động nhận diện bullet chuẩn Markdown (`- `, `* `, `+ `, `• `) hoặc danh sách từ Word XML.
  - Phân cấp mức độ theo cơ chế thụt lề tương đối chuẩn Markdown (mỗi cấp con thụt lề thêm từ 2 đến 5 khoảng trắng so với mốc của cấp cha liền trước, tự động lùi cấp khi giảm thụt lề).
  - Tự động làm sạch các tiền tố ký hiệu thừa ở đầu câu khi chuyển thành thẻ `<li>`.
- 🔗 **Liên Kết Tham Chiếu Nội Bộ**:
  - Tự động chuyển các câu tham chiếu nội bộ ("xem trang...", "xem mục...") thành liên kết neo thông minh.
- 💾 **Xuất Tập Tin Nhanh Dễ Dàng**:
  - Tải file HTML kết quả chỉ với một cú nhấp chuột.
  - Tự động đặt tên tập tin đầu ra khớp với tên tập tin `.docx` nhập vào.
- ⚡ **Tối Ưu Hiệu Năng & Offline**:
  - Viết bằng Vanilla JS sạch sẽ, bắt lỗi đầy đủ.
  - Sử dụng phông chữ hệ thống (`system-ui`), không tải phông từ liên kết ngoài, hỗ trợ chạy offline tốc độ cao.
  - Thiết kế giao diện phẳng, tương thích mọi thiết bị từ điện thoại cấu hình thấp đến máy vi tính.

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
- **Tác giả**: Dương Tấn Chánh.

---

## 📄 Giấy Phép & Bản Quyền

Bản quyền © 2026 **Dương Tấn Chánh**. Tất cả các quyền được bảo lưu.

