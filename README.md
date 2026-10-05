KES SBOX Landing v30 — Custom Result Page via Netlify AJAX

Fix chính:
- Không dùng native form redirect nữa, vì Netlify đang đưa user về generic "Thank you!".
- Submit lead bằng AJAX đúng format Netlify:
  POST /
  Content-Type: application/x-www-form-urlencoded
  body: URLSearchParams(FormData)
- Sau khi request hoàn tất, JS chủ động chuyển:
  + Không đạt -> /review/
  + Đạt -> /success/
- Không kiểm tra response.ok, nên generic response/status của Netlify không chặn redirect custom.
- Không hiện alert lỗi cho người dùng.
- Có sendBeacon fallback nếu fetch gặp network error.
- success/index.html và review/index.html vẫn nằm trong package.

Deploy nguyên ROOT_READY.zip lên Netlify.
Sau deploy test bằng tab ẩn danh.
