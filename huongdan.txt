# Hướng dẫn Setup Python trên Termux và PC (Bản tối ưu)

## 1. Termux (Android)

### 1.1. Cập nhật hệ thống

```bash
pkg update && pkg upgrade -y
termux-setup-storage
```

### 1.2. Cài Python

```bash
pkg install python -y
python --version
```

### 1.3. (Khuyến nghị) Tạo Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate
```

### 1.4. Cài thư viện và chạy script

```bash
pip install --upgrade pip
pip install -r requirements.txt
python main.py
```

Nếu file chính không phải `main.py`, hãy đổi lại cho đúng.

---

## 2. PC (Windows / macOS / Linux)

### 2.1. Cài Python

Tải Python tại: [https://www.python.org/](https://www.python.org/)

* **Windows:** nhớ tick *"Add Python to PATH"* khi cài.

### 2.2. Kiểm tra cài đặt

```bash
python --version
pip --version
```

(Một số hệ điều hành dùng `python3` thay vì `python`.)

### 2.3. Tạo Virtual Environment

```bash
python -m venv .venv
```

### 2.4. Kích hoạt Virtual Environment

* **Windows:**

```bash
.\.venv\Scripts\activate
```

* **macOS / Linux:**

```bash
source .venv/bin/activate
```

### 2.5. Cài thư viện và chạy script

```bash
pip install --upgrade pip
pip install -r requirements.txt
python main.py
```

---

## Ghi chú

* Hãy luôn tạo virtual environment để tránh lỗi và giữ project sạch.
* Khi chạy trên Termux, nên để project trong thư mục Home hoặc thư mục được cấp quyền sau `termux-setup-storage`.
* Nếu thiếu thư viện build trên Termux, có thể cài thêm:

```bash
pkg install clang make openssl-dev libffi-dev -y
```
