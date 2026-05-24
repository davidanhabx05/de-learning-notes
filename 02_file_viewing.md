# Bí kíp Linux CLI - Xem và Tìm kiếm nội dung File

Trong Data Engineering, chúng ta thường xuyên phải làm việc với các file log hoặc file dữ liệu (CSV, JSON) rất lớn. Việc dùng giao diện chuột để mở file là không khả thi. Dưới đây là các lệnh CLI chuyên dụng:

## 1. Xem toàn bộ nội dung
* **`cat <tên_file>`**: (Concatenate) In toàn bộ nội dung file ra màn hình terminal. 
  * *Lưu ý:* Chỉ nên dùng với file nhỏ (dưới 50 dòng). Nếu dùng với file lớn, terminal sẽ bị trôi tuột đi rất nhanh.
  * *Ví dụ:* `cat config.json`

## 2. Xem một phần nội dung
* **`head -n <số_dòng> <tên_file>`**: In ra các dòng ĐẦU TIÊN của file.
  * *Ví dụ:* `head -n 10 data.csv` (Xem 10 dòng đầu, thường dùng để xem tiêu đề cột của file CSV).
* **`tail -n <số_dòng> <tên_file>`**: In ra các dòng CUỐI CÙNG của file.
  * *Ví dụ:* `tail -n 20 server.log` (Xem 20 lỗi mới nhất).
* **`tail -f <tên_file>`**: (Follow) Đọc file theo thời gian thực. Cứ có dòng log nào mới ghi vào file, nó sẽ hiện ra màn hình ngay lập tức. (Bấm `Ctrl + C` để thoát).

## 3. Chế độ đọc tương tác (Interactive)
* **`less <tên_file>`**: Mở file lớn (hàng triệu dòng) một cách an toàn mà không làm treo RAM. Nó chỉ tải từng trang hiển thị lên màn hình.
  * `Space`: Cuộn xuống 1 trang.
  * `b`: Cuộn ngược lên 1 trang.
  * `Shift + G`: Xuống dòng cuối cùng.
  * `g`: Lên dòng đầu tiên.
  * `/từ_khóa`: Tìm kiếm từ khóa (nhấn `n` để đến kết quả tiếp theo).
  * `q`: Thoát chế độ đọc.

## 4. Tìm kiếm nội dung siêu tốc
* **`grep "từ_khóa" <tên_file>`**: Lọc và in ra tất cả các dòng chứa từ khóa.
  * *Ví dụ:* `grep "ERROR" system.log`
* Các cờ (flags) hữu ích của grep:
  * `grep -i "lỗi"`: Tìm kiếm không phân biệt chữ hoa/thường.
  * `grep -n "Timeout"`: Hiển thị kèm theo số thứ tự của dòng chứa từ khóa.
  * `grep -c "WARN"`: Không in nội dung, chỉ đếm tổng số dòng chứa từ khóa.