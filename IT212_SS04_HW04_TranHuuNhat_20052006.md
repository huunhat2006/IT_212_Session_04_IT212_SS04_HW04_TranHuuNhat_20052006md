Đáp án: Phương án B

Đây là lựa chọn tối ưu nhất vì nó áp dụng đúng tinh thần Iterative Prompting (Prompt lặp): không chỉ nói rằng code chậm mà còn chỉ rõ nguyên nhân, mục tiêu tối ưu và các ràng buộc kỹ thuật cần đạt được.

1. Vì sao chọn phương án B?
Nội dung phương án B

"Hàm fib đệ quy trên có độ phức tạp O(2N), gây treo hệ thống khi n = 50. Hãy tối ưu lại hàm này sử dụng kỹ thuật Quy hoạch động (Dynamic Programming - Tabulation hoặc Memoization) để đưa độ phức tạp thời gian về O(N) và độ phức tạp không gian O(1) hoặc O(N). Giữ nguyên kiểu trả về long."

(Lưu ý: Fibonacci đệ quy cổ điển có độ phức tạp xấp xỉ O(2ⁿ), không phải O(2N). Tuy nhiên ý đồ của prompt vẫn là chỉ rõ thuật toán hiện tại quá tốn tài nguyên.)

Đầy đủ các yếu tố quan trọng
Xác định chính xác vấn đề

Prompt nêu rõ:

Hàm hiện tại dùng đệ quy.
Hiệu năng kém.
Khi n = 50 có thể chạy rất chậm.

AI hiểu đây là bài toán tối ưu thuật toán chứ không phải sửa lỗi cú pháp.

Chỉ định kỹ thuật cần sử dụng

Prompt yêu cầu rõ:

Dynamic Programming
- Tabulation
hoặc
- Memoization

Điều này giúp AI không đi chệch hướng sang:

Stream API
Parallel Processing
Các kỹ thuật không phù hợp
Đưa ra mục tiêu định lượng

Prompt quy định:

Time Complexity: O(N)
Space Complexity: O(1) hoặc O(N)

Đây là điểm rất mạnh.

AI có tiêu chí cụ thể để đánh giá lời giải.

Có ràng buộc kỹ thuật

Prompt yêu cầu:

Giữ nguyên kiểu trả về long

Nhờ vậy AI không tự ý đổi sang:

BigInteger
double
int
2. Vì sao đây là ví dụ tốt của Iterative Prompting?

Lượt đầu:

return fib(n - 1) + fib(n - 2);

AI tạo lời giải đúng nhưng chưa tối ưu.

Lượt tiếp theo:

Người dùng phản hồi dựa trên kết quả trước.
Chỉ rõ điểm yếu.
Đưa tiêu chí cải thiện.

Đó chính là bản chất của:

Iterative Prompting = Đánh giá → Phản hồi → Tinh chỉnh.

3. Loại trừ phương án A
Prompt A

"Code chạy chậm quá, viết lại bằng thuật toán khác tối ưu hơn giúp tôi."

Ưu điểm
Có chỉ ra vấn đề hiệu năng.
Nhược điểm
Quá mơ hồ

"Thuật toán khác tối ưu hơn" có thể là:

Memoization
Tabulation
Matrix Exponentiation
Fast Doubling
Song song hóa

AI không biết chính xác người dùng muốn gì.

Không có mục tiêu độ phức tạp

Không yêu cầu:

O(N)

nên AI có thể tạo lời giải:

O(N log N)

hoặc thậm chí vẫn chưa tối ưu đủ.

Không có ràng buộc

AI có thể:

Đổi kiểu trả về.
Đổi giao diện hàm.
Viết lại hoàn toàn class.

➡️ Kết quả không ổn định.

4. Loại trừ phương án C
Prompt C

"Hãy viết lại code tính Fibonacci bằng cách sử dụng Java Stream API để code chạy song song (parallel) cho nhanh hơn."

Sai hướng tối ưu

Vấn đề gốc không phải:

Thiếu đa luồng

Mà là:

Thuật toán quá tệ
Thuật toán xấu + Parallel = Vẫn xấu

Hiện tại:

O(2ⁿ)

Nếu chạy song song:

Parallel O(2ⁿ)

vẫn là:

O(2ⁿ)

Chỉ giảm một phần thời gian thực thi, không giải quyết bản chất.

Tăng chi phí hệ thống

Song song hóa đệ quy Fibonacci thường gây:

Tạo quá nhiều task.
Overhead quản lý thread.
Tốn bộ nhớ.

Thậm chí có thể còn chậm hơn với giá trị n vừa phải.

Không đúng yêu cầu đề bài

Đề bài yêu cầu:

Dynamic Programming

Trong khi phương án C yêu cầu:

Java Stream API

Hai hướng hoàn toàn khác nhau.

➡️ Không đạt mục tiêu tối ưu thuật toán.

Kết luận
Phương án	Đánh giá
A	❌ Có nêu vấn đề nhưng quá mơ hồ, thiếu ràng buộc kỹ thuật
B	✅ Tối ưu nhất, chỉ rõ kỹ thuật DP, mục tiêu độ phức tạp và ràng buộc
C	❌ Tập trung vào song song hóa thay vì cải thiện thuật toán
Đáp án cuối cùng: B

Vì phương án B mô tả rõ nguyên nhân hiệu năng, kỹ thuật cần áp dụng (Dynamic Programming), độ phức tạp mục tiêu O(N) và ràng buộc giữ nguyên kiểu dữ liệu, giúp AI tạo ra lời giải chính xác, nhất quán và phù hợp với kỹ thuật Prompt lặp (Iterative Prompting).