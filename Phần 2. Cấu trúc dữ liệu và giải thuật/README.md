#  1. CÁC BƯỚC CƠ BẢN KHI TIẾN HÀNH GIẢI CÁC BÀI TOÁN TIN HỌC
Thức dậy lúc 7h sáng, Sanji bắt đầu công việc nấu ăn thường nhật của mình. Vừa vào bếp, nhìn thấy bãi chiến trường lộn xộn, Sanji biết ngay tối qua Luffy và Usopp đã xỉn quắc cần câu và lục tung tủ lạnh của băng. Sanji cay lắm: "Ta thề là sẽ phải ném thằng thuyền trưởng xuống biển và bẻ mũi thằng Usopp cho chúng nó không bao giờ quậy mới được".

<img width="928" alt="sanji" src="https://github.com/user-attachments/assets/17210a8f-ca30-45d5-b757-a6cf18179303" />


Nói rồi, Sanji vừa dọn vừa chửi. Đồng thời cũng chọn ra những **nguyên liệu** cần thiết để nấu món **bún đậu mắm tôm** chuẩn vị Hà Nội cho cả băng (tất nhiên là trừ 2 thằng phá hoại trên). Chỉ riêng việc chọn nguyên liệu cũng mất tới **30 phút**. _"Giá mà không có 2 đứa phá hoại kia thì ta đã chuẩn bị xong nguyên liệu trong 5 phút rồi"_.

Flashback về 1 năm trước, khi mà Sanji còn chưa gia nhập băng. Luffy khi đó cũng rất thèm bún đậu mắm tôm, và nó đã tự tay mình nấu cho Zoro lẫn Usopp ăn. Kết quả là cả bọn bị tiêu chảy 3 ngày 3 đêm. Vì vậy mới cần biết rằng, vài trò của đầu bếp và **nấu đúng công thức** là quan trọng như thế nào.

Sau khi hoàn thành món bún đậu và bát chấm mắm tôm ngon nhức nách, Sanji cầm đũa lên và **ăn thử** một miếng để đảm bảo mọi thí ngon lành cành đào. _"Chà, cũng được đấy! Nhất định Nami-swan và Robin-chwan sẽ thích lắm đây"_. Dọn dẹp bát đũa xong xuôi mọi thứ và anh chàng hắc cước lãng tử của chúng ta gọi cả băng lên thuyền ăn sáng.

![Bún đậu mắm tôm](https://github.com/user-attachments/assets/e851fa87-f47c-489d-baa1-958ab7f40345)


Các bài toán trong Tin học cũng y như câu chuyện nấu bữa sáng của Sanji vậy: `INPUT --> Xử lý --> OUTPUT`. 
- **Input** là nguyên liệu (thịt heo, bún, mắm tôm, đậu hũ...).
- **Output** là món bún đậu mắm tôm.
- Luffy và Sanji có thể coi như là một **developer** (đầu bếp). Chỉ khác một cái là thành quả của Sanji thì ai cũng khen, còn của Luffy thì cả băng sẽ lao vào đấm.
- Việc sắp xếp ngăn nắp nguyên liệu trong tủ lạnh hay vứt bừa bãi trong bếp chính là **Cấu trúc dữ liệu (data structure)**. CTDL tốt sẽ giúp cho máy tính xử lý bài toán một cách nhanh chóng; trái lại, CTDL không tốt sẽ làm chương trình tốn rất nhiều thời gian.
- Việc nấu đúng công thức chính là **Giải thuật (hay thuật toán)**. Nấu đúng cách thì ngon, nấu sai cách thì có khi còn bị tiêu chảy.
- Bước cuối cùng là nếm thử để chắc chắn món ăn ngon lành, nước chấm không quá mặn, vừa đủ ngọt và chua cũng chính là bước **Kiểm thử**, đảm bảo chương trình hoạt động chính xác.

_Hồ Chí Minh, 26/4/2025_

# 2. PHÂN TÍCH THỜI GIAN THỰC HIỆN GIẢI THUẬT
## 2.1 Tại sao phải quan tâm thời gian chạy?

Bạn đã từng bao giờ đi ăn gà rán KFC chưa? Những miếng gà của họ có hương vị thơm ngon tuyệt vời, mọng nước bên trong và giòn rụm bên ngoài. Những miếng gà được tạo ra bằng cách chiên ngập trong dầu. Mình có một bài toán thế này:

> Giả sử bỏ qua hương vị của gà rán, bạn là quản lý của một cửa hàng KFC đang phục vụ hàng trăm thực khách mỗi ngày. Có 2 công thức chiên gà: một là chiên trong nồi áp suất, hai là chiên trên chảo như bình thường. Bạn sẽ chọn cách nào?

Được biết, nếu chiên gà trong nồi áp suất thì thời gian ra lò sẽ là **8-14 phút**, trong khi chiên bình thường sẽ là **20-30 phút**. Bạn có nghĩ thực khách sẽ đợi được 20 phút chỉ để ăn được món gà được coi là "đồ ăn nhanh" này không? Và cửa hàng của bạn sẽ tốn bao nhiêu tiền, mất bao nhiêu khách hàng nếu chiên trong thời gian lâu như vậy?

Thuật toán trong lập trình cũng giống như cách mà bạn chiên gà vậy. Chọn công thức hiệu quả sẽ giúp máy tính hoàn thành công việc nhanh hơn, tối ưu chi phí, tăng trải nghiệm người dùng, bla bla...

![gà rán kfc](https://github.com/user-attachments/assets/c3c4251f-bda2-44bd-b084-1c417d8e922d)

## 2.2. Làm sao để so sánh công bằng?

Thật ra, thời gian thực thi chạy của chương trình còn phụ thuộc vào nhiều yếu tố như là sức mạnh CPU (VD: Intel Core i3 2010 vs Apple M4 2024), ngôn ngữ lập trình và trình biên dịch compiler (VD: Python vs C++). Cũng giống nhau nấu bếp củi phải tốn thời gian nhóm bếp nếu so với bếp ga vậy.

Vì vậy, người ta tạo ra một lý thuyết chung để đánh giá tốc độ của một thuật toán, gọi là **Big O notation**.

## 2.3. Big O notation

Quay trở lại với những miếng gà, để phục vụ cho `n=100` đơn hàng:
- Chiên trong nồi áp suất sẽ tốn: **`O(10n)`** = 10 x 100 = 1000 phút.
- Chiên trên chảo thường sẽ tốn:  **`O(20n)`** = 20 x 100 = 2000 phút.

Độ phức tạp thuật toán **Big O** (ký hiệu là **O**) là một cách để miêu tả độ phức tạp của thuật toán khi số lượng đơn hàng/Input **`n`** tăng lên. Big O có thể là về độ phức tạp về thời gian (**time complexity**) hoặc về không gian (**space complexity**).

Big O thường được sử dụng để mô tả hiệu suất trong **trường hợp xấu nhất**, đảm bảo rằng thuật toán sẽ không bao giờ chạy chậm hơn giới hạn đã cho. Ví dụ:
1. `O(1)` - Hằng số: Thời gian không đổi dù `n` là bao nhiêu.
   - Nếm thử: Dù nồi to hay nồi nhỏ, đều chỉ cần nếm thử 1 miếng.
   - Lấy phần tử đầu tiên của array: `arr[0]`.
















