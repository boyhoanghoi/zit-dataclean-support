# Dùng thử Zit DataClean

1. Mở `ZitDataClean.exe` trong thư mục bản portable. Không cần cài Python.
2. Bấm **Thử dữ liệu mẫu** hoặc kéo file CSV/XLSX vào cửa sổ.
3. Chọn các trang tính muốn gộp ở danh sách bên trái.
4. Chọn quy tắc bên phải. Bấm **Khóa so trùng** để chọn cột ID/email thay vì so toàn bộ dòng.
5. Bấm **Áp dụng quy tắc**. So sánh tab Dữ liệu gốc / Xem trước và các số đếm.
6. Bấm **Xuất file kết quả**, chọn tên file mới với đuôi `.xlsx` hoặc `.csv`.
7. Bấm **Lưu cấu hình** để lưu các quy tắc thành JSON. Mở cấu hình đó khi xử lý đợt báo cáo tiếp theo.

File CSV cần chọn đúng bảng mã/dấu phân cách trước khi nhập nếu nhận diện tự động
không đúng. Mặc định hỗ trợ UTF-8/UTF-16 có BOM; các bảng mã khác phải chọn rõ ràng.
Thay đổi thiết lập nhập chỉ áp dụng cho file nhập sau đó; xóa danh sách để nhập lại.

Giới hạn: Windows x64, Windows 10 build 19041 trở lên hoặc Windows 11; tối đa 30
file / 50 MB mỗi file, 250.000 dòng / 3 triệu ô trong không gian làm việc, 1.000 cột.
Bản xem trước và tìm kiếm hiển thị tối đa 5.000 dòng đầu; file xuất gồm toàn bộ kết quả.

XLSX xuất ra giữ dữ liệu dạng văn bản để bảo toàn số 0 đầu mã và tránh chạy công thức.
Đây là công cụ xử lý bảng, không phải ứng dụng giữ nguyên định dạng Excel: không giữ
màu sắc, biểu đồ, macro, kiểu số hay công thức tính toán. Công thức được nhập dạng
chuỗi. Khi cần tính toán số sau khi xuất, hãy chuyển các cột phù hợp sang Number trong Excel.

CSV mặc định thêm dấu nháy trước ô giống công thức để hạn chế Excel thực thi chúng.
Điều này cũng áp dụng cho số âm được lưu dưới dạng chuỗi. Muốn giữ nguyên chuỗi
CSV cho hệ thống máy, có thể bỏ chọn Bảo vệ công thức, sau khi đã kiểm tra nguồn.

Không ghi đè file đầu vào. Đọc bản xem trước trước khi xuất dữ liệu quan trọng.
Ứng dụng không tải dữ liệu lên Internet và không lưu bảng giữa các phiên làm việc.

Gói MSIX chưa ký dành cho bước upload Partner Center. Không coi đây là bộ cài
đã được Microsoft xác nhận. Bản portable chưa ký có thể xuất hiện cảnh báo của Windows.
Microsoft Store sẽ ký gói sau khi duyệt; không cần tắt bảo vệ của Windows.
