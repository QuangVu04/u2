# Báo & Truyền Hình Công Thương - Mockup Giao Diện (Phong Cách The Wired)

Dự án giao diện báo chí điện tử cao cấp cho **Truyền Hình Công Thương - Bộ Công Thương**, được thiết kế theo phong cách tạp chí quốc tế **The Wired** (Editorial Magazine Layout):
- **Typography báo chí mạnh mẽ**: Tiêu đề Serif sang trọng (*Merriweather*), nội dung Sans-serif sắc nét (*Inter*).
- **Độ tương phản cao**: Đen tuyền (`#0A0A0A`), Đỏ cờ nhận diện Công Thương (`#C4161C`) và Trắng kem báo chí.
- **Bố cục Wired đặc trưng**: Khối tin đinh *The Big Story*, bảng xếp hạng xu hướng *Trending 01-05*, phân khu video đêm *Media Dark Section*, và khối chuyên mục dứt khoát.
- **Dữ liệu cứng chất lượng cao**: Tuyển chọn tin tức thời sự, kinh tế, năng lượng và video YouTube thực tế.
- **100% Độc lập**: Không cần cài `node_modules`, mở trực tiếp bằng trình duyệt.

---

## 🚀 Cách Xem Trực Tiếp Trên Máy Tính

1. Vào thư mục `u2`.
2. Nhấp đúp chuột vào file `index.html` để mở ngay trên trình duyệt (Chrome, Edge, Firefox, Cốc Cốc).
3. Hoặc mở bằng extension **Live Server** trong VS Code / IDE.

---

## 🌐 Hướng Dẫn Đẩy Lên GitHub Riêng & Chạy GitHub Pages

Thư mục `u2` được thiết kế hoàn toàn độc lập, bạn có thể đẩy lên repository GitHub mới theo các lệnh sau:

### 1. Khởi tạo Git trong thư mục `u2`
Mở Terminal / PowerShell tại thư mục `u2`:
```bash
cd c:\Users\PC\Desktop\truyenhinhcongthuong\u2
git init
git add .
git commit -m "feat: initial commit - mockup truyen hinh cong thuong wired style"
git branch -M main
```

### 2. Kết nối với GitHub Repository của bạn
Tạo một repository mới trên GitHub (ví dụ: `truyenhinhcongthuong-wired-ui`), sau đó chạy:
```bash
git remote add origin https://github.com/<tai-khoan-cua-ban>/<ten-repo>.git
git push -u origin main
```

### 3. Kích hoạt GitHub Pages để xem online miễn phí
1. Trên GitHub repo, vào tab **Settings** > chọn mục **Pages** (ở menu bên trái).
2. Tại phần **Build and deployment > Branch**, chọn branch `main` và thư mục `/ (root)`.
3. Bấm **Save**. 
4. Sau 1 - 2 phút, GitHub sẽ cung cấp đường link website online (ví dụ: `https://<tai-khoan>.github.io/<ten-repo>/`) để bạn gửi cho đối tác hoặc khách hàng xem trực tiếp!
