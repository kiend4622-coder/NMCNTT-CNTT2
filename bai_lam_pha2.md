# BÀI LÀM PHA 2 

- **Họ tên:**
- **Lớp:**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "SVT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "FZ",
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": "thuong",
    "ghi_chu": "hỗ trợ xe lăn"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
  }
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b056e8c-d920-83ec-bcd0-2776cd4fdf5f

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Gói vé SVT – Trận bán kết

1. Tiền người lớn

Công thức: Số người lớn × Giá vé SVT

= 5 × 1.200.000

= 6.000.000 đồng

2. Tiền trẻ em
- Trẻ 8 tuổi: 1.200.000 × 70% = 840.000 đồng.
- Trẻ 10 tuổi: 1.200.000 × 70% = 840.000 đồng.
- Trẻ 3 tuổi: Miễn phí = 0 đồng.
Tổng tiền trẻ em:

= 840.000 + 840.000 + 0

= 1.680.000 đồng

3. Tổng tiền vé trước giảm giá

Công thức: Tiền người lớn + Tiền trẻ em

= 6.000.000 + 1.680.000

= 7.680.000 đồng

4. Giảm giá nhóm

Nhóm có 5 người lớn nên được giảm 5%.

Công thức: Tổng tiền vé trước giảm × 5%

= 7.680.000 × 5%

= 384.000 đồng

Tiền vé sau giảm:

= 7.680.000 − 384.000

= 7.296.000 đồng

5. Phụ thu khu ghế ưu tiên

Công thức: Số người chọn ghế ưu tiên × Phụ thu mỗi người

= 1 × 300.000

= 300.000 đồng

6. Tổng tiền cuối cùng

Công thức: Tiền vé sau giảm + Phụ thu

= 7.296.000 + 300.000

= 7.596.000 đồng

Tổng thanh toán
7.596.000 đồng
[RESULT: 7596000 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b056eda-94d0-83ec-b3c5-94c427aa97f9

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
a:

 {
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Hai khán giả bị xếp vào khu không mái che thay vì khán đài có mái như cam kết, ảnh hưởng trong 2 hiệp đầu."
 }

c:

2.000.000 đồng để bù đắp những bất tiện mà Quý khán giả đã gặp phải trong 2 hiệp đầu trận đấu.

Ban tổ chức chân thành xin lỗi Quý khán giả vì sự cố sắp xếp chỗ ngồi không đúng với quyền lợi đã cam kết, đặc biệt trong điều kiện thời tiết mưa gây ảnh hưởng đến trải nghiệm theo dõi trận đấu.

Chúng tôi ghi nhận phản ánh và sẽ rà soát lại quy trình bố trí chỗ ngồi nhằm tránh những sự việc tương tự xảy ra trong các trận đấu tiếp theo.

Rất mong nhận được sự thông cảm của Quý khán giả. Ban tổ chức xin chân thành cảm ơn Quý khán giả đã đồng hành và ủng hộ Cúp Sao Vàng.

Trân trọng,

**Ban tổ chức Cúp Sao Vàng**
```

**Link trò chuyện:** https://chatgpt.com/share/6b057030-a024-83ec-b6df-61056db488d9

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---|---|---|
| Đúng thông tin | 0/5 | Giá vé ghi 1.000.000đ, sai so với giá chuẩn 1.200.000đ. Chính sách huỷ trước 3 ngày ghi hoàn 100%, trong khi thực tế chỉ hoàn 50%. | Sửa thành: Vé SVT giá 1.200.000 đồng/người lớn. Huỷ trước 3 ngày được hoàn 50%. |
| Đầy đủ | 1/3 | Đã trả lời hai câu hỏi nhưng chưa mời khách cung cấp ngày trận đấu và số lượng vé để đặt. | Bổ sung: Anh vui lòng cung cấp ngày trận đấu và số lượng vé cần đặt để bên em hỗ trợ ạ! |
| Giọng điệu | 1/2 | Các cụm “xem rất đã luôn” và “cứ nhắn em nhé” chưa đủ chuyên nghiệp. | Sử dụng lời văn lịch sự, chuyên nghiệp và trang trọng hơn. |
| **Tổng điểm** | **2/10** | **Bài mắc lỗi về giá vé, chính sách huỷ và chưa đầy đủ yêu cầu tư vấn.** | **Cần chỉnh sửa theo thông tin chuẩn của Ban tổ chức.** |
```

**Link trò chuyện:** https://chatgpt.com/share/6b057153-cccc-83ec-9648-b2b80acef73f

