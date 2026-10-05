KES SBOX Landing v22 — 3-step Screening Form

Logic:
STEP 1 — Thông tin doanh nghiệp
- Họ và tên người liên hệ
- SĐT Zalo
- Email (optional)
- Tên doanh nghiệp / công ty
- Loại hình kinh doanh
- Khu vực

Đạt Step 1 nếu business_type thuộc:
- Kiến trúc sư
- Đơn vị thiết kế
- Đơn vị thiết kế - thi công
- Thương mại

Không đạt:
- Xưởng thi công
- Nhà thầu/đội thi công
=> Vẫn submit record lên Netlify, screening_status = Không đạt điều kiện loại hình kinh doanh
=> Redirect review.html

STEP 2 — Năng lực doanh nghiệp
- Dưới 200 tấm/tháng
- Từ 200 đến dưới 500 tấm/tháng
- Từ 500 tấm/tháng trở lên
- Tình trạng sử dụng KES

Đạt Step 2 khi capacity = Từ 500 tấm/tháng trở lên.
Không đạt => vẫn submit record + redirect review.html.

STEP 3 — Xác nhận nhận SBOX
- Tên người nhận
- SĐT người nhận
- Địa chỉ nhận hàng
- Google Maps URL (optional)
=> submit screening_status = Đủ điều kiện nhận SBOX + redirect success.html

Netlify form name: kes-sbox-registration
