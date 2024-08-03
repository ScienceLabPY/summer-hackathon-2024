# Một Khung Làm Việc Hiệu Quả Để Tiếp Cận Các Vấn Đề Thiết Kế Hệ Thống

**Tác giả:** Li Lu  
**Xuất bản trên:** The Startup  
**Thời gian đọc:** 6 phút  
**Ngày xuất bản:** 10/08/2020

---

## Tổng Quan

Trong quá trình làm việc như một nhà phát triển phần mềm hoặc một người hướng dẫn cho các nhà phát triển phần mềm, cụm từ "thiết kế hệ thống" xuất hiện khá thường xuyên. Thực tế, dù là trong phát triển phần mềm thực tế hay các cuộc phỏng vấn kỹ thuật, "thiết kế hệ thống" luôn đóng vai trò trung tâm. Tôi hiểu rõ những khó khăn mà các vấn đề thiết kế hệ thống mang lại, và tôi cũng đã từng phải đối mặt với chúng trong cả các tình huống thực tế lẫn phỏng vấn. Những kinh nghiệm này, dù là những thành công hay những lần thất bại, đã dẫn dắt tôi tìm kiếm một khung làm việc hiệu quả để tiếp cận các thách thức thiết kế hệ thống một cách có hệ thống. Dưới đây là một số suy nghĩ của tôi.

## Góc nhìn toàn cảnh

![System Design](/assets/design-system/problem.png)

Đầu tiên, hãy nói về một số ý tưởng chung về việc thiết kế hệ thống phần mềm. Tôi nhận thấy có ba điều cơ bản làm cho các chủ đề liên quan đến thiết kế khác biệt so với các chủ đề kỹ thuật khác:

1. Không có thiết kế nào là hoàn hảo tuyệt đối, nhưng có nhiều giải pháp đủ tốt. Các kỹ sư khác nhau có thể có quan điểm hoàn toàn khác nhau, và chúng ta cần chấp nhận sự đa dạng này.
2. Cách bạn đạt đến kết luận quan trọng hơn nhiều so với chính kết luận đó. Trong khi chúng ta hiểu rằng các hành động và kết quả là rất quan trọng, thì các câu hỏi được đặt ra, những ý tưởng và sự động não trong quá trình thảo luận cũng nâng cao kết quả của thiết kế.
3. "Rome không được xây trong một ngày." Việc thu thập và hiểu tất cả các thông tin cho cuộc thảo luận có thể cần nhiều năm kinh nghiệm, vì vậy không thực tế để xây dựng kỹ năng thiết kế của bạn chỉ bằng sự hưng phấn nhất thời.

Dưới những quan sát này, có hai loại thách thức thực sự khi theo đuổi một thiết kế. Loại đầu tiên là biết quá ít về kiến thức lĩnh vực: để đưa ra thiết kế tốt, bạn cần phải hiểu rõ nhiều khía cạnh của khoa học máy tính, đặc biệt là các hệ thống máy tính. Loại thứ hai là biết quá nhiều: đôi khi chúng ta biết quá nhiều và nhận ra có quá nhiều vấn đề cần giải quyết nhưng không biết bắt đầu từ đâu. Chúng ta có thể chọn một cách ngẫu nhiên để bắt đầu nhưng dễ dàng bị phân tâm. Sau nhiều giờ thảo luận (hoặc nửa giờ trong một cuộc phỏng vấn), chúng ta nhận ra rằng mình đã bị phân tâm và quên mất điều gì đó quan trọng.

Mô hình của chúng tôi giải quyết loại thách thức thứ hai nêu trên. Đối với loại thách thức đầu tiên, tôi khuyên bạn nên bắt đầu xây dựng kỹ năng của mình một cách từ từ, vì vậy hãy có một danh sách đọc về thiết kế hệ thống tốt và bắt đầu đọc ngay hôm nay.

## Mô Hình Để Tiếp Cận Thiết Kế Tốt

Vậy, phần thú vị đây rồi. Mặc dù các vấn đề thiết kế hệ thống đặt ra những thách thức đáng kể cho quá trình phát triển phần mềm của chúng ta, cả trong môi trường làm việc thực tế và trong các cuộc phỏng vấn, tôi nhận thấy có những quy tắc chung. Sau khi tóm tắt những quy tắc này, đây là mô hình tôi sử dụng để tiếp cận một thiết kế tốt.

Cụ thể, chúng ta có thể tiếp cận một thiết kế tốt bằng cách xem xét các trường hợp sử dụng, yêu cầu, kế hoạch cam kết và chính hệ thống. Để dễ nhớ, tôi gọi đó là mô hình "URCS", đặt tên theo chương trình tiến sĩ của tôi tại Khoa Khoa Học Máy Tính, Đại học Rochester.

![URCS](/assets/design-system/urcs.png)

### Trường Hợp Sử Dụng (Use Cases)

Hiểu các trường hợp sử dụng giúp chúng ta hiểu đúng cách hệ thống hoạt động cho người dùng của chúng ta, và làm thế nào để tối ưu hóa hệ thống theo các trường hợp sử dụng. Trong bước này, chúng ta chuyển một yêu cầu kinh doanh mơ hồ thành một vấn đề phần mềm cụ thể. Chúng ta có thể bắt đầu bằng cách tự hỏi:

a. Ai là người dùng của hệ thống?  
b. Quy trình làm việc từ đầu đến cuối cho mỗi loại người dùng là gì?  
c. Có các mẫu sử dụng cụ thể nào không? Ví dụ, có bao nhiêu người đọc/người viết/người quản trị sẽ sử dụng hệ thống? Ai là người dùng thường xuyên? Ai là người dùng không thường xuyên?

Sau khi hiểu rõ các trường hợp sử dụng, chúng ta chuyển vấn đề của mình hoàn toàn vào thế giới kỹ thuật. Chúng ta có thể tiến tới các khía cạnh kỹ thuật.

### Yêu Cầu (Requirements)

Có nhiều khía cạnh chúng ta cần xem xét để định nghĩa chính xác hệ thống của mình. Đây là một trong những phần chính để tiếp cận một thiết kế tốt, vì chúng ta thực sự cần biết mình đang làm gì sau đó. Chúng ta có thể bắt đầu kiểm tra bằng cách tự hỏi các câu hỏi từ các khía cạnh khác nhau.

a. Quy mô hệ thống
- Người dùng: Có bao nhiêu người dùng? Bao nhiêu người dùng hoạt động? Qps (queries per second)? Chất lượng yêu cầu như thế nào?
- Dữ liệu: Khi hệ thống chạy, chúng ta sẽ tạo ra và lưu trữ bao nhiêu dữ liệu?

b. Yêu cầu về độ trễ
- Chúng ta sẽ cung cấp hệ thống trực tuyến hay ngoại tuyến? Độ trễ mong đợi của hệ thống là gì? Micro/Nanosecond? Millisecond? Phút? Giờ? Ngày?
- Dựa trên yêu cầu độ trễ, đối với disk IOs, chúng ta bị giới hạn bởi seeks hay throughput? Còn network IOs thì sao?
- Chúng ta sẽ tối ưu cho số trung bình, hay 80 percentile, hay 99 percentile?

c. Tiêu thụ băng thông
- Dựa trên dữ liệu chúng ta sẽ xử lý (đã đề cập trong mục a, ii), disk IO hoặc network sẽ trở thành điểm nghẽn?

d. Ngữ nghĩa
- Độ chịu lỗi của hệ thống: điều gì sẽ xảy ra nếu một thành phần bị lỗi? Cái gì trong bộ nhớ? Chúng ta sẽ mất gì?
- Chúng ta có cần độ sẵn sàng cao không? Nếu có, hãy quyết định chiến lược HA (High Availability) cho từng thành phần
- Chúng ta có duy trì tính nhất quán mạnh không? Nếu có, làm thế nào để đảm bảo điều này ngay cả khi có phân vùng mạng?
- Lưu ý giới hạn của định lý CAP.

e. Các hạn chế/giới hạn khác
- Hệ thống: số lượng nút? số lượng kết nối hoạt động? số lượng kết nối mạng tổng (bị giới hạn bởi số lượng cổng, số cố định)?
- Người dùng: giới hạn trên bị giới hạn bởi tổng dân số. Chúng ta có thể giới hạn thêm điều này không? Ví dụ, giới hạn bởi kích thước tổ chức, hoặc bởi vị trí địa lý của họ.
- Các yêu cầu khác: Bảo mật? An toàn? Lịch sự/Can thiệp khi hệ thống chạy?

### Kế Hoạch Cam Kết (Commitment Plan)

Chúng ta cần đảm bảo làm thế nào để đạt được các tính năng thiết kế. Lý tưởng nhất, tất cả các yêu cầu sẽ được thỏa mãn trong một lần. Tuy nhiên, trong thế giới thực, chúng ta luôn cần điều chỉnh kế hoạch và kỳ vọng do hạn chế về thời gian và ngân sách. Do đó, trước khi bắt tay vào hệ thống thực tế, chúng ta cần suy nghĩ về các bước để đạt được mục tiêu từ góc độ kỹ thuật thuần túy.

a. Chiến lược tổng thể của chúng ta là gì? Chúng ta cần giải pháp nhanh hay bền vững? Hạn chế về chi phí như thế nào?
b. Xác định tập hợp tính năng cơ bản cho MVP (Minimum Viable Product).
c. Định nghĩa kế hoạch phát triển của chúng ta theo các giai đoạn. Ban đầu, chúng ta có thể tập trung vào giai đoạn I, nhưng chắc chắn cần lưu ý đến các giai đoạn sau.
d. Xem xét tốc độ phát triển và chiến lược quản lý rủi ro của chúng ta. Chúng ta có thể đạt được mục tiêu nhanh đến mức nào? Khi nào chúng ta sẽ kiểm tra tiến độ? Và, làm thế nào để quản lý rủi ro nếu có sự cố trong quá trình phát triển? Có kế hoạch B không?

### Tổng Quan Hệ Thống (System Overview)

Chúng ta bắt đầu với các giao diện, định nghĩa ngữ nghĩa của chúng, định nghĩa loại giao diện: chúng là API, CLI, hay UI? Nếu là API, loại API nào chúng ta sẽ sử dụng? Ví dụ, chúng là RPC hay REST? Và tại sao?

Chúng ta có thể bắt đầu thiết kế, chia nhỏ các thành phần và vẽ sơ đồ. Một lưu ý nhanh ở đây là thiết kế ban đầu của chúng ta nên là thiết kế thỏa mãn các yêu cầu của chúng ta. Tôi không khuyến khích chiến lược "land and then expand" để dần dần khám phá các điểm nghẽn mới cần được đề cập trong các yêu cầu ban đầu của chúng ta. Kinh nghiệm trong kỹ thuật và phỏng vấn trước đây đã dạy tôi những bài học khó khăn về điều đó.

Một khi bạn đạt được bước này, chúc mừng bạn, bạn đang trên con đường đến với một thiết kế tốt!

## Suy Nghĩ Cuối Cùng

Cảm ơn bạn rất nhiều vì đã đọc đến đây. Nếu bạn cảm thấy điều này hữu ích, đừng quên vỗ tay! (Đây là lần đầu tiên tôi sử dụng Medium và hy vọng đây là cách mọi thứ hoạt động.) Tôi hiểu một số độc giả có thể cảm thấy thất vọng vì đây không phải là bài viết kỳ diệu giúp bạn hiểu ngay tất cả các khái niệm đã đề cập. Tuy nhiên, tôi hy vọng nó đóng vai trò là một khung làm việc tốt và là điểm khởi đầu để giúp bạn vượt qua thiết kế tiếp theo của mình.

## Tuyên Bố Miễn Trừ Trách Nhiệm

Mô hình được thảo luận trong bài viết này không nhằm mục đích là giải pháp tối ưu cho các cuộc thảo luận về thiết kế hệ thống. Nó chỉ đơn thuần là một dàn ý, hoặc điểm khởi đầu, để khởi động một cách có hệ thống tất cả các cuộc thảo luận liên quan đến thiết kế.
Các quan điểm trong bài viết này chỉ phản ánh quan điểm cá nhân của tôi. Bài viết này không có bất kỳ mối quan hệ nào với các nhà tuyển dụng trước đây hoặc trong tương lai của tôi. Chúng ta chỉ nên giới hạn cuộc thảo luận vào khía cạnh công nghệ thuần túy.
Tôi có quyền thêm mới các tuyên bố miễn trừ trách nhiệm.
