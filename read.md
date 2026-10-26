# 📝 NHẬT KÝ THAY ĐỔI DỰ ÁN BIO LINK (CHANGELOG)

Tài liệu ghi chú toàn bộ quá trình cập nhật, nâng cấp giao diện, âm thanh, video, biểu tượng và hệ thống API theo yêu cầu.

---

## 1. 🎬 Thay thế Video Nền (Background Video)
- **Tệp nguồn**: `PinGrab_1792768685884.mp4` (Video mèo ngồi ngắm mưa bên khung cửa sổ nhìn ra vườn hoa cẩm tú cầu xanh mát, phong cách cực chill / lofi aesthetic).
- **Xử lý kỹ thuật**:
  - Chuyển đổi từ HEVC (H.265) sang chuẩn **H.264 (AVC) profile High** (`CRF 18`, 736x414, 25fps) kích hoạt cờ `+faststart` (đưa metadata `moov atom` lên đầu tệp để video phát tức thì mà không cần chờ tải hết).
  - Tên tệp xuất: [`bg.mp4`](file:///D:/Nguyen/Bio/Bio/bg.mp4).
- **Dọn dẹp**: Xóa video cũ và các tệp video tạm.

---

## 2. 🌧️ Tiếng Mưa Nền & Hiệu Ứng Mưa Rơi (Ambient Rain Audio & Visuals)
- **Âm thanh mưa nền (`rain.mp3`)**:
  - Tích hợp tệp âm thanh tiếng mưa rơi êm dịu, nhẹ nhàng gõ tí tách ngoài cửa kính [`rain.mp3`](file:///D:/Nguyen/Bio/Bio/rain.mp3) (90s seamless loop, dung lượng tối ưu 1.4 MB).
  - Tự động phát nhẹ nhàng làm nền phía dưới tiếng nhạc (âm lượng mặc định 25%).
  - Bổ sung nút bấm riêng trên thanh điều khiển nhạc: biểu tượng đám mây mưa `fa-cloud-showers-heavy` (`#rainBtn`) với hiệu ứng phát sáng xanh nước biển, cho phép người dùng bật/tắt tiếng mưa tùy ý.
- **Hiệu ứng hạt mưa rơi trên Canvas (`#particleCanvas`)**:
  - Nâng cấp 38 hạt bụi sao cũ thành các vệt nước mưa trong suốt (`rgba(186, 224, 255, alpha)`) rơi chéo nhẹ nhàng từ trên xuống dưới, tạo chiều sâu 3D chân thực ngay trước mắt người xem.

---

## 3. 🐱 Cập Nhật Biểu Tượng & Ảnh Bìa Khung Cảnh (Aesthetic Icons & Artwork)
- **Favicon & Icon Tab (`icon.png`)**:
  - Xóa bỏ biểu tượng chữ "N" kim loại 3D cũ (vốn thuộc chủ đề cyberpunk).
  - Thay bằng biểu tượng hình tròn trong suốt cao cấp: chú mèo nhị thể ngồi bên ô cửa sổ ngắm mưa và hoa cẩm tú cầu xanh, đồng bộ hoàn hảo với khung cảnh trang web.
- **Ảnh đại diện bài hát (`dislay.png`)**:
  - Thay thế ảnh gif cũ bằng bức tranh bìa đĩa than vintage nghệ thuật: *"Rainy Day Melodies - Lo-fi Cat"* với chú mèo cuộn tròn ngủ êm ái trên chăn len cạnh tách trà nóng bên khung cửa mưa.
- **Văn bản & Tiêu đề**:
  - Tiêu đề tab động: `Bio Link - Nguyen 🌧️🐱🌿`
  - Dòng tiểu sử: `Ngủ ngày mưa 💤 🌧️`
  - Vị trí: `🌧️ New York, USA 🐾`
  - Trạng thái Discord: Tự động hiển thị các thông báo thời tiết êm dịu như `🌿 ONLINE - ENJOYING THE RAIN 🌧️`.

---

## 4. 🎵 Tuyển tập 10 Bài Nhạc US-UK Chill & Trình Phát Nhạc
- Xóa 2 bài hát cũ (`nhac1.mp3`, `nhac2.mp3`).
- Tải về và tích hợp 10 bài nhạc US-UK bản đầy đủ:
  1. **Track 1**: `Rex Orange County - Sunflower` → [`track1_sunflower.mp3`](file:///D:/Nguyen/Bio/Bio/track1_sunflower.mp3) *(Bài mở đầu)*
  2. **Track 2**: `Powfu - death bed (coffee for your head)` → [`track2_death_bed.mp3`](file:///D:/Nguyen/Bio/Bio/track2_death_bed.mp3)
  3. **Track 3**: `Stephen Sanchez - Until I Found You` → [`track3_until_i_found_you.mp3`](file:///D:/Nguyen/Bio/Bio/track3_until_i_found_you.mp3)
  4. **Track 4**: `dhruv - double take` → [`track4_double_take.mp3`](file:///D:/Nguyen/Bio/Bio/track4_double_take.mp3)
  5. **Track 5**: `Jeremy Zucker - comethru` → [`track5_comethru.mp3`](file:///D:/Nguyen/Bio/Bio/track5_comethru.mp3)
  6. **Track 6**: `d4vd - Here With Me` → [`track6_here_with_me.mp3`](file:///D:/Nguyen/Bio/Bio/track6_here_with_me.mp3)
  7. **Track 7**: `Ricky Montgomery - Line Without a Hook` → [`track7_line_without_a_hook.mp3`](file:///D:/Nguyen/Bio/Bio/track7_line_without_a_hook.mp3)
  8. **Track 8**: `Laufey - Falling Behind` → [`track8_falling_behind.mp3`](file:///D:/Nguyen/Bio/Bio/track8_falling_behind.mp3)
  9. **Track 9**: `New West - Those Eyes` → [`track9_those_eyes.mp3`](file:///D:/Nguyen/Bio/Bio/track9_those_eyes.mp3)
  10. **Track 10**: `JVKE - golden hour` → [`track10_golden_hour.mp3`](file:///D:/Nguyen/Bio/Bio/track10_golden_hour.mp3)

---

## 5. 👁️ Nâng cấp API Đếm Lượt Xem Chuẩn Real-time & Mới 100%
- Thay thế API `mileshilliard` cũ bị lỗi 403 bằng **Abacus Cloud**:
  - `https://abacus.jasoncameron.dev/hit/nvkn-real-bio/pageviews`
  - `https://abacus.jasoncameron.dev/get/nvkn-real-bio/pageviews`
- Hỗ trợ chống tăng ảo khi F5 qua `sessionStorage` và lưu đệm qua `localStorage`.

---

## 6. 📂 Danh mục cấu trúc tệp tin hiện tại
```text
D:\Nguyen\Bio\Bio\
├── bg.mp4                     (Video nền mèo ngắm mưa H.264 Web Optimized)
├── dislay.png                 (Bìa album Rainy Day Melodies Lo-fi Cat)
├── icon.png                   (Favicon chú mèo bên cửa sổ mưa trong suốt)
├── index.html                 (Mã nguồn chính tích hợp âm thanh mưa & nhạc)
├── rain.mp3                   (Âm thanh tiếng mưa rơi êm dịu làm nền)
├── read.md                    (Tệp nhật ký thay đổi này)
├── track1_sunflower.mp3       (Rex Orange County - Sunflower)
├── track2_death_bed.mp3       (Powfu - death bed)
├── track3_until_i_found_you.mp3 (Stephen Sanchez - Until I Found You)
├── track4_double_take.mp3     (dhruv - double take)
├── track5_comethru.mp3        (Jeremy Zucker - comethru)
├── track6_here_with_me.mp3    (d4vd - Here With Me)
├── track7_line_without_a_hook.mp3 (Ricky Montgomery - Line Without a Hook)
├── track8_falling_behind.mp3  (Laufey - Falling Behind)
├── track9_those_eyes.mp3      (New West - Those Eyes)
└── track10_golden_hour.mp3    (JVKE - golden hour)
```
