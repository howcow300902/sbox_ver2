KES SBOX Landing v28 — REDIRECT REAL FIX

Lỗi tìm thấy:
- Trong v27 thực tế VẪN còn submitToNetlify(), fetch('/') và alert
  "Chưa gửi được thông tin. Vui lòng thử lại."
- Vì vậy browser vẫn chạy AJAX cũ và báo lỗi.

v28 đã:
- Xóa hoàn toàn fetch/AJAX và alert lỗi.
- Hồ sơ chưa đạt -> native POST Netlify -> /review/
- Hồ sơ đạt -> native POST Netlify -> /success/
- Có success/index.html + review/index.html + _redirects.
- VERIFY.txt phải cho:
  contains_fetch: False
  contains_alert_error: False
  contains_submitToNetlify: False

QUAN TRỌNG:
Deploy toàn bộ nội dung của folder này.
Nếu upload ZIP trực tiếp, dùng file ROOT_READY.zip vì index.html nằm ngay root ZIP.
Sau deploy mở tab ẩn danh hoặc hard refresh.
