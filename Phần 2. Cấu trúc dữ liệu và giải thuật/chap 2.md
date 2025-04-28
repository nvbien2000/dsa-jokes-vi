# 2. PHÂN TÍCH THỜI GIAN THỰC HIỆN GIẢI THUẬT
## 2.1 Tại sao phải quan tâm thời gian chạy?

Bạn đã từng bao giờ đi ăn gà rán KFC chưa? Những miếng gà của họ có hương vị thơm ngon tuyệt vời, mọng nước bên trong và giòn rụm bên ngoài. Những miếng gà được tạo ra bằng cách chiên ngập trong dầu. Mình có một bài toán thế này:

> Giả sử bỏ qua hương vị của gà rán, bạn là quản lý của một cửa hàng KFC đang phục vụ hàng trăm thực khách mỗi ngày. Có 2 công thức chiên gà: một là chiên trong nồi áp suất, hai là chiên trên chảo như bình thường. Bạn sẽ chọn cách nào?

Được biết, nếu chiên gà trong nồi áp suất thì thời gian ra lò sẽ là **8-14 phút**, trong khi chiên bình thường sẽ là **20-30 phút**. Bạn có nghĩ thực khách sẽ đợi được 20 phút chỉ để ăn được món gà được coi là "đồ ăn nhanh" này không? Và cửa hàng của bạn sẽ tốn bao nhiêu tiền, mất bao nhiêu khách hàng nếu chiên trong thời gian lâu như vậy?

Thuật toán trong lập trình cũng giống như cách mà bạn chiên gà vậy. Chọn công thức hiệu quả sẽ giúp máy tính hoàn thành công việc nhanh hơn, tối ưu chi phí, tăng trải nghiệm người dùng, bla bla...

![gà rán kfc](https://github.com/user-attachments/assets/c3c4251f-bda2-44bd-b084-1c417d8e922d)

## 2.2. Làm sao để so sánh công bằng?

Khi Ben và Biên phải làm món trứng ốp la đơn giản, chỉ cần đổ dầu vào chảo và đập quả trứng cái bẹp là xong. Vậy liệu 2 người sẽ hoàn thành món ăn trong cùng 1 khoảng thời gian chứ?

Câu trả lời là: Chưa chắc! Nếu Ben được nấu bằng bếp ga và Biên phải nấu bằng bếp củi, thì Biên còn lâu mới xong được tại còn phải nhóm củi nữa.

Giống như bếp ga và bếp củi, thời gian thực thi của chương trình phụ thuộc vào nhiều yếu tố như là sức mạnh CPU, ngôn ngữ lập trình và trình biên dịch compiler. Vì vậy, người ta tạo ra một lý thuyết chung để đánh giá tốc độ của một thuật toán, gọi là **Big O notation**.

<img width="200" alt="bep cui" src="https://github.com/user-attachments/assets/2204732d-79d6-43b4-9663-fe86da3a6e47">
<img width="200" alt="bep ga" src="https://github.com/user-attachments/assets/2d131919-62bf-4d56-9cfa-aa5b292c279d">



## 2.3. Big O notation

Quay trở lại với những miếng gà, để phục vụ cho `n=100` đơn hàng:
- Chiên trong nồi áp suất sẽ tốn: **`O(10n)`** = 10 x 100 = 1000 phút.
- Chiên trên chảo thường sẽ tốn:  **`O(20n)`** = 20 x 100 = 2000 phút.

**Big O** (ký hiệu là **O**) là một cách để miêu tả độ phức tạp của thuật toán khi số lượng đơn hàng/input **`n`** tăng lên. Big O có thể là về độ phức tạp về thời gian (**time complexity**) hoặc về không gian (**space complexity**).

Big O thường được sử dụng để mô tả hiệu suất trong **trường hợp xấu nhất**, đảm bảo rằng thuật toán sẽ không bao giờ chạy chậm hơn giới hạn đã cho. Ví dụ:

1. **O(1)** - hằng số: Thời gian không đổi dù `n` là bao nhiêu. VD:
   - Nếm thử: Dù bạn có nấu nồi súp xương hầm rau củ siêu to khổng lồ, hay nồi rau ngót nhỏ cho 1 người ăn, đều chỉ cần nếm thử 1 miếng.
   - Lấy phần tử đầu tiên của array `arr[0]`.
2. **O(n)** - tuyến tính: Thời gian tỉ lệ với `n`. VD:
   - Rửa `n` cái bát bằng tay.
   - Duyệt qua `n` phần tử trong mảng.
3. **O(n<sup>2</sup>)**, **O(n<sup>3</sup>)** - luỹ thừa: Tăng nhanh theo luỹ thừa của `n`. VD:
   - 2,3 vòng lặp lồng nhau.
4. **O(_log<sub>2</sub>_ n)** - logarit hệ cơ số 2: Tăng rất chậm dù `n` tăng rất nhanh. VD:
   - Tìm kiếm nhị phân.
5. **O(2<sup>n</sup>)** - hàm mũ: Tăng nhanh khủng khiếp, khiến cho bài toán trở nên bất khả thi nếu `n` ngày càng lớn.

## 2.4. Quy tắc ước lượng Big O

**1. Bỏ qua hằng số nhỏ**
- Thằng Ben vì cờ bạc mà phải mang món nợ 1 Trương Mỹ Lan (673.800 tỉ đồng). Nó sẽ phải đi rửa bát thuê mà trả nợ tới hết đời. Giả sử nó có thêm 2 thằng bạn thân nữa là Biên và Bủm, cả 3 đều đi rửa bát thuê để trả nợ giúp nhưng chắc chắn sẽ chẳng xi nhê vào đâu với con số 673.800 tỉ đồng này. 
- Khi `n` rất lớn, các hằng số nhỏ trở nên ít quan trọng, ít ảnh hưởng tới tốc độ thực thi của dự án. Ví dụ, nếu ta ước lượng thuật toán có độ phức tạp **O(3n)** thì có thể rút gọn thành **O(n)**.

**2. Giữ lại hạng tử chi phối**
- Ngoại trừ nợ cờ bạc 670.800 tỉ, Ben còn nợ thêm tiền ăn quỵt quán phở 100K, quán trà sữa 50K và nhiều quán khác. Tuy nhiên, đấy toàn là mấy con số lẻ và chẳng thấm vào đâu so với khoản nợ cờ bạc.
- Khi cộng các độ phức tạp lại, chỉ cần giữ lại hạng tử tăng nhanh nhất (chi phối nhất) khi `n` lớn. Ví dụ:
**O(2<sup>n</sup>) + O(n) + O(_log<sub>2</sub>_ n)** ==> Giữ lại hạng tử chi phối, rút gọn lại thành **O(2<sup>n</sup>)**.

**3. Quy tắc nhân**
- Quy tắc này thường áp dụng cho vòng lặp. Ví dụ, một vòng lặp `for i:=1 to n do` chỉ thực hiện 2 phép gán đơn giản, thì thời gian thực thi sẽ là **O(n x 2) = O(n)**.
- Một ví dụ khác, nếu 2 vòng lặp lồng nhau như thế này:
```
for i := 1 to n do
   for j := 1 to n do
      <phép gán 1>
      <phép gán 2>
```

Thì độ phức tạp của nó sẽ là **O(n x n x 2) = O(n<sup>2</sup>)**.

## Tóm lại
**Big O** và các quy tắc phân tích thời gian giúp chúng ta có một "ngôn ngữ chung" để đánh giá xem một thuật toán có hiệu quả hay không. Nó tập trung vào xu hướng thời gian tăng lên khi khối lượng công việc lớn dần (input lớn dần), giúp ta chọn được cách làm tốt nhất cho những bài toán lớn.

_Hồ Chí Minh, CN/T2 ngày 27-28/4/2025_
