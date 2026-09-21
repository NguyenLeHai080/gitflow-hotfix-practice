# Gitflow & Hotfix Practice Repository

Dự án mẫu thực hành quy trình làm việc chuẩn với Gitflow và xử lý Hotfix.

## 🌿 Cấu trúc nhánh (Branch Structure)

1. **`prod`**:
   - Môi trường Production thực tế.
   - Luôn ở trạng thái ổn định và sẵn sàng phục vụ người dùng.
   - Được bảo vệ bởi Branch Protection (bắt buộc thông qua Pull Request, không commit/push trực tiếp).
2. **`staging`**:
   - Môi trường tiền triển khai (Pre-production / UAT).
   - Kiểm thử tính năng trước khi đưa lên `prod`.
   - Được bảo vệ bởi Branch Protection.
3. **`dev`**:
   - Môi trường tích hợp phát triển (Development).
   - Tiếp nhận các tính năng (`feat/*`) từ các lập trình viên.
4. **`feat/<feature-name>`**:
   - Nhánh phát triển tính năng, tạo ra từ `dev`, merge lại vào `dev` qua Pull Request sau khi review.
5. **`hotfix/<hotfix-name>`**:
   - Nhánh sửa lỗi khẩn cấp cho production, tạo ra trực tiếp từ `prod`.
   - Merge vào `prod` qua PR.
   - Đồng bộ ngược về `staging` và `dev`.

## 📜 Chuẩn Commit Message (Conventional Commits)
- `feat: <nội dung tính năng> #<issue_id>`
- `fix: <nội dung sửa lỗi> #<issue_id>`
- `hotfix: <nội dung sửa lỗi khẩn cấp> #<issue_id>`
