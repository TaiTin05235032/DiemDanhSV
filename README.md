# 🎓 HỆ THỐNG NHẬN DIỆN KHUÔN MẶT

## 📌 Giới thiệu

Đây là ứng dụng nhận diện khuôn mặt được xây dựng bằng Python, sử dụng thư viện xử lý ảnh để phát hiện và nhận dạng khuôn mặt từ camera hoặc ảnh có sẵn.

Hệ thống có thể ứng dụng trong điểm danh, quản lý người dùng hoặc các bài toán liên quan đến nhận dạng.

---

## 🎯 Chức năng

* 📷 Nhận diện khuôn mặt từ webcam
* 🧠 So sánh khuôn mặt với dữ liệu đã lưu
* 👤 Nhận dạng người dùng
* 💾 Lưu trữ dữ liệu khuôn mặt

---
## 📊 Sơ đồ hoạt động hệ thống

![Sơ đồ hệ thống](images/system.png)

### 🔍 Mô tả:
1. Camera thu hình ảnh khuôn mặt  
2. Hệ thống phát hiện khuôn mặt (Face Detection)  
3. Trích xuất đặc trưng (Encoding)  
4. So sánh với dữ liệu đã lưu  
5. Trả về kết quả nhận diện  
## 🛠️ Công nghệ sử dụng

* Python
* OpenCV
* face_recognition
* NumPy

---

## 📁 Cấu trúc project

```
project/
│
├── main.py              # Chương trình chính (nhận diện khuôn mặt)
├── dataset/             # Dữ liệu ảnh khuôn mặt
├── model/               # File dữ liệu đã train (nếu có)
├── requirements.txt     # Thư viện cần cài
└── README.md
```

---

## ⚙️ Cài đặt

### 1. Cài Python

Cài đặt Python phiên bản 3.x

### 2. Cài thư viện

Mở terminal hoặc cmd và chạy:

```
pip install -r requirements.txt
```
## 🧠 Nguyên lý hoạt động

Hệ thống nhận diện khuôn mặt hoạt động theo các bước sau:

### 🔹 1. Phát hiện khuôn mặt (Face Detection)
Sử dụng OpenCV để xác định vị trí khuôn mặt trong khung hình từ camera.

---

### 🔹 2. Trích xuất đặc trưng (Face Encoding)
Thư viện face_recognition chuyển mỗi khuôn mặt thành một vector đặc trưng (128 chiều).

👉 Mỗi khuôn mặt = 1 dãy số đại diện duy nhất

---

### 🔹 3. So sánh khuôn mặt (Face Comparison)
So sánh vector khuôn mặt mới với dữ liệu đã lưu bằng khoảng cách Euclidean:

- Nếu khoảng cách nhỏ → cùng người  
- Nếu khoảng cách lớn → khác người  

---

### 🔹 4. Nhận diện kết quả
Nếu trùng khớp:
- Hiển thị tên người  
Ngược lại:
- Hiển thị "Unknown"  

---

## 📐 Công thức so sánh

Khoảng cách giữa 2 vector:

d = √((x1 - y1)² + (x2 - y2)² + ... + (xn - yn)²)

👉 d càng nhỏ → độ giống càng cao
---

## ▶️ Cách chạy chương trình

Chạy file chính:

```
python main.py
```

Sau khi chạy:

* Camera sẽ bật
* Hệ thống bắt đầu nhận diện khuôn mặt

---

## ⚠️ Lưu ý

* Cần có webcam để sử dụng
* Đảm bảo thư mục `dataset` có ảnh khuôn mặt để nhận diện
* Ánh sáng môi trường ảnh hưởng đến độ chính xác

---

## 📌 Hướng phát triển

* Cải thiện độ chính xác nhận diện
* Thêm giao diện người dùng (GUI/Web)
* Lưu lịch sử nhận diện

---

## 👨‍💻 Tác giả

* Nguyễn Tấn Tài
