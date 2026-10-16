# Smart-Farm (Lan Farm)

##  Mô tả
*Hệ thống Smart-Farm tích hợp IoT giúp tự động hóa việc tưới tiêu, giám sát nhiệt độ và độ ẩm tại trang trại Lan. Người nông dân có thể quản lý từ xa qua ứng dụng di động.*

---

## Phân tích hệ thống

### Input / Output
- **Input:**
  - Cảm biến nhiệt độ, độ ẩm đất, ánh sáng
  - Lệnh điều khiển từ ứng dụng quản lý
  - Nguồn điện và kết nối mạng IoT
- **Output:**
  - Bật/tắt hệ thống tưới nước tự động
  - Gửi cảnh báo qua điện thoại
  - Lưu nhật ký dữ liệu vào RAM/Cloud

### Sơ đồ phối hợp phần cứng (SoC)
```mermaid
graph TD
A[Cảm biến nhiệt độ/độ ẩm] --> B[CPU SoC ESP32]
B --> C[Wi-Fi Module]
B --> D[Van điện từ tưới]
C --> E[Ứng dụng quản lý trên điện thoại]
Nếu **RAM bị đầy dữ liệu nhật ký**, hãy:

-   Xuất dữ liệu sang Cloud/USB
    
-   Xóa log cũ theo chu kỳ (FIFO)
    
-   Tránh ghi đè trực tiếp để không mất dữ liệu quan trọng
