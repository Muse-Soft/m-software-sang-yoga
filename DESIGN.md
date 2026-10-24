# Thiết kế giao diện — Trang giới thiệu lớp yoga ngoài trời Sáng Yoga

> Mã việc: TEC-44 · Project Linear: m-software-sang-yoga · Epic: TEC-43 ([Epic] Sprint 1 — Trang giới thiệu lớp yoga Sáng Yoga)
> Tài liệu bàn giao cho Dev triển khai. Đây là bản thiết kế (đặc tả giao diện), chưa phải code trang web.

## 1. Nguyên tắc thiết kế

- **Đối tượng chính: người lớn tuổi.** Mọi quyết định dưới đây phục vụ khả năng đọc nhanh, nhìn rõ, bấm dễ.
- **Tông xanh lá nhẹ, nhiều khoảng trắng:** nền sáng, không rườm rà, không chữ chen chúc.
- **Một màn hình, một ý chính:** cuộn dọc theo đúng thứ tự các khối ở mục 3; không dùng tab ẩn nội dung quan trọng.
- **Nút bấm lớn, rõ:** nút kêu gọi hành động (CTA) luôn đủ lớn để bấm bằng ngón tay, có độ tương phản cao.

## 2. Bảng màu và chữ

### Bảng màu (tông xanh lá nhẹ)

| Vai trò | Màu | Mã hex |
|---|---|---|
| Nền chính | Trắng ngà | `#FDFEF9` |
| Nền khối xen kẽ | Xanh lá rất nhạt | `#EAF5EC` |
| Màu chủ đạo (tiêu đề, nút chính) | Xanh lá đậm vừa | `#2E7D4F` |
| Màu nhấn (giá, CTA phụ) | Xanh lá tươi | `#4CAF7A` |
| Chữ chính | Xám đen | `#222222` |
| Chữ phụ | Xám vừa | `#555555` |
| Viền, đường phân cách | Xanh lá nhạt | `#C8E6D0` |

Không dùng nền tối, không dùng chữ màu nhạt trên nền sáng, không dùng quá 2 sắc xanh lá đậm trong cùng một khối.

### Cỡ chữ (lớn, dễ đọc cho người lớn tuổi)

| Thành phần | Cỡ tối thiểu (desktop / mobile) |
|---|---|
| Tiêu đề trang (hero) | 40px / 32px, đậm |
| Tiêu đề mỗi khối | 28px / 24px, đậm, màu `#2E7D4F` |
| Nội dung chính | 18px / 17px, chiều cao dòng 1.6 |
| Giờ học, giá tiền | 22px / 20px, đậm |
| Chữ nhỏ (ghi chú, điều khoản) | Không dưới 15px |
| Nút bấm | Chữ 18px, chiều cao nút tối thiểu 52px, bo tròn 12px |

- Font: sans-serif hệ thống, dễ đọc (ví dụ Inter, Be Vietnam Pro hoặc system-ui). Không dùng font trang trí cho nội dung.
- Khoảng trắng: mỗi khối cách nhau tối thiểu 64px (desktop) / 48px (mobile); lề hai bên tối thiểu 24px trên mobile.

## 3. Bố cục từng khối (theo đúng thứ tự từ trên xuống)

### Khối 1 — Đầu trang (Header, cố định khi cuộn)

- Bên trái: tên "Sáng Yoga" + dòng nhỏ "Yoga ngoài trời buổi sáng".
- Bên phải: menu ngắn gọn — Lịch học · Huấn luyện viên · Học phí · Đăng ký tập thử · Hỏi đáp.
- Nút CTA luôn hiện: "Đăng ký tập thử miễn phí" (màu `#2E7D4F`, chữ trắng).
- Trên mobile menu thu gọn thành một nút bấm lớn, không giấu nút đăng ký.

### Khối 2 — Mở đầu (Hero)

- Tiêu đề lớn: "Sáng Yoga — Yoga ngoài trời buổi sáng".
- Dòng phụ 1–2 câu: tập ngoài trời, nhẹ nhàng, phù hợp người lớn tuổi và người mới bắt đầu.
- Thông tin nổi bật ngay dưới tiêu đề, cỡ chữ lớn: **"5:30 – 6:30 sáng · Thứ 2 đến Thứ 7"**.
- Nút chính: "Đăng ký tập thử miễn phí" → cuộn xuống form ở Khối 6.
- Nút phụ: "Xem lịch học và học phí".
- Hình minh họa: ảnh lớp yoga ngoài trời buổi sáng, tông xanh lá, sáng sủa. Ảnh chỉ mang tính minh họa, không che chữ.

### Khối 3 — Lịch học

- Tiêu đề: "Lịch học".
- Bảng lịch rõ ràng, một dòng một buổi, chữ lớn:

| Ngày | Giờ | Ghi chú |
|---|---|---|
| Thứ 2 – Thứ 7 | 5:30 – 6:30 sáng | Lớp ngoài trời, tập chung |
| Chủ nhật | Nghỉ | — |

- Ghi chú dưới bảng: đến sớm 10 phút khởi động; mưa to hoặc thời tiết xấu sẽ thông báo dời/hoãn buổi tập (kênh thông báo do Dev/PO chốt sau).
- Không dùng lịch dạng lưới tháng — người lớn tuổi đọc bảng dọc dễ hơn.

### Khối 4 — Huấn luyện viên (2 người)

- Tiêu đề: "Huấn luyện viên".
- Hai thẻ ngang nhau, mỗi thẻ gồm: ảnh chân dung, tên, vài dòng giới thiệu ngắn (kinh nghiệm, phong cách dạy nhẹ nhàng, phù hợp người mới/người lớn tuổi).
- **Lưu ý bàn giao:** tên, ảnh và tiểu sử thật của 2 huấn luyện viên chưa có trong mô tả task — Dev dùng khung giữ chỗ dưới đây, PO/BA bổ sung nội dung thật trước khi công bố:

| Thẻ | Nội dung giữ chỗ |
|---|---|
| Huấn luyện viên 1 | [Tên — chờ bổ sung] · [Giới thiệu ngắn — chờ bổ sung] |
| Huấn luyện viên 2 | [Tên — chờ bổ sung] · [Giới thiệu ngắn — chờ bổ sung] |

- Không tự đặt tên hay tiểu sử giả cho huấn luyện viên.

### Khối 5 — Bảng học phí

- Tiêu đề: "Học phí".
- Hai gói đặt cạnh nhau, gói tháng nổi bật hơn:

| Gói | Nội dung hiển thị | Ghi chú |
|---|---|---|
| Theo tháng | Giá tháng — số buổi: tất cả buổi Thứ 2 – Thứ 7 trong tháng | Gói chính, gắn nhãn "Tiết kiệm nhất" |
| Buổi lẻ | Giá 1 buổi — trả theo từng buổi tập | Dành cho người tập không đều |

- **Lưu ý bàn giao:** mức giá cụ thể chưa có trong mô tả task — Dev hiển thị khung giá theo bảng trên, PO/BA điền số tiền thật trước khi công bố. Không tự đặt giá.
- Dưới bảng: dòng ghi chú "Buổi tập thử đầu tiên miễn phí" + nút "Đăng ký tập thử miễn phí".

### Khối 6 — Form đăng ký tập thử miễn phí

- Tiêu đề: "Đăng ký tập thử miễn phí".
- Dòng phụ: "Buổi đầu tiên miễn phí — không cần kinh nghiệm, chỉ cần đến đúng giờ."
- Các trường (tối thiểu, nhãn chữ lớn, ô nhập cao tối thiểu 52px):
  1. Họ và tên (bắt buộc)
  2. Số điện thoại (bắt buộc)
  3. Ngày muốn tập thử (chọn Thứ 2 – Thứ 7, mặc định buổi gần nhất)
  4. Ghi chú sức khỏe / điều cần lưu ý (không bắt buộc, ví dụ đau lưng, huyết áp — để huấn luyện viên chuẩn bị bài phù hợp)
- Nút gửi: "Gửi đăng ký" (lớn, màu `#2E7D4F`).
- Sau khi gửi thành công: thông báo rõ ràng "Đã nhận đăng ký! Sáng Yoga sẽ liên hệ xác nhận qua số điện thoại của bạn." và nhắc lại giờ tập 5:30 – 6:30.
- Xử lý gửi form (lưu dữ liệu ở đâu, gửi thông báo qua kênh nào) do Dev/PO chốt ở task triển khai — bản thiết kế này chỉ quy định giao diện và trường dữ liệu.

### Khối 7 — Hỏi đáp (FAQ)

- Tiêu đề: "Câu hỏi thường gặp".
- Dạng danh sách mở từng câu (accordion), mỗi câu một dòng tiêu đề chữ lớn, bấm để mở đáp án. Các câu hỏi bắt buộc có:
  1. Tôi chưa từng tập yoga, có theo kịp không?
  2. Cần chuẩn bị gì khi đi tập? (trang phục, thảm, nước uống)
  3. Trời mưa thì lớp học thế nào?
  4. Tập thử miễn phí là tập buổi nào, có cần đăng ký trước không?
  5. Học phí tháng và buổi lẻ khác nhau thế nào?
  6. Tôi có vấn đề sức khỏe (đau lưng, huyết áp...) thì tập được không?
- Đáp án viết ngắn, giọng thân thiện, mỗi đáp án tối đa 3 câu. Nội dung đáp án chi tiết do BA/PO duyệt khi triển khai — khung câu hỏi trên là bắt buộc phải có.

### Khối 8 — Chân trang (Footer)

- Tên "Sáng Yoga", giờ tập 5:30 – 6:30 (Thứ 2 – Thứ 7), nút "Đăng ký tập thử miễn phí" nhắc lại một lần cuối.
- Liên hệ: số điện thoại / kênh liên hệ [chờ PO bổ sung — không tự điền].

## 4. Responsive (điện thoại là ưu tiên)

- Mobile (màn hình nhỏ) là trường hợp thiết kế trước: một cột duy nhất, chữ không nhỏ hơn bảng ở mục 2, nút bấm đủ lớn.
- Desktop: nội dung tối đa 1080px, căn giữa; thẻ huấn luyện viên và gói học phí xếp 2 cột.
- Không có nội dung nào chỉ hiện trên desktop mà mất trên mobile.

## 5. Checklist bàn giao cho Dev (Acceptance Criteria đối chiếu)

- [x] Đủ các mục: lịch học, 2 huấn luyện viên, bảng học phí tháng/buổi lẻ, form đăng ký tập thử miễn phí, FAQ.
- [x] Lịch học đúng: 5:30 – 6:30, Thứ 2 đến Thứ 7.
- [x] Tông xanh lá nhẹ, nhiều khoảng trắng (bảng màu mục 2).
- [x] Chữ lớn, dễ đọc cho người lớn tuổi (cỡ chữ tối thiểu mục 2).
- [ ] Nội dung chờ PO/BA bổ sung trước khi công bố: tên + tiểu sử 2 huấn luyện viên, mức học phí, số điện thoại/kênh liên hệ (đã đánh dấu rõ trong tài liệu, không tự bịa).
