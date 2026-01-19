# Deep Learning – Tuần 2: NumPy, Pandas, Matplotlib

## 1. Công nghệ sử dụng
- **Python**
- **NumPy**: xử lý mảng, ma trận và dữ liệu số
- **Matplotlib** (giới thiệu): dùng để trực quan hóa dữ liệu
- **Terminal / VS Code**: chạy và kiểm tra chương trình

## 2. Cách hoạt động

### Bài 1: Tic-Tac-Toe với NumPy
- Sử dụng NumPy để khởi tạo bàn cờ 3x3 dưới dạng ma trận.
- Giá trị `99` đại diện cho ô trống, `1` là X và `0` là O.
- Người chơi nhập vị trí hàng và cột để đánh dấu.
- Chương trình kiểm tra điều kiện thắng theo hàng, cột và đường chéo.
- Trò chơi kết thúc khi có người chiến thắng.

### Bài 2: Trích xuất phần tử trong ma trận
- Khởi tạo ma trận 3x3 bằng NumPy.
- Sử dụng slicing và indexing để lấy:
  - Một hàng
  - Một cột
  - Các phần tử riêng lẻ
  - Các phần tử theo thứ tự đảo ngược

### Bài 3: Lọc số chẵn
- Duyệt danh sách số bằng vòng lặp `for`.
- Lọc các số chẵn bằng điều kiện `i % 2 == 0`.
- Thực hiện lại bài toán bằng **list comprehension** để code ngắn gọn hơn.

### Bài 4: Tách tập dữ liệu
- Tạo dữ liệu ngẫu nhiên kích thước `150 x 5`.
- Tách dữ liệu thành:
  - `X`: 4 cột đầu
  - `Y`: cột cuối
- Chia dữ liệu thành tập train (70%) và test (30%).
- Tách `X_train` thành 10 phần nhỏ bằng `array_split`.

## 3. Kết quả
- Hiểu cách sử dụng NumPy để thao tác với mảng và ma trận.
- Thực hành slicing, indexing và xử lý dữ liệu.
- Mô phỏng được trò chơi Tic-Tac-Toe bằng NumPy.
- Biết cách chia dữ liệu phục vụ cho bài toán Machine Learning.
