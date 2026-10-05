Mục tiêu
Khởi tạo cặp khóa SSH bảo mật phục vụ mục đích xác thực kết nối từ xa.
Cấu hình liên kết an toàn giữa repository cục bộ với máy chủ GitHub.
Đẩy (push) mã nguồn và lịch sử commit thành công lên GitHub bằng giao thức SSH.
Yêu cầu
Bối cảnh: Học viên cần đưa dự án cục bộ lên kho lưu trữ đám mây GitHub để lưu trữ và cộng tác nhóm.
Ràng buộc: Bắt buộc sử dụng giao thức SSH và thuật toán Ed25519 để sinh khóa (không sử dụng giao thức HTTPS để tránh phải nhập password/token thủ công).
Kiểm tra
Lệnh kiểm tra:
Kiểm tra kết nối SSH tới GitHub: