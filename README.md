# Portfolio — Nguyen Tan Tai

Trang portfolio tĩnh (HTML + CSS + JS), không cần build. Mở `index.html` bằng Chrome/Edge là xem được.

## Cấu trúc

```
index.html                    Trang chủ: giới thiệu, domain, 4 dự án, cách làm việc, kỹ năng, kinh nghiệm, liên hệ
projects/eudr-coffee.html     Case study EUDR
projects/social-insurance.html  Case study BHXH & TNCN (ẩn danh, không lộ thông tin khách)
projects/sim-handbook.html    Sổ tay nghiệp vụ BHXH (tiếng Việt) — đã tắt toàn bộ link xem giao diện FIS
projects/battery-2030.html    Case study Battery 2030 (số 3)
projects/hl-oms.html          Case study HL-OMS (số 4)
assets/style.css              Giao diện — không cần sửa
assets/main.js                Hiệu ứng (menu mobile, sáng/tối, phóng ảnh) — không cần sửa
assets/img/                   Ảnh (.webp)
assets/cv/                    Đặt file CV PDF vào đây
```

## Sửa nội dung

Chỉ sửa chữ giữa các thẻ HTML, giữ nguyên thẻ và `class`. Chỗ hay sửa đều có comment `<!-- EDIT: ... -->`.

| Muốn sửa | Ở đâu |
|---|---|
| Câu giới thiệu | `index.html`, phần `HERO` |
| Hàng domain | `index.html`, khối `class="domains"` — `class="tag core"` là domain chính (tô xanh) |
| 4 con số nổi bật | `index.html`, khối `class="stats"` |
| Thẻ dự án trên trang chủ | `index.html`, các khối `<article class="project …">` |
| Kỹ năng | `index.html`, mỗi kỹ năng là một `<li class="tag">…</li>` |
| Kinh nghiệm | `index.html`, mỗi công ty là một `<li class="job">` |
| Email, GitHub, LinkedIn, số điện thoại | `index.html`, phần `CONTACT` (LinkedIn và SĐT đang bị comment — bỏ `<!--` `-->` để hiện) |
| Nội dung case study | file trong `projects/` |

### Mẫu thường dùng

```html
<!-- thêm một tag kỹ năng -->
<li class="tag">Power BI</li>

<!-- thêm một gạch đầu dòng kinh nghiệm -->
<li>Mô tả việc đã làm, bắt đầu bằng động từ quá khứ.</li>

<!-- thêm ảnh có thể bấm phóng to -->
<figure class="shot">
  <img src="../assets/img/ten-anh.webp" alt="Mô tả ảnh" loading="lazy">
  <figcaption><b>Tiêu đề.</b> Chú thích ngắn.</figcaption>
</figure>
```

Màu của từng dự án: `theme-green` (EUDR), `theme-blue` (BHXH), `theme-violet` (Battery 2030), `theme-amber` (HL-OMS). Số thứ tự case nằm ở `<span class="case-no">`. Ảnh trong thẻ dự án có class `fill` để tràn kín khung. Thêm dự án mới thì copy một khối `<article class="project …">`.

## CV

Lưu CV thành `assets/cv/Nguyen-Tan-Tai-CV.pdf`. Đổi tên file thì sửa link nút "Download CV" trong `index.html`.

## Đưa lên mạng (GitHub Pages)

1. Tạo repo mới trên GitHub, ví dụ `taint7684.github.io` (link sẽ là `https://taint7684.github.io/`) hoặc `ba-portfolio`.
2. Push thư mục này lên.
3. Settings → Pages → Source: `Deploy from a branch`, branch `main`, thư mục `/ (root)`.

## Lưu ý BHXH / NDA

Trang `social-insurance.html` và `sim-handbook.html` không có tên khách, tên sản phẩm, mã nội bộ, ảnh màn hình hay link tài liệu nội bộ. Nếu thêm nội dung thì giữ đúng nguyên tắc đó: chỉ dùng luật công khai và mô tả phương pháp làm việc.

Nếu cập nhật sổ tay từ bản gốc `../so-tay-sim.html`: chép đè vào `projects/sim-handbook.html` rồi nhờ Claude tắt lại link Artifact (`const ART={}`), bỏ mục "Giao diện 38 màn hình" và thêm thanh quay lại case study.
