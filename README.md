KES SBOX FINAL REVIEWABLE

Bản này giữ nguyên logic FINAL và thêm 3 field để Trade kiểm tra tay:

- eligibility_result:
  ĐẠT / CHƯA ĐẠT

- eligibility_reason:
  Đủ điều kiện hệ thống
  hoặc
  Loại hình không thuộc nhóm ưu tiên
  hoặc
  Năng lực dưới 200 tấm/tháng
  hoặc
  kết hợp cả 2 lý do

- manual_status:
  mặc định = CHƯA KIỂM TRA

Nhờ vậy khi đổ về Netlify / Google Sheet có thể lọc nhanh:
- Hệ thống tự phân loại trước
- Trade vẫn review thủ công từng lead trước khi cấp SBOX

Logic:
ĐẠT = loại hình ưu tiên VÀ năng lực từ 200 tấm/tháng trở lên
CHƯA ĐẠT = không đạt một trong hai điều kiện trên

Tất cả lead vẫn được đi đến bước nhập địa chỉ.
