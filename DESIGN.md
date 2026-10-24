# DESIGN.md — Homestay Nhà Gốm (Hội An)

> Quyết định thiết kế cho website homestay Nhà Gốm: 4 phòng + xưởng gốm nhỏ.
> Mọi quyết định hình ảnh của dự án này phải tuân theo tài liệu này.
> Task gốc: TEC-138 (Epic: TEC-137).

## 1. Phong cách tham chiếu (chỉ một)

**"Homestay phố cổ, tông ấm thủ công"** — không gian nhà phố cổ Hội An:
tường vàng kem, gỗ mộc, gốm nung thủ công, ánh đèn vàng ấm buổi chiều.
Cảm giác cần đạt: ấm, mộc, chậm rãi, gần gũi — như bước vào một xưởng gốm
đang mở cửa đón khách, không phải khách sạn sang trọng lạnh lẽo.

## 2. Bảng màu (mã hex + vai trò từng màu)

| Mã hex | Tên gọi | Vai trò |
|---|---|---|
| `#F5EFE4` | Kem gốm | Màu nền chính toàn trang — nền section, nền thẻ |
| `#33261A` | Nâu đất đậm | Màu chữ chính — tiêu đề, đoạn văn, chữ trên nền kem |
| `#8A5A3B` | Nâu gốm | Màu nhấn chính — nút bấm, link, tiêu đề phụ, giá phòng |
| `#4E5D3A` | Xanh lá | Màu nhấn phụ — nhãn trạng thái, tag tiện ích, điểm nhấn lá cây |
| `#FFFFFF` | Trắng | Nền thẻ nổi trên nền kem (dùng ít, chỉ khi cần tách lớp) |
| `#E4D9C6` | Kem đậm | Viền, đường phân cách, nền section xen kẽ với nền kem gốm |

Quy tắc dùng màu:

- Chữ trên nền kem gốm `#F5EFE4` luôn dùng `#33261A` (tương phản cao, dễ đọc).
- Nút chính: nền `#8A5A3B`, chữ trắng `#FFFFFF`. Nút phụ: viền `#8A5A3B`, chữ `#8A5A3B`, nền trong suốt.
- Xanh lá `#4E5D3A` chỉ dùng cho tag/nhãn và điểm nhấn nhỏ, không dùng làm nền lớn.
- Không dùng thêm màu ngoài bảng trên nếu chưa sửa tài liệu này.

## 3. Font chữ

- **Font tiêu đề: Fraunces** (serif, có chân, nét cong mềm) — dùng cho mọi tiêu đề
  H1/H2/H3, tên phòng, tên section. Cỡ: H1 40–48px, H2 28–32px, H3 20–24px.
- **Font nội dung: Be Vietnam Pro** (sans-serif, hỗ trợ tiếng Việt đầy đủ) — dùng cho
  đoạn văn, mô tả phòng, bảng giá, nút bấm, chú thích. Cỡ: văn bản thường 16px,
  chú thích 14px, nút bấm 16px in đậm vừa (weight 600).
- Nạp cả hai font qua Google Fonts. Không dùng font hệ thống thay thế ngoài
  fallback: Fraunces → Georgia, serif; Be Vietnam Pro → system-ui, sans-serif.

## 4. Quy tắc hình ảnh

- **Ưu tiên bố cục ảnh lớn + khoảng trắng** (sản phẩm visual-first): ảnh là nội dung
  chính, mỗi section tối đa một khối chữ ngắn đi kèm ảnh lớn, không xếp chữ dày đặc.
- **Tỉ lệ khung ảnh:**
  - Ảnh hero trang chủ: 16:9, chiều rộng toàn màn hình.
  - Ảnh phòng (4 phòng): 4:3, ảnh ngang, mỗi phòng tối thiểu 3 ảnh.
  - Ảnh xưởng gốm: 3:2 hoặc 4:3.
  - Ảnh dọc dùng cho story/giới thiệu (nếu có): 4:5, không dùng ảnh dọc cho ảnh phòng.
- **Tông ảnh:** tông ấm, ánh sáng vàng tự nhiên buổi chiều, độ bão hòa vừa phải;
  ảnh phải đồng tông với nhau (không trộn ảnh lạnh xanh dương với ảnh ấm).
  Ảnh mẫu dùng trong bản dựng đầu tiên phải là ảnh chất lượng cao, đúng tỉ lệ
  khung trên, và ghi rõ là ảnh mẫu.
- **Nội dung ảnh:** ưu tiên ảnh thật của không gian (phòng, sân, xưởng gốm,
  chi tiết gốm thủ công); tránh ảnh stock chung chung không liên quan đến gốm
  hoặc phố cổ Hội An.

## 5. Bố cục và thành phần

- Trang chủ theo thứ tự: hero (ảnh 16:9 + tên homestay + nút đặt phòng) →
  giới thiệu ngắn → 4 phòng (thẻ ảnh 4:3) → xưởng gốm → tiện ích → liên hệ.
- Thẻ phòng: ảnh 4:3 ở trên, tên phòng (Fraunces), giá (nâu gốm `#8A5A3B`),
  mô tả ngắn 1–2 câu (Be Vietnam Pro), nút "Xem phòng".
- Khoảng trắng: khoảng cách giữa các section tối thiểu 64px trên desktop,
  40px trên mobile; lề nội dung tối đa 1200px, căn giữa.

## 6. Ghi chú áp dụng

- Tài liệu này chốt theo thông số khách đã duyệt (màu, font, phong cách ở trên).
  Muốn đổi bất kỳ mã màu, font hay phong cách nào thì sửa tài liệu này trước,
  rồi mới sửa code theo.
