# Tigren_Faq

# Đối tượng sử dụng: 
- Khách hàng 
- Admin

# Phân tích luồng xử lý
## Khách hàng

Khách hàng sẽ thấy tab FAQ ở hàng tab dưới sản phẩm
Khi chưa có câu hỏi, sẽ hiển thị như trên
![image](https://user-images.githubusercontent.com/72716233/227912106-cf591e1d-7089-4b65-baaf-0820011fe2da.png)

Khách hàng có thể thêm câu hỏi bằng cách điền form tên người dùng và câu hỏi
Có validate yêu cầu điền 
Khi điền xong thông tin khách sẽ thấy câu hỏi của mình được hiển thị 
![image](https://user-images.githubusercontent.com/72716233/227912942-f21492a0-eb09-4611-8f90-83010d9a7b60.png)

Câu hỏi được hiển thị sẽ có 
- Question: Câu hỏi
- Author: Tên người hỏi
- Answer: Câu trả lời (chỉ Admin được điền)
- Status: Trạng thái (khi khách hàng tạo sẽ luôn là pending - đang chờ xử lý)

Admin sẽ xem xét và trả lời, khi đó người dùng sẽ thấy câu trả lời và status chuyển thành Answered - Đã trả lời

Khách hàng sẽ thấy các câu hỏi được trả lời ưu tiên sắp xếp ở trên, ở dưới là các câu hỏi đang đợi xử lý

## Admin
