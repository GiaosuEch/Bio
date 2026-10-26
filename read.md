# 📝 NHẬT KÝ THAY ĐỔI DỰ ÁN BIO LINK (CHANGELOG)

Tài liệu ghi chú toàn bộ quá trình cập nhật, nâng cấp giao diện, âm thanh, video và hệ thống API theo yêu cầu.

---

## 1. 🎬 Thay thế Video Nền (Background Video)
- **Tệp nguồn phát hiện**: `PinGrab_1792768685884.mp4` (Video mèo ngồi ngắm mưa bên khung cửa sổ nhìn ra vườn hoa cẩm tú cầu xanh mát, phong cách cực chill / lofi aesthetic).
- **Xử lý kỹ thuật**:
  - Tệp gốc dùng định dạng mã hóa HEVC (H.265) vốn hay gặp lỗi không tương thích hoặc đen màn hình trên các trình duyệt Chrome/Edge không có codec mở rộng của Windows.
  - Đã sử dụng `ffmpeg` chuyển đổi sang chuẩn **H.264 (AVC) profile High** với độ phân giải `736x414`, tỷ lệ khung hình `25fps`, tham số chất lượng `CRF 18` (hình ảnh sắc nét, không suy hao), kích hoạt cờ `+faststart` (đưa metadata `moov atom` lên đầu tệp để video phát tức thì mà không cần chờ tải hết).
  - Tên tệp xuất: [`bg.mp4`](file:///D:/Nguyen/Bio/Bio/bg.mp4).
- **Dọn dẹp**:
  - Đã xóa tệp `bg.mp4` cũ (vũ trụ/cyberpunk).
  - Đã dọn dẹp các tệp `PinGrab_1792768685884.mp4` và tệp tạm trong thư mục dự án.

---

## 2. 🎵 Tuyển tập 10 Bài Nhạc US-UK Chill & Trình Phát Nhạc
- Đã xóa 2 bài hát cũ (`nhac1.mp3`, `nhac2.mp3`).
- Đã tải về và tối ưu 10 bài hát US-UK phong cách Bedroom Pop / Indie Chill / Acoustic cực kỳ hòa hợp với video mưa rơi bên cửa sổ.
- Đã cập nhật tiêu đề hiển thị mặc định trên giao diện HTML từ `Microdose` sang:
  ```html
  <div id="songTitle" class="song-title">Rex Orange County - Sunflower</div>
  ```

### Danh sách 10 bài hát trong Playlist:
1. **Track 1**: `Rex Orange County - Sunflower` → [`track1_sunflower.mp3`](file:///D:/Nguyen/Bio/Bio/track1_sunflower.mp3) *(Bài mở đầu theo yêu cầu)*
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

## 3. 👁️ Nâng cấp API Đếm Lượt Xem Chuẩn Real-time & Mới 100%
- **Vấn đề của API cũ**:
  - Dịch vụ cũ `countapi.mileshilliard.com` đã bị lỗi `HTTP 403 Forbidden` trên server, khiến bộ đếm bị đóng băng tại số mặc định 97.
- **Giải pháp thay thế mới**:
  - Chuyển sang dịch vụ API hiện đại **Abacus Cloud**:
    - **Endpoint tăng lượt xem**: `https://abacus.jasoncameron.dev/hit/nvkn-real-bio/pageviews`
    - **Endpoint lấy lượt xem (không tăng)**: `https://abacus.jasoncameron.dev/get/nvkn-real-bio/pageviews`
  - Hỗ trợ đầy đủ CORS (`Access-Control-Allow-Origin: *`).
  - Dữ liệu trả về JSON định dạng chuẩn: `{"value": N}`.
  - Tích hợp cơ chế thông minh:
    - Sử dụng `sessionStorage ('counted_this_session')` để đảm bảo mỗi phiên truy cập thực sự chỉ tính 1 lần (F5 không bị nhảy ảo số).
    - Lưu giá trị lượt xem vào `localStorage ('nvkn_cached_views')` làm bộ nhớ đệm (cache), đảm bảo nếu mất mạng hoặc mạng chậm thì số hiển thị vẫn luôn mượt mà.
    - Hiệu ứng nhảy số (counting animation) tăng dần mượt mà tạo cảm giác trực quan, sống động.

---

## 4. 📂 Danh mục cấu trúc tệp tin hiện tại
```text
D:\Nguyen\Bio\Bio\
├── bg.mp4                     (Video nền mèo ngắm mưa H.264 Web Optimized)
├── dislay.png                 (Ảnh thumbnail đĩa nhạc)
├── icon.png                   (Favicon trang web)
├── index.html                 (Trang chính đã cập nhật Playlist, Video, API View)
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
