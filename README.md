# Báo cáo Bài 3: Cấu hình xác thực SSH và Đẩy dự án lên GitHub

## 1. Mục tiêu
Tạo khóa SSH Ed25519, liên kết repository cục bộ với GitHub qua giao thức SSH, và đẩy mã nguồn lên thành công.

## 2. Quá trình tạo khóa SSH Ed25519
- Sinh cặp khóa bằng thuật toán Ed25519:
  ssh-keygen -t ed25519 -C "tkhuyen1303@gmail.com"
- Khóa được lưu tại: ~/.ssh/id_ed25519 (private) và ~/.ssh/id_ed25519.pub (public).
- Copy nội dung khóa công khai:
  cat ~/.ssh/id_ed25519.pub
- Thêm khóa công khai vào GitHub tại: Settings > SSH and GPG keys > New SSH key.

## 3. Liên kết remote repository (giao thức SSH)
- Nối remote origin bằng URL dạng SSH:
  git remote add origin git@github.com:tranhuyen133/Devops_ss4_ex3.git
- Đẩy mã nguồn lên GitHub:
  git push -u origin main

## 4. Kiểm tra kết quả

Kiểm tra kết nối SSH:
ssh -T git@github.com
Kết quả:
Hi tranhuyen133! You've successfully authenticated, but GitHub does not provide shell access.

Kiểm tra remote URL:
git remote -v
Kết quả:
origin  git@github.com:tranhuyen133/Devops_ss4_ex3.git (fetch)
origin  git@github.com:tranhuyen133/Devops_ss4_ex3.git (push)

## 5. Đường dẫn repository GitHub
https://github.com/tranhuyen133/Devops_ss4_ex3

## Lưu ý bảo mật
Chỉ chia sẻ khóa công khai (id_ed25519.pub). Tuyệt đối không nộp/chia sẻ khóa private (id_ed25519).