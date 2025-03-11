# Website-Event-Dev

# Hướng dẫn làm việc với repository `website-event-dev`


## 1. Clone repository về máy

Nếu bạn chưa có repository trên máy, chạy lệnh sau:
```sh
git clone https://github.com/thinhdinh127/Website-Event-Dev.git
cd website-event-dev
```

## 2. Tạo nhánh riêng để làm việc

Mỗi thành viên cần làm việc trên nhánh riêng, không push trực tiếp lên `main`.

**Tạo nhánh mới:**
```sh
git checkout -b ten-nhanh
```
Ví dụ:
```sh
git checkout -b ThinhDinh
```

**Push nhánh lên GitHub:**
```sh
git push origin ten-nhanh
```

## 3. Cập nhật code mới nhất từ `main`

Trước khi làm việc, hãy luôn cập nhật nhánh của bạn với code mới nhất từ `main`:
```sh
git checkout main
git pull origin main
```
Sau đó, chuyển sang nhánh đang làm việc và merge code mới:
```sh
git checkout ten-nhanh
git merge main
```
Giải quyết xung đột (nếu có), rồi commit lại:
```sh
git commit -am "Fix conflict"
```

## 4. Push code lên GitHub
Sau khi làm xong, đẩy code lên GitHub:
```sh
git push origin ten-nhanh
```

## 5. Tạo Pull Request (PR)

Vào GitHub, vào repository `website-event`, chọn **Pull Requests**, nhấn **New Pull Request**:
- Chọn **base branch** là `main`
- Chọn **compare branch** là `ten-nhanh`
- Nhấn **Create Pull Request**
- Thêm mô tả về thay đổi của bạn và gửi yêu cầu

## 6. Review và Merge Code

- Người quản lý sẽ review code.
- Nếu có yêu cầu sửa, cập nhật code theo phản hồi và push lại.
- Khi được chấp nhận, code sẽ được merge vào `main`.

## 7. Xóa nhánh sau khi merge
Sau khi PR đã được merge, bạn có thể xóa nhánh cũ:
```sh
git branch -d ten-nhanh
git push origin --delete ten-nhanh
```

---
**Lưu ý:**
- Không commit trực tiếp lên `main`.
- Luôn cập nhật code mới nhất từ `main` trước khi làm việc.
- Viết commit message rõ ràng, mô tả cụ thể thay đổi.

Chúc mọi người làm việc hiệu quả! Anh em 10 điểm 🚀
