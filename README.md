# 💖 I Love You — A Little Love Animation

<p align="center">
  <strong>Một món quà nhỏ bằng HTML, CSS và JavaScript — dành cho một người thật đặc biệt.</strong>
  <br>
  Một trái tim được ghép từ những mảnh nhỏ, khẽ bay lên cùng lời nhắn
  <strong>“I Love You”</strong>.
</p>

<p align="center">
  <img alt="HTML" src="https://img.shields.io/badge/HTML-5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img alt="CSS" src="https://img.shields.io/badge/CSS-3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=222">
  <img alt="Dependencies" src="https://img.shields.io/badge/Dependencies-None-36B37E?style=for-the-badge">
</p>

---

## ✨ Giới thiệu

**I Love You** là một website hoạt ảnh lãng mạn chạy trực tiếp trên trình duyệt. Không framework, không cài thư viện — chỉ cần mở trang web và để những mảnh trái tim lần lượt xuất hiện, kết thành hình rồi bay lên, nhường chỗ cho lời nhắn yêu thương.

Phù hợp để gửi tặng người thương, dùng làm thiệp điện tử hoặc tùy biến thành một món quà trực tuyến của riêng bạn.

## 💝 Có gì trên trang?

| Thành phần | Mô tả |
|---|---|
| ❤️ **Trái tim ghép hình** | JavaScript lần lượt định vị các khối gồm những mảnh hình trái tim, tạo thành một trái tim lớn. |
| 🎈 **Hiệu ứng bay lên** | Sau khi hoàn thiện, trái tim chuyển động lên phía trên màn hình. |
| 💌 **Lời nhắn xuất hiện** | Dòng chữ **“I Love You”** hiện ra với hiệu ứng mờ dần và phóng nhẹ. |
| 🐰 **GIF trang trí** | Hình động `biubiubiu.gif` tạo điểm nhấn bên trái màn hình. |
| 🎵 **Nhạc nền** | Tệp `1.mp3` được phát lặp lại khi trình duyệt cho phép phát tự động. |
| 💫 **Đường viền hoạt ảnh** | Hai đường viền màu đen và đỏ lần lượt chạy ngang ở cuối trang. |
| 🖥️ **Không phụ thuộc framework** | Website tĩnh, không cần cài package hay chạy quy trình build. |

## 🎬 Nhịp điệu hoạt ảnh

1. Trang tải và bắt đầu hoạt ảnh đường viền.
2. Sau khoảng **12 giây**, các mảnh trái tim bắt đầu xuất hiện lần lượt.
3. Mỗi mảnh được thêm cách nhau khoảng **300 ms**, tạo hiệu ứng trái tim đang được lắp ghép.
4. Khi hoàn thành, trái tim bay lên và dòng chữ **“I Love You”** xuất hiện.

Thời điểm phát nhạc phụ thuộc vào chính sách autoplay của trình duyệt và cài đặt âm thanh của thiết bị.

## 📁 Cấu trúc dự án

```text
i-love-you/
├── index.html          # Nội dung và bố cục chính của website
├── css/
│   └── love.css        # Giao diện, hình trái tim và các hiệu ứng CSS
├── js/
│   └── love.js         # Trình tự lắp ghép và chuyển động của trái tim
├── images/
│   ├── biubiubiu.gif   # GIF trang trí
│   └── heart.png       # Hình ảnh dùng cho các mảnh trái tim
└── MP3/
    └── 1.mp3           # Nhạc nền phát lặp
```

## 🚀 Chạy website

### Cách nhanh nhất

Mở tệp `index.html` bằng trình duyệt.

### Chạy bằng máy chủ tĩnh

Nếu trình duyệt hoặc môi trường của bạn hoạt động tốt hơn với một máy chủ cục bộ, hãy mở terminal tại thư mục dự án và chạy một trong các lệnh sau:

**Python**

```bash
python -m http.server 8000
```

Sau đó truy cập [http://localhost:8000](http://localhost:8000).

**Node.js (nếu đã cài `http-server`)**

```bash
npx http-server .
```

> Dự án không có bước build và không yêu cầu cài dependencies để hoạt động.

## 🛠️ Tùy biến thành món quà của bạn

### Đổi lời nhắn

Trong `index.html`, thay nội dung bên trong `.text-love`:

```html
<div class="text-love">I Love You</div>
```

### Đổi nhạc

Thay tệp `MP3/1.mp3` bằng bản nhạc của bạn, hoặc cập nhật đường dẫn trong phần tử `<audio>` của `index.html`. Giữ thuộc tính lặp nếu muốn nhạc phát liên tục.

### Đổi hình trang trí

Thay `images/biubiubiu.gif` bằng hình GIF khác và cập nhật đường dẫn tương ứng trong `index.html`. Để đổi hình trái tim, thay `images/heart.png`; CSS đang tham chiếu đến hình này trong `css/love.css`.

### Điều chỉnh thời gian và chuyển động

Trong `js/love.js`, thời gian chờ trước khi ghép trái tim và khoảng nghỉ giữa các mảnh được điều khiển bởi các giá trị `12000` và `300`. Trong `css/love.css`, có thể tùy chỉnh kiểu chữ, màu sắc và thời lượng hiệu ứng hiển thị lời nhắn.

## 📱 Trình duyệt và lưu ý

- Hoạt động trên trình duyệt hiện đại có hỗ trợ HTML, CSS và JavaScript.
- **Âm thanh có thể không tự phát:** nhiều trình duyệt chặn autoplay có âm thanh cho đến khi người dùng tương tác với trang. Hãy bấm hoặc chạm vào trang rồi thử lại nếu chưa nghe thấy nhạc.
- Trang hiện dùng bố cục kích thước cố định cho hiệu ứng trái tim; trải nghiệm có thể khác nhau trên màn hình nhỏ.
- Biểu tượng favicon hiện được tải từ một URL bên ngoài, vì vậy có thể không hiển thị khi ngoại tuyến.

## 🧰 Công nghệ

- **HTML5** — nội dung trang và âm thanh.
- **CSS3** — bố cục, hình trái tim, hoạt ảnh đường viền và hiệu ứng lời nhắn.
- **Vanilla JavaScript** — dựng trái tim theo từng khối và điều khiển trình tự hoạt ảnh.

---

<p align="center">
  Đôi khi, một trái tim nhỏ cũng đủ để nói điều lớn lao. 💗
</p>
