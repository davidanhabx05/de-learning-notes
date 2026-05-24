# Bí kíp Linux CLI - Đường ống (Pipe) và Chuyển hướng (Redirection)

Đây là xương sống của tự động hóa trong Linux. Nó cho phép kết hợp các lệnh nhỏ, đơn lẻ thành một luồng xử lý dữ liệu (Data Pipeline) mạnh mẽ.

## 1. Chuyển hướng luồng dữ liệu (Redirection)
Mặc định, kết quả của một lệnh sẽ in ra màn hình (Standard Output - stdout). Redirection giúp bạn "bẻ lái" kết quả đó vào một file.

* **`>` (Ghi đè - Overwrite)**: Đẩy kết quả vào file. Nếu file chưa có thì tạo mới. Nếu file đã có, XÓA SẠCH nội dung cũ và ghi đè lên.
  * *Ví dụ:* `echo "Hello Data" > test.txt`
* **`>>` (Ghi nối - Append)**: Đẩy kết quả vào CUỐI file mà không làm mất dữ liệu cũ.
  * *Ví dụ:* `echo "Dòng số 2" >> test.txt`
* **`<` (Đầu vào - Input)**: Lấy dữ liệu từ một file để đưa cho một lệnh xử lý (ít dùng hơn Pipe).

## 2. Đường ống (Pipe - Ký hiệu `|`)
Thay vì đẩy kết quả vào file, Pipe `|` lấy kết quả đầu ra của lệnh bên TRÁI, làm đầu vào trực tiếp cho lệnh bên PHẢI. Bạn không cần tạo file trung gian.

* **Cú pháp:** `Lệnh_1 | Lệnh_2 | Lệnh_3`

## 3. Các ví dụ thực tế trong Data Engineering
* **Đếm số lượng lỗi trong file log:**
```bash
  grep "ERROR" server.log | wc -l