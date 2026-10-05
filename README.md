KES SBOX Landing v27 — Native Custom Redirect

Fix lỗi alert "Chưa gửi được thông tin":
- Bỏ hoàn toàn AJAX fetch('/') vì Netlify có thể trả status khác 2xx và làm JS báo lỗi.
- Quay lại native HTML POST của Netlify Forms.
- Hồ sơ chưa đạt:
  action = /review/
  -> Netlify lưu lead
  -> redirect custom review/index.html
- Hồ sơ đạt:
  action = /success/
  -> Netlify lưu lead
  -> redirect custom success/index.html

Quan trọng:
Deploy NGUYÊN folder/ZIP gồm:
index.html
success/index.html
review/index.html
_redirects
assets/

Sau deploy nên hard refresh / mở tab ẩn danh để tránh cache bản JS cũ.
