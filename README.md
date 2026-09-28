# 🐟 AndyLe Pool

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
![Three.js](https://img.shields.io/badge/Three.js-r170-black)
![WebGL](https://img.shields.io/badge/WebGL-3D-green)
![HTML5](https://img.shields.io/badge/HTML5-CSS%20%2B%20JavaScript-orange)

**AndyLe Pool** là một hồ cá Koi 3D tương tác chạy trực tiếp trên trình duyệt.  
Ứng dụng mô phỏng mặt nước, cá Koi, thời tiết, mùa trong năm, ánh sáng và nhạc nền theo từng khung cảnh.

![AndyLe Pool](screenshot.jpg)

---

## ✨ Tính năng chính

- Hồ cá Koi 3D tương tác bằng **Three.js / WebGL**.
- Chạm hoặc click mặt nước để **thả thức ăn cho cá**.
- Kéo chuột để **xoay góc nhìn**.
- Cuộn chuột hoặc chụm hai ngón để **phóng to / thu nhỏ**.
- Nút **Xua cá** tạo phản ứng cho đàn cá.
- Hiệu ứng mặt nước, gợn sóng, phản xạ và khúc xạ.
- Hiệu ứng ánh sáng thay đổi theo từng cảnh.
- Hỗ trợ nhiều trạng thái thời tiết và mùa.
- Nhạc nền riêng cho từng cảnh.
- Hiệu ứng sấm được tạo trực tiếp bằng Web Audio API.
- Giao diện responsive, dùng được trên máy tính và thiết bị di động.
- Không cần framework hoặc bước build riêng.

---

## 🌤 Các khung cảnh

| Phím | Cảnh |
|---|---|
| `1` | ☀️ Nắng đẹp |
| `2` | 🌅 Hoàng hôn |
| `3` | 🌙 Đêm |
| `4` | 🌧 Mưa |
| `5` | ⛈ Sấm sét |
| `6` | 🌸 Mùa xuân |
| `7` | 🌿 Mùa hạ |
| `8` | 🍂 Mùa thu |
| `9` | ❄️ Mùa đông |

---

## 🎮 Điều khiển

| Thao tác | Chức năng |
|---|---|
| Click / chạm mặt nước | Thả thức ăn |
| Kéo chuột / kéo ngón tay | Xoay camera |
| Cuộn chuột / pinch | Zoom |
| `Space` | Xua cá |
| `M` | Bật / tắt nhạc |
| `H` | Ẩn / hiện giao diện |
| `1` → `9` | Chuyển nhanh giữa các cảnh |

---

## 🎵 Thêm nhạc nền

Tạo thư mục:

```text
music/
```

đặt cạnh file `index.html`.

Cấu trúc đề xuất:

```text
AndyLe-Pool/
├── index.html
├── README.md
├── LICENSE
├── screenshot.jpg
└── music/
    ├── sunny.mp3
    ├── sunset.mp3
    ├── night.mp3
    ├── rain.mp3
    ├── storm.mp3
    ├── spring.mp3
    ├── summer.mp3
    ├── autumn.mp3
    ├── winter.mp3
    └── default.mp3
```

Các định dạng âm thanh được hỗ trợ:

```text
.mp3
.m4a
.ogg
.wav
```

Nếu một cảnh không có file nhạc riêng, ứng dụng sẽ thử dùng:

```text
music/default.*
```

Riêng cảnh mùa đông có thể dùng:

```text
winter.*
```

hoặc:

```text
snow.*
```

> **Lưu ý về bản quyền âm thanh:** Apache License 2.0 chỉ áp dụng cho mã nguồn của dự án nếu bạn khai báo như vậy. Các file nhạc, hình ảnh hoặc tài nguyên bên thứ ba không tự động trở thành Apache 2.0. Chỉ đưa lên repository những tài nguyên bạn sở hữu hoặc có quyền phân phối.

---

## 🚀 Chạy ứng dụng

AndyLe Pool là ứng dụng web tĩnh, không cần `npm install`.

### Cách 1 — GitHub Pages

1. Upload toàn bộ project lên GitHub.
2. Vào **Settings** của repository.
3. Chọn **Pages**.
4. Trong **Build and deployment**, chọn:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Bấm **Save**.
6. Chờ GitHub hoàn tất deploy.

Sau đó GitHub sẽ cung cấp URL để chạy app trực tuyến.

### Cách 2 — Chạy local bằng Python

Mở Terminal / CMD tại thư mục project:

```bash
python -m http.server 8000
```

Sau đó mở trình duyệt:

```text
http://localhost:8000
```

Khuyến nghị chạy qua HTTP thay vì mở trực tiếp `index.html` bằng `file://`.

---

## 🧩 Công nghệ sử dụng

- HTML5
- CSS3
- JavaScript ES Modules
- WebGL
- Three.js `0.170.0`
- Three.js `OrbitControls`
- Three.js `BufferGeometryUtils`
- Web Audio API
- Google Fonts

Three.js và Google Fonts hiện được tải từ CDN, vì vậy khi chạy phiên bản hiện tại cần có kết nối Internet để tải các dependency này.

---

## 📁 Cấu trúc repository

```text
.
├── index.html          # Toàn bộ ứng dụng AndyLe Pool
├── screenshot.jpg      # Hình preview dùng trong README
├── README.md           # Tài liệu hướng dẫn
├── LICENSE             # Apache License 2.0
└── music/              # Nhạc nền theo từng cảnh
```

---

## 📜 License

Mã nguồn của **AndyLe Pool** được phát hành theo **Apache License 2.0**.

Apache License 2.0 cho phép người khác:

- sử dụng mã nguồn;
- chỉnh sửa;
- phân phối lại;
- sử dụng cho mục đích thương mại;
- tạo sản phẩm phát triển từ mã nguồn;

với điều kiện họ phải tuân thủ các yêu cầu của Apache License 2.0, bao gồm việc giữ lại thông tin bản quyền và giấy phép liên quan, đồng thời ghi chú các file đã được thay đổi khi phân phối phiên bản sửa đổi.

Xem toàn bộ điều khoản trong file:

```text
LICENSE
```



## © Copyright

```text
Copyright 2026 AndyLeAI
```

Licensed under the Apache License, Version 2.0.

---

## 👤 Author

**AndyLeAI**


