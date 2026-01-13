# README – Bài tập PyTorch (BTVN 1 → BTVN 5)

## 1. Công nghệ sử dụng

- **Ngôn ngữ:** Python 3
- **Thư viện chính:** PyTorch
- **Môi trường làm việc:** VS Code / Jupyter Notebook
- **Kiến thức áp dụng:**
  - Tensor
  - Autograd (tính gradient tự động)
  - Gradient Descent
  - Linear Regression
  - Quản lý bộ nhớ giữa NumPy và PyTorch

---

## 2. Cách hoạt động

### 🔹 BTVN 1: Tính độ dốc của đa thức
- Định nghĩa hàm số bậc 5
- Sử dụng PyTorch/TensorFlow để tính đạo hàm thông qua cơ chế **tự động vi phân**
- Độ dốc được tính tại một giá trị cụ thể của `x`

---

### 🔹 BTVN 2: Gradient & Gradient Descent
- Khởi tạo tensor `x = 2` với `requires_grad = True`
- Tính gradient của hàm số bậc 3
- Áp dụng **Gradient Descent** với learning rate `α = 0.1`
- Cập nhật giá trị `x` trong 10 vòng lặp

---

### 🔹 BTVN 3: Linear Regression với dữ liệu giả lập
- Tạo tập dữ liệu giả lập với:
  - `x`: số giờ học (ngẫu nhiên từ 1 đến 10)
  - `y = 3x + 5 + noise`
- Khởi tạo tham số `w`, `b` ngẫu nhiên
- Tính **MSE loss**
- Dùng Gradient Descent cập nhật `w` và `b`
- Huấn luyện mô hình trong 100 vòng lặp

---

### 🔹 BTVN 4: Chia sẻ bộ nhớ NumPy và PyTorch
- So sánh cách tạo tensor bằng:
  - `torch.from_numpy()`
  - `torch.tensor()`
- Giải thích sự khác nhau về **cơ chế quản lý bộ nhớ**
- Nhận biết trường hợp tensor bị thay đổi khi NumPy array thay đổi

---

### 🔹 BTVN 5: Các cách tạo và reshape tensor
- Tạo tensor bằng:
  - `empty`
  - `zeros`
  - `ones`
  - `random`
- Thay đổi hình dạng tensor bằng:
  - `view()`
  - `view_as()`
- Hiểu cách reshape **không làm thay đổi dữ liệu**

---

## 3. Kết quả

- Hiểu và sử dụng thành thạo **tensor trong PyTorch**
- Biết cách tính gradient bằng **autograd**
- Áp dụng được **Gradient Descent** cho bài toán tối ưu
- Huấn luyện thành công mô hình **Linear Regression**
- Nắm được sự khác nhau giữa **copy dữ liệu và chia sẻ bộ nhớ**
- Biết các cách tạo và reshape tensor thường dùng trong Deep Learning