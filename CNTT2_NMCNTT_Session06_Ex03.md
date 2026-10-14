5. Yêu cầu đầu ra
Phần 1: Phân tích
Vẽ sơ đồ mô tả luồng dữ liệu khi qua Pipeline PowerShell (Đọc tệp ➔ Lọc từ khóa ➔ Đếm kết quả).
Đọc tệp (Get-Content) 
   ➔ Lọc từ khóa (Select-String / Where-Object) 
   ➔ Đếm kết quả (Measure-Object)


Phần 2: Triển khai
Viết câu lệnh nối 3 bước hoàn chỉnh trên PowerShell để trả về con số báo cáo chính xác, xử lý đúng bẫy dữ liệu ở mục 4.

Get-Content .\access.log | Select-String "TIMEOUT" | Where-Object { $_ -notmatch "NOT TIMEOUT" } | Measure-Object | Select-Object -ExpandProperty Count
