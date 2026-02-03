# README – LAB3 - Thực hành Pandas

## 1. Công nghệ sử dụng

* Ngôn ngữ: Python 3
* Thư viện:

  * Pandas: xử lý và phân tích dữ liệu dạng bảng
  * NumPy: xử lý mảng và tính toán số học
  * Seaborn: trực quan hóa dữ liệu và dataset mẫu
* Môi trường: Jupyter Notebook

---

## 2. Mục tiêu bài thực hành

* Làm quen với Pandas Series và DataFrame.
* Hiểu cách tạo, truy cập và thao tác dữ liệu với Pandas.
* Thực hành xử lý dữ liệu thực tế từ file CSV.
* Sử dụng các hàm GroupBy, Merge và xử lý dữ liệu thiếu.

---

## 3. Nội dung chính

### 3.1 File LAB3.ipynb - Giới thiệu Pandas cơ bản

**Mô tả:**

* Tạo Pandas Series từ list, NumPy array và dictionary.
* Tìm hiểu về indexing: số nguyên, chữ cái, kết hợp.
* Tạo DataFrame từ nhiều dictionary.
* Thao tác truy cập dữ liệu: slicing, loc, iloc.

**Kết quả:**

* Hiểu sự khác nhau giữa explicit index và implicit index.
* Biết cách tạo và truy cập Series/DataFrame.
* Giải thích được lỗi KeyError khi dùng index âm.

---

### 3.2 File Pandas.ipynb - Thực hành Pandas nâng cao

**Mô tả:**

* Series: tạo, indexing, slicing, masking, fancy indexing.
* DataFrame: tạo từ nhiều nguồn, truy cập cột/hàng, thuộc tính.
* Xử lý dữ liệu thiếu: isnull(), fillna(), dropna().
* GroupBy: nhóm dữ liệu và tính toán thống kê.
* Merge/Join: gộp nhiều DataFrame.

**Kết quả:**

* Thành thạo các thao tác cơ bản với Pandas.
* Biết cách xử lý dữ liệu thiếu.
* Hiểu cách sử dụng GroupBy và Merge.

---

### 3.3 Bài tập 1 - Xử lý file howlongwelive.csv

**Mô tả:**

* Tải file CSV vào DataFrame.
* In 2 dòng đầu/cuối, kích thước, tên cột.
* Xóa cột có nhiều NaN (Hepatitis B, Population).
* Chuyển đổi cột Status sang dạng số.
* Đổi tên cột và tách dữ liệu thành X, y.

**Kết quả:**

* Biết cách đọc và khám phá dữ liệu.
* Xử lý được dữ liệu để chuẩn bị cho mô hình học máy.

---

### 3.4 Bài tập 2 - Xử lý dữ liệu thiếu và GroupBy

**Mô tả:**

* Kiểm tra và thay thế giá trị thiếu bằng mean.
* GroupBy theo Country để tìm quốc gia tuổi thọ cao/thấp nhất.
* GroupBy theo Status để so sánh Developed và Developing.
* Tạo DataFrame mới và merge.

**Kết quả:**

* Biết cách xử lý dữ liệu thiếu.
* Phân tích dữ liệu theo nhóm.
* Gộp nhiều nguồn dữ liệu lại với nhau.

---

## 4. Kết quả đạt được

* Hiểu cách sử dụng Pandas Series và DataFrame.
* Thành thạo các thao tác indexing, slicing, filtering.
* Biết cách xử lý dữ liệu thiếu và dữ liệu không đồng nhất.
* Sử dụng được GroupBy để phân tích dữ liệu theo nhóm.
* Biết cách gộp nhiều DataFrame bằng merge/join.
