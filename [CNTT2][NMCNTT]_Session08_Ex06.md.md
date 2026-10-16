##  Sai lầm của Nam
1. **Dùng Word (.docx) cho Git:**  
   - Là Rich Text, chứa nhiều metadata → mỗi thay đổi nhỏ bị coi là thay đổi toàn bộ file → dễ xung đột.  
2. **Dễ hỏng khi mất dữ liệu:**  
   - Chỉ mất 1 byte trong file Word → file có thể hỏng hoàn toàn, không mở được.  

##  Ưu thế của Markdown
- Là **Plain Text**, nhẹ, dễ đọc trực tiếp trên GitHub.  
- Git Diff hiển thị rõ từng dòng thay đổi, dễ merge.  
- Nếu mất dữ liệu, chỉ ảnh hưởng một ký tự, phần còn lại vẫn đọc được.  
- An toàn hơn, dung lượng nhỏ hơn.  

---

#  GreenTech Project

## Giới thiệu
*GreenTech là dự án nghiên cứu ứng dụng IoT và AI để tối ưu hóa năng lượng xanh trong nông nghiệp và đô thị.*

## Mục tiêu
- [x] Tích hợp IoT để giám sát môi trường  
- [x] Ứng dụng AI để dự đoán nhu cầu năng lượng  
- [x] Giảm chi phí và tăng hiệu quả sử dụng năng lượng  

##  So sánh Word vs Markdown
| Tiêu chí              | Word (.docx) | Markdown (.md) |
|-----------------------|--------------|----------------|
| Đọc trực tiếp trên GitHub | x          | v             |
| Hỗ trợ Git Diff       | x          | v             |
| Nguy cơ hỏng file     | Cao          | Thấp           |
| Dung lượng            | Nặng         | Nhẹ            |





