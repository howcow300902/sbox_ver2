KES SBOX Landing v13 — Netlify form fix

Lỗi cũ:
- JavaScript chặn submit bằng fetch('/') và báo lỗi nếu Netlify trả response không phải 2xx.

Bản v13:
- Dùng native HTML POST của Netlify Forms.
- action="/success.html".
- Có success.html riêng.
- Có hidden detection form để Netlify nhận form chắc hơn lúc deploy.
- Form name giữ nguyên: kes-sbox-registration.
- GTM giữ nguyên.

Deploy:
1. Upload nguyên folder này lên Netlify/GitHub.
2. Sau deploy vào Netlify > Forms để chắc chắn form kes-sbox-registration xuất hiện.
3. Submit test 1 lead.
4. Nếu dùng webhook Sheet/Gmail, tạo Submission notification riêng cho form kes-sbox-registration.
