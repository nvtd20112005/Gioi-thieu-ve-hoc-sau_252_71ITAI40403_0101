# README – LAB 1: Làm quen PyTorch và Autograd

## 1. Công nghệ sử dụng

* Python 3
* PyTorch
* NumPy
* Pandas
* Scikit-learn
* Matplotlib (chỉ dùng khi cần trực quan hóa)

---

## 2. Nội dung và cách hoạt động từng bài

### BT1 – Tính độ dốc (đạo hàm) của đa thức

**Mô tả:**
Cho hàm số y = 5x^5 + 6x^3 − 3x + 1. Sử dụng PyTorch để tính đạo hàm tại một điểm x cụ thể.

**Cách hoạt động:**

* Khởi tạo tensor x với `requires_grad=True`.
* Định nghĩa hàm y theo công thức đề bài.
* Gọi `backward()` để PyTorch tự động tính dy/dx.

**Kết quả:**

* Giá trị `x.grad` chính là độ dốc của hàm tại điểm x đã chọn.

---

### BT2 – Gradient Descent cho hàm một biến

**Mô tả:**
Cho hàm y = x^3 + 2x^2 + 5x + 1. Khởi tạo x = 2 và cập nhật x bằng Gradient Descent.

**Cách hoạt động:**

* Khởi tạo x là tensor có `requires_grad=True`.
* Mỗi vòng lặp:

  * Tính giá trị y.
  * Gọi `backward()` để tính gradient dy/dx.
  * Cập nhật x theo công thức Gradient Descent.
  * Reset gradient sau mỗi vòng.

**Kết quả:**

* Giá trị x thay đổi dần qua 50 vòng lặp.
* Gradient dy/dx được PyTorch tự động tính.

---

### BT3 – Hồi quy tuyến tính với dữ liệu giả lập

**Mô tả:**
Tạo dữ liệu giả lập với x là số giờ học (1–10) và y = 3x + 5 + noise. Huấn luyện mô hình y = wx + b.

**Cách hoạt động:**

* Sinh dữ liệu x, y và noise ngẫu nhiên.
* Khởi tạo w và b với `requires_grad=True`.
* Dùng hàm mất mát MSE.
* Áp dụng Gradient Descent để cập nhật w và b trong 100 vòng lặp.

**Kết quả:**

* Loss giảm dần theo số vòng lặp.
* Giá trị w xấp xỉ 3 và b xấp xỉ 5.

---

### BT4 – So sánh `torch.from_numpy` và `torch.tensor`

**Mô tả:**
Giải thích sự khác nhau khi tạo tensor từ NumPy.

**Cách hoạt động:**

* `torch.from_numpy(arr)` dùng chung vùng nhớ với NumPy.
* `torch.tensor(arr)` tạo bản sao dữ liệu mới.

**Kết quả:**

* Thay đổi NumPy array sẽ làm tensor thay đổi ở trường hợp `from_numpy`.
* Tensor không thay đổi khi dùng `torch.tensor`.

---

### BT5 – Tạo và reshape tensor

**Mô tả:**
Tạo các tensor cơ bản và thay đổi shape.

**Cách hoạt động:**

* Sử dụng `empty`, `zeros`, `ones`, `rand` để tạo tensor.
* Dùng `view` và `view_as` để reshape tensor.

**Kết quả:**

* Tensor được tạo đúng kích thước.
* Reshape không làm thay đổi dữ liệu bên trong.

---

## 3. Giao diện web

* Không yêu cầu giao diện web cho Lab 1.

---

## 4. Kết luận

Lab 1 giúp làm quen với PyTorch, cơ chế autograd, cách tính gradient và áp dụng Gradient Descent cho các bài toán cơ bản.
