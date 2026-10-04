# Kế Hoạch Thiết Kế Mockup "Truyền Hình Công Thương" (Cảm Hứng The Wired + Bản Sắc Đỏ - Xanh)

> **Tầm nhìn thiết kế**: Kết hợp đỉnh cao giữa **cấu trúc tạp chí báo chí hiện đại của The Wired** (Editorial grid sắc sảo, đường kẻ hairline 1px, typography quyền lực, khối The Big Story, Trending 01-05) với **hệ nhận diện Đỏ - Xanh truyền thống của Truyền Hình Công Thương** (Đỏ cờ Bộ Công Thương `#C4161C` và Xanh dương đài truyền hình `#004B87`).
> **Toàn bộ nội dung hardcoded 100%**: Dữ liệu thật từ kho bài viết cào được, không dùng chữ mẫu vô nghĩa, độc lập hoàn toàn trong thư mục `u2`, sẵn sàng đẩy lên GitHub riêng.

---

## 1. Hệ Nhận Diện Thương Hiệu: "The Wired Meets Truyền Hình Công Thương"

```
+-------------------------------------------------------------------------------+
|  THE WIRED EDITORIAL ARCHITECTURE          BẢN SẮC TRUYỀN HÌNH CÔNG THƯƠNG   |
|  - Bố cục lưới Hairline 1px sắc nét        - Đỏ cờ đặc trưng: #C4161C         |
|  - Tiêu đề Serif lớn, đanh thép            - Xanh đài truyền hình: #004B87    |
|  - Nhãn Kicker viết hoa bold (TAGS)        - Xanh Navy chiều sâu: #071526     |
|  - Khối Trending đánh số 01 - 05 to bản    - Trắng kem báo chí: #F8FAFC       |
|  - Phân khu Media Dark sang trọng          - Logo & Slogan chuẩn Bộ Công Thương |
+-------------------------------------------------------------------------------+
```

### Bảng Mã Màu Chi Tiết (Tailwind Config / CSS Tokens)
* **Màu Đỏ Chủ Đạo (Công Thương Red)**: `#C4161C` / `#B91C1C`
  - *Ứng dụng*: Nhãn danh mục (Tag Kicker), dải tin nóng Breaking News, số thứ tự Trending `01-05`, vạch chỉ báo bài đọc, nút CTA và hover links.
* **Màu Xanh Dương Nhận Diện (Broadcast Blue)**: `#004B87` / `#0284C7`
  - *Ứng dụng*: Thanh Topbar điều hành, viền khối chuyên mục chính, biểu tượng phát sóng, link tiểu mục, icon tương tác.
* **Màu Nền Tương Phản Sâu (Deep Navy Broadcast Dark)**: `#071526` / `#0B192C`
  - *Ứng dụng*: Thay vì dùng màu đen tuyền đơn điệu như Wired gốc, ta sử dụng **Xanh Navy sẫm** cho khối **Truyền Hình Đa Phương Tiện (Wired Media)**, mang lại cảm giác đẳng cấp của phim trường truyền hình hiện đại.
* **Màu Nền Báo & Văn Bản**:
  - Nền trang: `#F8FAFC` (Off-white tạo cảm giác trang giấy tạp chí cao cấp, dịu mắt).
  - Màu chữ tiêu đề: `#0F172A` (Slate Black đanh thép, độ tương phản tuyệt đối).
  - Màu chữ nội dung: `#334155` (Slate Gray dễ đọc chuẩn báo chí).
  - Đường kẻ phân cách: `#E2E8F0` / `#CBD5E1` (Hairline border 1px tinh tế).

### Hệ Thống Typography Báo Chí
* **Tiêu Đề (Headlines)**: `Playfair Display` & `Merriweather` (Google Fonts tiếng Việt) – Sang trọng, đĩnh đạc, mang phong thái cơ quan ngôn luận báo chí hàng đầu.
* **Nội dung & Nhãn (Body & Kickers)**: `Be Vietnam Pro` & `Inter` – Tối ưu hóa hiển thị tiếng Việt trên màn hình số, độ sắc nét cao từ di động đến màn hình 4K.
* **Bộ Số Trending**: `Space Grotesk` / Mono Serif đậm – Dành riêng cho các con số `01`, `02`, `03`, `04`, `05` phong cách Wired.

---

## 2. Toàn Bộ Nội Dung Hardcoded (Dữ Liệu Thật 100%)

Toàn bộ tin bài, video, số liệu được hardcode chuẩn xác trong file [u2/js/data.js](file:///c:/Users/PC/Desktop/truyenhinhcongthuong/u2/js/data.js), trích xuất từ các file JSON đã cào sẵn trong dự án:

1. **Tin Tiêu Điểm Lớn ("The Big Story")**:
   - *Tiêu đề*: "Quy hoạch điện VIII: Cú hích chiến lược cho chuyển dịch năng lượng xanh và đảm bảo an ninh năng lượng quốc gia".
   - *Sapo*: Đánh giá toàn diện các chính sách đột phá của Bộ Công Thương nhằm khai phóng nguồn năng lượng tái tạo, điện gió ngoài khơi và định hình bức tranh năng lượng Việt Nam tầm nhìn 2045.
   - *Ảnh đại diện*: Ảnh dự án điện gió ngoài khơi độ phân giải cao.
   - *Byline*: Ban Năng lượng & Công nghiệp · 15 phút trước.
2. **4 Tin Vệ Tinh Khối Hero**:
   - "Thương mại điện tử Việt Nam vượt mốc 25 tỷ USD: Đòn bẩy đưa hàng Việt vươn ra biển lớn qua các sàn quốc tế".
   - "EVFTA sau 5 năm thực thi: Nông sản và dệt may Việt Nam khẳng định vị thế vững chắc tại thị trường EU".
   - "Bình ổn thị trường xăng dầu: Tăng cường giám sát số hóa chuỗi cung ứng từ tổng kho đến cây xăng".
   - "Bộ Công Thương tăng tốc giải pháp hỗ trợ doanh nghiệp vượt rào cản kỹ thuật CBAM của châu Âu".
3. **5 Bài Viết Xu Hướng ("Trending 01 - 05")**:
   - `01`: Biến động giá vàng và tỷ giá: Tác động đa chiều đến doanh nghiệp xuất nhập khẩu.
   - `02`: Đột phá chuyển đổi số ngành bán lẻ: Trải nghiệm tiêu dùng thông minh thời kỳ mới.
   - `03`: Khởi công tổ hợp hóa dầu và logistics năng lượng sạch tại miền Trung.
   - `04`: Xuất khẩu sầu riêng và thanh long sang thị trường Trung Quốc lập kỷ lục mới.
   - `05`: Kiểm tra liên ngành công tác phòng chống gian lận xuất xứ hàng hóa.
4. **Khối Video Truyền Hình Nổi Bật (Wired Broadcast Spotlight - Nền Xanh Navy `#071526`)**:
   - Video chính phát trực tiếp: "Bản tin Thời sự Công Thương 24h: Nỗ lực đảm bảo nguồn cung hàng hóa thiết yếu" (Link YouTube iframe hoạt động thật).
   - 4 Video phóng sự vệ tinh kèm thời lượng: `08:45`, `15:20`, `04:12`, `10:30`.
5. **Các Khối Chuyên Mục Báo Chí Chuyên Biệt**:
   - **Khối Công Nghiệp & Năng Lượng**: Điện khí LNG, Khai thác khoáng sản bền vững, Công nghiệp hỗ trợ.
   - **Khối Thương Mại & Xuất Nhập Khẩu**: Xúc tiến thương mại 2026, Phân tích thị trường Mỹ - EU - ASEAN.
   - **Khối Khoa Học & Chuyển Đổi Số**: AI trong quản lý lưới điện thông minh, Tự động hóa nhà máy.

---

## 3. Kiến Trúc Trang Web & Chi Tiết Từng Khối Bố Cục

```
+-----------------------------------------------------------------------------------------------+
| TOPBAR (Đồng hồ tiếng Việt thực | Tỷ giá USD, EUR | Giá xăng dầu | Hotline: 024.3934.xxxx)    |
+-----------------------------------------------------------------------------------------------+
| MASTHEAD (Logo Truyền Hình Công Thương Đỏ-Xanh | Slogan chính thức | Nút Search & Mobile Menu)|
+-----------------------------------------------------------------------------------------------+
| THE NAVIGATION (Menu chính: Trang chủ, Thời sự, Công nghiệp, Thương mại, Hội nhập, Media)    |
+-----------------------------------------------------------------------------------------------+
| BREAKING NEWS TICKER (Nền đỏ #C4161C: Dải chữ tin nóng ngành công thương chuyển động mượt mà) |
+-----------------------------------------------------------------------------------------------+
| HERO SECTION - THE WIRED BIG STORY                                                            |
| +---------------------------------------------------+ +-------------------------------------+ |
| | CỘT TRÁI (65%): TIN ĐINH KHỔ LỚN                  | | CỘT PHẢI (35%): 4 TIN VỆ TINH       | |
| | [TAG: CÔNG NGHIỆP]                                | | [TAG: THƯƠNG MẠI] - Tiêu đề tin 1   | |
| | TIÊU ĐỀ SERIF LỚN - ĐANH THÉP                     | | ----------------------------------- | |
| | [ẢNH PHÓNG SỰ KHỔ RỘNG CHẤT LƯỢNG CAO]            | | [TAG: HỘI NHẬP] - Tiêu đề tin 2     | |
| | Đoạn Sapo phân tích thời sự sâu sắc...            | | ----------------------------------- | |
| | Byline: Ban Biên tập · 15 phút trước              | | [TAG: NĂNG LƯỢNG] - Tiêu đề tin 3   | |
| +---------------------------------------------------+ +-------------------------------------+ |
+-----------------------------------------------------------------------------------------------+
| TRENDING / XEM NHIỀU NHẤT (THE WIRED NUMERIC COUNTER)                                         |
| [ 01 ] Tin nóng số 1   | [ 02 ] Tin nóng số 2   | [ 03 ] Tin nóng số 3   | [ 04 ] | [ 05 ]   |
+-----------------------------------------------------------------------------------------------+
| PHÂN KHU MEDIA TRUYỀN HÌNH - WIRED BROADCAST (NỀN XANH NAVY #071526, CHỮ TRẮNG, VIỀN ĐỎ)     |
| +---------------------------------------------------+ +-------------------------------------+ |
| | Video Player Chính (Bản tin 24h phát YouTube)     | | Danh sách 4 Video Phóng sự hot      | |
| | Nút Play nổi bật, tiêu đề và tóm tắt bản tin      | | Có thumbnail, thời lượng (08:45)    | |
| +---------------------------------------------------+ +-------------------------------------+ |
+-----------------------------------------------------------------------------------------------+
| KHỐI CHUYÊN MỤC BÁO CHÍ CHUYÊN SÂU (Grid 3 cột Hairline phân cách tinh tế)                    |
| [ CỘT 1: CÔNG NGHIỆP & NĂNG LƯỢNG ] | [ CỘT 2: THƯƠNG MẠI THỊ TRƯỜNG ] | [ CỘT 3: HỘI NHẬP ]  |
+-----------------------------------------------------------------------------------------------+
| FOOTER TÒA SOẠN CHUẨN CƠ QUAN BỘ CÔNG THƯƠNG (Giấy phép, Ban biên tập, Địa chỉ, Bản quyền)   |
+-----------------------------------------------------------------------------------------------+
```

---

## 4. Các Màn Hình Chi Tiết Trong `u2`

### 4.1. Trang Chủ (`index.html`)
- Masthead ấn tượng với phong cách tạp chí Wired: logo Truyền hình Công Thương sắc nét, slogan thời sự.
- Khối Tin Đinh (The Big Story) chiếm lĩnh góc nhìn với ảnh phóng sự khổ lớn.
- Thanh đếm số Trending `01-05` màu đỏ `#C4161C` kích thước lớn.
- Khối Truyền hình Đa phương tiện nền xanh navy `#071526` sang trọng.
- Banner tuyên truyền EVFTA và Xúc tiến thương mại.

### 4.2. Trang Đọc Bài Viết (`detail.html`)
- **Breadcrumb chuẩn SEO**: Trang chủ > Công nghiệp & Năng lượng > Chi tiết bài viết.
- **Tiêu đề H1 Serif lớn**, đoạn Sapo in đậm với đường kẻ viền trái màu đỏ nhận diện.
- **Reading Toolbar đa năng**:
  - Tăng / giảm cỡ chữ đọc (`A-` / `A+`).
  - Nút Copy Link bài viết (hiển thị popup thông báo tức thì).
  - Nút chia sẻ mạng xã hội Facebook, Zalo, In bài (`window.print()`).
- **Nội dung bài viết phong cách The Wired**:
  - Chữ cái mở đầu (Drop-cap) cách điệu màu xanh dương `#004B87`.
  - Khung trích dẫn phát biểu (Pull-quote) viền đỏ `#C4161C` nổi bật.
  - Ảnh phóng sự chèn giữa bài kèm chú thích chi tiết.
- **Khung Bình Luận Tương Tác (Interactive Mockup)**:
  - Cho phép người xem nhập Họ tên, Nội dung và bấm "Gửi bình luận".
  - Bình luận mới sẽ lập tức được thêm vào danh sách hiển thị (lưu vào state/LocalStorage).
- **Khối 4 Bài viết liên quan** cùng chuyên mục.

### 4.3. Trang Chuyên Mục (`category.html`) & Trang Video (`video.html`)
- Phân loại theo từng lĩnh vực: Công nghiệp, Thương mại, Hội nhập, Chuyển đổi số.
- Bộ lọc bài viết (Mới nhất, Đọc nhiều nhất) và lưới bài viết 3 cột chuẩn tạp chí.
- Trang Video với player popup YouTube tiện lợi.

---

## 5. Kế Hoạch Triển Khai Code Từng Bước (Implementation Plan)

| Bước | Nhiệm vụ cụ thể | Tập tin thao tác |
| :---: | :--- | :--- |
| **Bước 1** | Xây dựng bộ dữ liệu hardcoded chuẩn xác từ các file JSON cào được | `u2/js/data.js` |
| **Bước 2** | Viết file CSS tùy chỉnh: font chữ tiếng Việt, màu sắc thương hiệu, đường kẻ hairline, animation dải tin nóng | `u2/css/custom.css` |
| **Bước 3** | Viết file logic JS chung: đồng hồ thời gian thực, dải tin nóng ticker, search modal, mobile drawer, video player modal | `u2/js/main.js` |
| **Bước 4** | Xây dựng trang chủ `index.html` phong cách The Wired x Truyền Hình Công Thương (Hero 1+4, Trending 01-05, Media Navy Dark, 3 cột chuyên mục) | `u2/index.html` |
| **Bước 5** | Xây dựng trang chi tiết `detail.html` (Reading experience, Drop-cap, Toolbar, Khung bình luận tương tác) | `u2/detail.html` & `u2/js/detail.js` |
| **Bước 6** | Xây dựng trang chuyên mục `category.html` & trang video `video.html` | `u2/category.html`, `u2/video.html` |
| **Bước 7** | Kiểm tra tương thích 100% Mobile/Desktop và hoàn tất tài liệu hướng dẫn đẩy Git | `u2/README.md` |
