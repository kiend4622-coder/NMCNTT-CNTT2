
# Báo Cáo Phân Tích I/O

* **Input (Văn bản thô):** Chuỗi ký tự chứa cú pháp Markdown (` ``` `, `|`, `- [ ]`, `\`) chưa qua xử lý.
* **Output (Giao diện render chuyên nghiệp):** Văn bản hiển thị trực quan; câu lệnh Terminal và tên biến nổi bật; khối code Python tô màu cú pháp (Syntax Highlighting); Task List và Bảng so sánh lồng trong comment code gọn gàng; ký tự Escape `\` hiển thị đúng nguyên bản.

---

# Hướng Dẫn Cài Đặt Cảm Biến Độ Ẩm Trang Trại Hoa Lan

Tài liệu này cung cấp các bước thiết lập hệ thống giám sát độ ẩm tự động và cấu hình điều khiển máy bơm cho trang trại lan.

---

### 1. Hướng Dẫn Cấu Hình Ban Đầu

Thao tác trên cửa sổ **Terminal**:

1. Di chuyển vào thư mục dự án: `cd /home/pi/orchid_monitoring`
2. Cập nhật các thư viện bổ trợ: `pip install -r requirements.txt`
3. Kiểm tra cổng kết nối cảm biến: `ls /dev/ttyUSB*`

> **Lưu ý nghiệp vụ**: Tên biến chân tín hiệu nhận dữ liệu là `sensor_pin` và ngưỡng độ ẩm tối thiểu là `moisture_threshold`.

---

### 2. Mã Nguồn Python Tích Hợp Bảng So Sánh & Task List

```python
import time

# ==============================================================================
# BẢNG SO SÁNH CÁC LOẠI CẢM BIẾN ĐỘ ẨM
# ------------------------------------------------------------------------------
# | Tiêu chí          | Cảm biến loại cũ (DHT11) | Cảm biến loại mới (SHT30)    |
# | Độ chính xác      | ±5%                      | ±2%                          |
# | Chuẩn giao tiếp   | Digital Single-Bus       | I2C                          |
# | Khả năng chống nước| Kém (Không vỏ bọc)       | Tốt (Vỏ kim loại chống ăn mòn)|
# | Độ bền thực tế    | 3 - 6 tháng              | > 2 năm                      |
# ==============================================================================

# ==============================================================================
# DANH SÁCH KIỂM TRA THIẾT BỊ (TASK LIST)
# ------------------------------------------------------------------------------
# [x] Kiểm tra nguồn điện 12V cấp cho mô-đun máy bơm
# [x] Đã đấu nối chính xác chân tín hiệu `sensor_pin`
# [ ] Kiểm tra khả năng chống nước của đầu đo SHT30 trong đất
# [ ] Chạy thử nghiệm hệ thống tưới tự động liên tục trong 24 giờ
# [ ] Bàn giao tài liệu hướng dẫn vận hành cho chủ trang trại
# ==============================================================================

def read_moisture_sensor(sensor_pin):
    """Đọc giá trị độ ẩm thực tế từ cảm biến SHT30"""
    moisture_level = 42.5  # Giá trị độ ẩm giả lập (%)
    return moisture_level

def control_pump(action):
    """Điều khiển bật / tắt máy bơm tưới"""
    if action == "START":
        print("[ALERT] Độ ẩm thấp! Đang kích hoạt máy bơm tưới lan...")
    elif action == "STOP":
        print("[INFO] Độ ẩm đạt tiêu chuẩn. Đã tắt máy bơm.")

# Cấu hình tham số hệ thống
sensor_pin = 4
moisture_threshold = 50.0  # Ngưỡng độ ẩm tối thiểu (%)

print("=== HỆ THỐNG GIÁM SÁT ĐỘ ẨM BẮT ĐẦU HOẠT ĐỘNG ===")
current_moisture = read_moisture_sensor(sensor_pin)

if current_moisture < moisture_threshold:
    control_pump("START")
else:
    control_pump("STOP")
