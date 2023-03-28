# Tigren_Faq

# Bài toán
Module FAQ đơn giản cho phép khách hàng xem và tạo câu hỏi của mình
Admin có thể thêm xem sửa xóa câu hỏi và câu trả lời
Có thể bật tắt module trong backend
Database chứa một bảng Question với các trường question, author, answer, status, product, position

# Đối tượng sử dụng: 
- Khách hàng 
- Admin

# Phân tích luồng xử lý
## Khách hàng

### Đặt câu hỏi 

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

Sau khi câu hỏi được trả lời, khách hàng sẽ xem được như sau

![image](https://user-images.githubusercontent.com/72716233/227948370-d5c071ea-d631-4645-b002-6408b1770793.png)

## Admin

### Trả lời câu hỏi đã đặt

Admin có thể tìm menu quản lý FAQ và cài đặt FAQ ở thanh menu chính

![image](https://user-images.githubusercontent.com/72716233/227946876-8f43aa10-47c2-4754-b011-92a2af66b52e.png)

Admin sau khi vào quản lý FAQ sẽ thấy danh sách các câu hỏi và câu trả lời của Admin

![image](https://user-images.githubusercontent.com/72716233/227953062-e54acbed-e8a8-474f-8c04-0629037468f2.png)

Admin có thể vào Action edit để trả lời các câu hỏi

![image](https://user-images.githubusercontent.com/72716233/227953195-0cd6c6e1-5e0b-495a-9cf5-ea8c222afff6.png)

![image](https://user-images.githubusercontent.com/72716233/227947352-11686dcd-13a3-449a-9d33-5169a562c376.png)

Admin có thể ghi câu trả lời, thay đổi độ ưu tiên hiển thị cho sản phẩm qua position

Câu hỏi với position cao hơn sẽ hiển thị trước cho khách hàng, câu hỏi có position = 0 là các câu chưa được trả lời và được hiển thị trước cho Admin
Các câu trả lời có position mặc định là 1 nếu chưa được đặt

![image](https://user-images.githubusercontent.com/72716233/227948145-1dce8462-46bc-4158-9c09-b0c579aaaeff.png)

![image](https://user-images.githubusercontent.com/72716233/227948217-b8452a9f-d7aa-41d7-b2c5-c0fb1e09d650.png)

### Thêm câu hỏi và trả lời luôn

Admin có thể thêm câu hỏi và trả lời để giải trình các thắc mắc thường có của khách hàng

![image](https://user-images.githubusercontent.com/72716233/227948617-1313a202-e24a-42a0-a79a-51572970bfe2.png)

![image](https://user-images.githubusercontent.com/72716233/227949089-bc6a6db4-f0a6-470e-87ef-3d66a4921c7f.png)

![image](https://user-images.githubusercontent.com/72716233/227949207-556bce61-9f81-47c7-9f3a-8d1c74fe3947.png)

### Bật tắt module

Admin có thể bật hoặc tắt module ở trong config, nhưng nhớ phải flush cache sau khi config

![image](https://user-images.githubusercontent.com/72716233/227949412-d1234d29-ae1d-449b-a2df-ed7ee49ce36b.png)

![image](https://user-images.githubusercontent.com/72716233/227949678-c5d34bc6-26c7-4372-a803-26ec96e81689.png)

Khách hàng sau khi bật module

![image](https://user-images.githubusercontent.com/72716233/227949947-e05e5db6-40d2-44c9-9fc0-124910d22fa1.png)

Khách hàng sau khi tắt module

![image](https://user-images.githubusercontent.com/72716233/227950072-81a7942f-8721-4e43-9d3c-f40f8b3aa725.png)

# Hướng mở rộng

- Lựa chọn sản phẩm trong box khi Admin tự tạo một FAQ thay vì ghi id sản phẩm
- Mass Action để sửa xóa nhanh hơn
- Validate kỹ hơn
- 






