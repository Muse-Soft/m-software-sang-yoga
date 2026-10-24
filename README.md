# Sáng Yoga — Trang giới thiệu lớp yoga ngoài trời buổi sáng

Triển khai từ thiết kế đã duyệt (TEC-44, xem `DESIGN.md`).

## Nội dung trang (`index.html`, trang tĩnh, không cần build)

- Header cố định + Hero: 5:30 – 6:30 sáng, Thứ 2 đến Thứ 7
- Lịch học (bảng dọc, một dòng một buổi)
- 2 huấn luyện viên (khung giữ chỗ — tên/tiểu sử chờ PO/BA bổ sung, không tự bịa)
- Học phí: gói tháng (gắn nhãn "Tiết kiệm nhất") + buổi lẻ (mức giá chờ PO/BA bổ sung)
- Form đăng ký tập thử miễn phí: họ tên, số điện thoại, ngày tập thử (Thứ 2 – Thứ 7, mặc định buổi gần nhất), ghi chú sức khỏe
- FAQ: 6 câu hỏi cho người mới (dạng accordion)
- Footer + nút đăng ký nhắc lại

## Form đăng ký hoạt động như thế nào

Trang tĩnh chưa có máy chủ riêng nên đăng ký được **ghi nhận vào localStorage của trình duyệt** (`sang-yoga-registrations`) và hiển thị thông báo xác nhận kèm giờ tập. Khi có kênh tiếp nhận chính thức (máy chủ/form dịch vụ), chỉ cần thay khối lưu trữ trong hàm `submit` — giao diện và các trường giữ nguyên.

## Mở trang

Mở trực tiếp file `index.html`, hoặc chạy máy chủ tĩnh bất kỳ, ví dụ: `python3 -m http.server` trong thư mục này rồi mở `http://localhost:8000`.
