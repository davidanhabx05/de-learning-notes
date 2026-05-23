# Basic Linux CLI Notes - Day 1

These are common Linux Terminal commands used daily for navigating and managing files/directories while working with data systems.

## 1. Navigation Commands
* `pwd` (Print Working Directory): Check the current directory you are in.
* `ls`: List files and subdirectories in the current location.
  * `ls -a`: List all files, including hidden files (such as `.git`).
  * `ls -l`: Display detailed information (permissions, size, modification date).
* `cd <directory_name>` (Change Directory): Move to a desired directory.
  * `cd ..`: Go back to the parent directory.
  * `cd ~`: Quickly return to the user's Home directory.

## 2. File & Directory Management Commands
* `mkdir <name>` (Make Directory): Create a new directory.
* `touch <file_name>`: Create a new empty file.
* `rm <file_name>` (Remove): Delete a file.
  * `rm -rf <directory_name>`: Permanently remove a directory (use this command very carefully).
* `cp <source_file> <new_file>` (Copy): Copy a file.
* `mv <old_name> <new_name>` (Move): Rename a file/directory or move it to another location.

---
*Note: Successfully tested and practiced on a local terminal.*


# Ghi nhớ Linux CLI cơ bản - Day 1

Đây là các lệnh Terminal hệ điều hành Linux dùng mỗi ngày để điều hướng và quản lý file/thư mục khi làm việc với hệ thống dữ liệu.

## 1. Nhóm lệnh điều hướng (Navigation)
* `pwd` (Print Working Directory): Kiểm tra xem mình đang đứng ở thư mục nào.
* `ls`: Liệt kê các file và thư mục con ở vị trí hiện tại.
  * `ls -a`: Liệt kê tất cả file, bao gồm cả file ẩn (như file `.git`).
  * `ls -l`: Hiển thị chi tiết (quyền truy cập, kích thước, ngày sửa đổi).
* `cd <tên_thư_mục>` (Change Directory): Di chuyển đến thư mục mong muốn.
  * `cd ..`: Lùi lại một cấp thư mục cha.
  * `cd ~`: Quay nhanh về thư mục Home của người dùng.

## 2. Nhóm lệnh quản lý File & Thư mục
* `mkdir <tên>` (Make Directory): Tạo một thư mục mới.
* `touch <tên_file>`: Tạo một file trống mới.
* `rm <tên_file>` (Remove): Xóa file.
  * `rm -rf <tên_thư_mục>`: Xóa sổ hoàn toàn một thư mục (cực kỳ cẩn thận với lệnh này).
* `cp <file_gốc> <file_mới>` (Copy): Sao chép file.
* `mv <tên_cũ> <tên_mới>` (Move): Đổi tên file/thư mục hoặc di chuyển chúng sang vị trí khác.

---
*Ghi chú: Đã kiểm tra và thực hành thành công trên terminal local.*