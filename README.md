# 📘 BÁO CÁO BÀI TẬP: TUẦN 3 & TUẦN 4
### GIÁO TRÌNH GIẢNG DẠY · HỌC PHẦN 111101 THIẾT KẾ WEB (ĐẠI HỌC LẠC HỒNG)

- **Sinh viên thực hiện:** **Huỳnh Mai Phát**
- **Mã học phần:** **111101 - Thiết kế Web**
- **Đơn vị đào tạo:** **Trường Đại học Lạc Hồng (LHU)**
- **Yêu cầu bổ sung đã hoàn thành:** 
  - Khớp 100% nội dung thực hành và bài tập trong giáo trình cho Tuần 3 và Tuần 4.
  - **Xóa bỏ hoàn toàn hình ảnh ở Tuần 3** (không dùng bất kỳ thẻ `<img>` nào, sử dụng 100% CSS Box và Typography thuần).
  - **Xóa bỏ toàn bộ nội dung Tuần 5**.

---

## 📂 1. CẤU TRÚC THƯ MỤC NỘP BÀI

```text
baitapvenhashowcase/
├── index.html                   # Trang Portal tổng hợp điều hướng Tuần 3 & Tuần 4
├── README.md                    # Bản báo cáo kỹ thuật chi tiết
│
├── tuan-3/                      # [TUẦN 3]: CSS LAYOUT SYSTEM (FLEXBOX & GRID)
│   ├── index.html               # Layout CSS Grid (Holy Grail), Skills Flexbox & The Grid Master
│   └── css/
│       └── portfolio.css        # CSS Grid-template-areas, Flexbox wrap gap 15px, Pricing table
│
└── tuan-4/                      # [TUẦN 4]: DESIGN SYSTEM & RESPONSIVE (MOBILE FIRST)
    ├── index.html               # 6 Bài tập tự rèn luyện tại nhà + Bảng đối chiếu Code Tốt/Rác
    ├── css/
    │   └── design-system.css    # Biến :root, Mobile First Breakpoints, Dark Mode (.dark-theme)
    └── js/
        └── design-system.js     # Script Hamburger Menu & Dark/Light Mode Switcher
```

---

## 📐 2. NỘI DUNG THỰC HIỆN TUẦN 3 (TRANG 26 - 32 GIÁO TRÌNH)
**Chủ đề: CSS LAYOUT SYSTEM (FLEXBOX & GRID)**

### 2.1. Cấu trúc tổng thể CSS Grid (Hoạt động 2 - Trang 28)
- Sử dụng thuộc tính `grid-template-areas` phân chia các phân vùng:
  - **Header:** Chiếm toàn bộ chiều ngang (`grid-area: header`).
  - **Sidebar:** Rộng cố định 250px ở bên trái (`grid-area: sidebar`).
  - **Main Content:** Chiếm toàn bộ không gian còn lại ở bên phải (`grid-area: main`).
  - **Footer:** Chiếm toàn bộ chiều ngang ở dưới cùng (`grid-area: footer`).
- Mã nguồn triển khai trong [`tuan-3/css/portfolio.css`](file:///c:/Users/Admin/baitapvenhashowcase/tuan-3/css/portfolio.css):
  ```css
  .portfolio-layout {
    display: grid;
    grid-template-columns: 250px 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
      "header header"
      "sidebar main"
      "footer footer";
    min-height: 100vh;
  }
  ```

### 2.2. Khu vực kỹ năng - Flexbox System (Trang 28)
- Đúng theo Prompt mẫu giáo trình:
  - Các item hiển thị dạng hàng ngang.
  - Tự động xuống dòng khi thiếu không gian (`flex-wrap: wrap`).
  - Khoảng cách giữa các item là `15px` (`gap: 15px`).
  - Căn giữa các item (`justify-content: center`).

### 2.3. Thách thức "The Grid Master" (Trang 32)
- Tạo lưới hiển thị 6 dự án bằng CSS Grid có kích thước bằng nhau (`repeat(3, 1fr)`).
- Khoảng cách đồng nhất bằng `gap: 20px`.
- **Đặc biệt (Xóa ảnh tuần 3):** Toàn bộ thẻ dự án và avatar của Huỳnh Mai Phát đều được xây dựng bằng các khối màu CSS, font chữ và badge code thuần túy, tuyệt đối **không sử dụng bất kỳ thẻ `<img>` nào**.

### 2.4. Bài tập mở rộng: Bảng giá dịch vụ (Trang 30)
- Thiết kế 3 bảng giá (Basic, Pro, Enterprise) nằm ngang hàng nhau bằng Flexbox.
- Nút "Mua ngay" luôn nằm sát đáy bảng giá dù nội dung dài ngắn khác nhau nhờ `display: flex; flex-direction: column;` và `margin-top: auto`.
- Hiệu ứng khi hover: Bảng giá phóng to nhẹ (`transform: scale(1.03)`).

---

## 🎨 3. NỘI DUNG THỰC HIỆN TUẦN 4 (TRANG 33 - 41 GIÁO TRÌNH)
**Chủ đề: DESIGN SYSTEM & TƯ DUY RESPONSIVE (MOBILE FIRST)**

### 3.1. Hệ thống biến Design System tại `:root` (Trang 34)
- 2 màu chủ đạo: `--primary-color: #2563eb;` (Xanh LHU), `--secondary-color: #0f172a;`.
- 3 mức màu xám cho text: `--text-dark: #1e293b;`, `--text-muted: #64748b;`, `--text-light: #f8fafc;`.
- Màu nền & viền: `--bg-color: #f8fafc;`, `--bg-card: #ffffff;`, `--border-color: #e2e8f0;`.
- Khoảng cách: `--spacing-base: 15px;`, `--spacing-lg: 30px;`.
- Thang font chữ: `--fs-h1`, `--fs-h2`, `--fs-h3`, `--fs-body`, `--fs-small`.

### 3.2. Chuỗi 6 Bài Tập Tự Rèn Luyện Tại Nhà (Trang 36)
1. **Bài 1: Responsive Typography Scale:** Tự động giảm cỡ chữ trên màn hình nhỏ hơn 600px qua Media Query để không bị tràn chữ.
2. **Bài 2: Adaptive Card Layout:** Sử dụng `flex-direction: column` trên Mobile (ảnh/khối trên, chữ dưới), tự chuyển sang `flex-direction: row` trên Desktop (ảnh bên trái, chữ bên phải).
3. **Bài 3: Smart Navigation Bar:** Ẩn toàn bộ menu ngang trên màn hình dưới 768px (`display: none`) và chỉ hiển thị nút Hamburger (`☰`).
4. **Bài 4: Dark/Light Mode Theme System:** Tạo class `.dark-theme` ghi đè trực tiếp các biến màu tại `:root`, có nút bấm bật/tắt thời gian thực trên thanh điều hướng.
5. **Bài 5: Responsive Image Gallery with CSS Grid:** Ứng dụng công thức vàng `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` tự động co giãn số lượng cột mà không cần lạm dụng Media Queries.
6. **Bài 6: Mobile-First Contact Form:** Trên Mobile ô nhập liệu chiếm 100% chiều rộng, trên Desktop giới hạn `max-width: 600px; margin: 0 auto;`.

### 3.3. Bảng đối chiếu "Code Tốt" vs "Code Rác" (Trang 40)
- Trình bày trực tiếp bảng so sánh chất lượng mã nguồn CSS chuẩn xác theo giáo trình.

---

## 🚀 4. HƯỚNG DẪN KIỂM THỬ

- Mở trực tiếp file [`index.html`](file:///c:/Users/Admin/baitapvenhashowcase/index.html) để truy cập cổng điều hướng tổng hợp.
- Mở [`tuan-3/index.html`](file:///c:/Users/Admin/baitapvenhashowcase/tuan-3/index.html) để kiểm tra bố cục Grid/Flexbox của Huỳnh Mai Phát (đã xóa toàn bộ ảnh).
- Mở [`tuan-4/index.html`](file:///c:/Users/Admin/baitapvenhashowcase/tuan-4/index.html) để kiểm tra 6 bài tập rèn luyện Tuần 4 và tính năng Dark Mode.