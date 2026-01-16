# README – LAB 1: Thực hành PyTorch cơ bản

## 1. Công nghệ sử dụng

* Ngôn ngữ: Python 3
* Thư viện: PyTorch, NumPy, Pandas, Scikit-learn
* Môi trường chạy: Jupyter Notebook / Google Colab / VS Code

---

## 2. Nội dung bài thực hành

### BT1 – Tính đạo hàm bằng PyTorch

**Mô tả:**
Bài này yêu cầu tính độ dốc (đạo hàm) của hàm số y = 5x^5 + 6x^3 − 3x + 1 tại một điểm x cho trước.

**Cách làm:**

* Khởi tạo biến x là tensor và bật `requires_grad=True`.
* Khai báo hàm y theo công thức đề bài.
* Dùng hàm `backward()` để PyTorch tự động tính đạo hàm.

**Kết quả:**

* Giá trị `x.grad` chính là độ dốc của hàm tại điểm x đã chọn.

---

### BT2 – Gradient Descent cho hàm một biến

**Mô tả:**
Sử dụng Gradient Descent để cập nhật giá trị x cho hàm y = x^3 + 2x^2 + 5x + 1, với x ban đầu bằng 2.

**Cách làm:**

* Khởi tạo x là tensor có `requires_grad=True`.
* Trong mỗi vòng lặp, tính y và gradient dy/dx.
* Cập nhật x theo công thức Gradient Descent với learning rate α = 0.1.
* Lặp lại 50 lần.

**Kết quả:**

* Giá trị x thay đổi dần sau mỗi vòng lặp.
* Gradient được PyTorch tính tự động.

---

### BT3 – Hồi quy tuyến tính với dữ liệu giả lập

**Mô tả:**
Tạo dữ liệu giả lập với x là số giờ học (từ 1 đến 10), y được tính theo công thức y = 3x + 5 + noise.

**Cách làm:**

* Sinh dữ liệu x, y và noise ngẫu nhiên.
* Khởi tạo tham số w và b ngẫu nhiên với `requires_grad=True`.
* Sử dụng hàm mất mát MSE.
* Áp dụng Gradient Descent để cập nhật w và b trong 100 vòng lặp.

**Kết quả:**

* Giá trị loss giảm dần theo số vòng lặp.
* Tham số w và b tiệm cận giá trị mong muốn.

---

### BT4 – So sánh cách tạo tensor từ NumPy

**Mô tả:**
Bài này nhằm phân biệt hai cách chuyển mảng NumPy sang tensor PyTorch.

**Cách làm và kết quả:**

* `torch.from_numpy(arr)`: tensor dùng chung vùng nhớ với NumPy, nên khi mảng NumPy thay đổi thì tensor cũng thay đổi.
* `torch.tensor(arr)`: tạo tensor mới, sao chép dữ liệu nên không bị ảnh hưởng khi NumPy thay đổi.

---

### BT5 – Tạo và reshape tensor

**Mô tả:**
Thực hành tạo các tensor cơ bản và thay đổi hình dạng của tensor.

**Cách làm:**

* Tạo tensor bằng `empty`, `zeros`, `ones`, `rand`.
* Dùng `view` và `view_as` để reshape tensor.

**Kết quả:**

* Tensor được tạo và reshape đúng kích thước theo yêu cầu.


