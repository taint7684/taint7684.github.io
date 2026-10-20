# Portfolio — Nguyen Tan Tai

Trang portfolio tĩnh (HTML + CSS + JS), không cần build. Mở `index.html` bằng Chrome/Edge là xem được.

## Cấu trúc

```
index.html                    Trang chủ: giới thiệu, 3 dự án, cách làm việc, kỹ năng, kinh nghiệm, liên hệ
projects/eudr-coffee.html     Case study EUDR
projects/social-insurance.html  Case study BHXH & TNCN (ẩn danh, không lộ thông tin khách)
projects/hl-oms.html          Case study HL-OMS
assets/style.css              Giao diện — không cần sửa
assets/main.js                Hiệu ứng (menu mobile, sáng/tối, phóng ảnh) — không cần sửa
assets/img/                   Ảnh (.webp)
assets/cv/                    Đặt file CV PDF vào đây
```

## Sửa nội dung

Chỉ sửa chữ giữa các thẻ HTML, giữ nguyên thẻ và `class`. Chỗ hay sửa đều có comment `<!-- EDIT: ... -->`.

| Muốn sửa | Ở đâu |
|---|---|
| Câu giới thiệu, dòng "Open to…" | `index.html`, phần `HERO` |
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

Màu của từng dự án: `theme-green` (EUDR), `theme-blue` (BHXH), `theme-amber` (HL-OMS). Thêm dự án mới thì copy một khối `<article class="project …">`.

## CV

Lưu CV thành `assets/cv/Nguyen-Tan-Tai-CV.pdf`. Đổi tên file thì sửa link nút "Download CV" trong `index.html`.

## Đưa lên mạng (GitHub Pages)

1. Tạo repo mới trên GitHub, ví dụ `taint7684.github.io` (link sẽ là `https://taint7684.github.io/`) hoặc `ba-portfolio`.
2. Push thư mục này lên.
3. Settings → Pages → Source: `Deploy from a branch`, branch `main`, thư mục `/ (root)`.

## Lưu ý BHXH / NDA

Trang `social-insurance.html` không có tên khách, tên sản phẩm, mã nội bộ, ảnh màn hình hay link tài liệu nội bộ. Nếu thêm nội dung thì giữ đúng nguyên tắc đó: chỉ dùng luật công khai và mô tả phương pháp làm việc.
