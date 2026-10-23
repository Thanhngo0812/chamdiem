# Hướng dẫn chấm Pha B

Oct 22, 2026 · @Thành

Mỗi người chấm đọc tab này trước, rồi đọc tab của đợt mình chấm. Tổng khoảng 29 giờ mỗi người, chia thành nhiều buổi; giờ ước sẽ được sửa sau đợt chấm thử.

| đợt | việc | tab | thời gian mỗi người (ước) |
| --- | --- | --- | --- |
| 19a | duyệt 40 câu hỏi thử của trợ lý | 19a · Duyệt bộ câu | khoảng 40 phút |
| SA-20 | xếp hạng tên module, chấm mô tả | SA-20 · Tên module | khoảng 5,5 giờ |
| SA-21 | chấm bài giảng | SA-21 · Bài giảng | khoảng 10 giờ |
| SA-22 | chấm câu hỏi trắc nghiệm | SA-22 · Quiz | khoảng 8 giờ |
| SA-23 | chấm câu trả lời của trợ lý | SA-23 · Trợ lý | khoảng 4,5 giờ |

Thứ tự đề nghị: 19a trước, vì đánh giá trợ lý chờ bộ câu này; sau đó SA-20, SA-22, SA-21, SA-23.

## Việc này để làm gì

Kết quả chấm của bạn là kết luận cuối của các đánh giá. Hệ thống đọc một giáo trình rồi dựng lộ trình học: mỗi module có tên, mỗi khái niệm có bài giảng, có câu hỏi trắc nghiệm, và có trợ lý để hỏi đáp. Phần lớn nội dung này do mô hình ngôn ngữ viết.

Máy cũng tự đo, nhưng số máy đo chỉ để tham khảo. Trong báo cáo đồ án, kết quả được ghi là "chấm của nhóm", không phải "chấm của chuyên gia".

## Bốn nguyên tắc

1. **Chấm độc lập.** Không bàn với người chấm kia cho tới khi cả hai đã nộp; sau đó mới hội ý. Bàn trước thì hai bộ nhãn giống nhau một cách giả tạo, và độ đồng thuận đo ra mất nghĩa.
2. **Chấm mù.** Bạn không biết bản nào do cấu hình nào sinh ra. Các bản mang nhãn A, B, C, D theo thứ tự ngẫu nhiên, mỗi phiếu một kiểu. Đừng cố đoán. Tình cờ đoán ra, ví dụ một bản chỉ gồm câu chép sách, thì vẫn chấm theo tiêu chí như mọi bản.
3. **Chấm theo tài liệu.** "Đúng" là đúng theo cuốn sách, không theo hiểu biết riêng hay Internet. Phân vân thì mở PDF ở trang được ghi. Ngoại lệ duy nhất: phần đánh dấu "ví dụ ngoài sách" chấm bằng hiểu biết chung.

## Bạn nhận được gì

Mỗi đợt, chủ dự án gửi bạn một thư mục. `<mã>` là mã người chấm của bạn, `C1` hoặc `C2`.

| thứ | dùng để làm gì |
| --- | --- |
| `phieu-<đợt>-<mã>.html` | **Đọc** các mục cần chấm. Mở bằng trình duyệt, chạy được khi không có mạng, ảnh công thức đã nhúng sẵn |
| `cham-<đợt>-<mã>.xlsx` | **Ghi** nhãn. Mỗi dòng một mục, khớp với mã mục trong tệp HTML |
| PDF của sáu cuốn phát triển | Tra khi cần |

Đợt tên module (SA-20) không có tệp HTML: mọi thứ cần đọc nằm trong Excel. Hai người có cùng các mục, nhưng thứ tự mục và thứ tự A/B/C/D có thể khác nhau.

Tệp Excel có ba sheet:

| sheet | nội dung | bạn làm gì |
| --- | --- | --- |
| **Hướng dẫn** | đợt, mã người chấm, tóm tắt luật, ô ghi thời gian | ghi giờ bắt đầu và kết thúc mỗi buổi |
| **Chấm** | mỗi dòng một mục; cột xám là thông tin, cột vàng là chỗ bạn ghi | **chỉ ghi vào cột vàng** |
| **Ghi chú chung** | bảng trống | ghi điều muốn báo không gắn với mục nào |

Cột vàng có danh sách chọn sẵn: chọn trong danh sách, đừng gõ chữ khác. Cột `ghi_chu` gõ tự do.

## Quy trình mỗi đợt

1. **Đọc tab của đợt** một lần từ đầu tới cuối.
2. **Chấm thử** (trừ 19a) trong tệp `thu-<đợt>-<mã>.xlsx`, độc lập, rồi nộp. Claude so hai bản; một tiêu chí bị hiểu theo hai cách thì sửa hướng dẫn. Mục chấm thử không tính vào kết quả.
3. **Chấm thật** theo thứ tự dòng. Đừng sắp lại hay lọc dòng: thứ tự đã được trộn để tránh thiên lệch.
4. **Chia buổi,** mỗi buổi tối đa 60–90 phút rồi nghỉ, vì chấm lâu sẽ mệt và dễ dãi dần. Ghi giờ vào sheet Hướng dẫn.
5. **Kiểm trước khi nộp:** mọi cột vàng đã có giá trị, trừ cột mà tab của đợt ghi là để trống khi không áp dụng.
6. **Nộp** tệp Excel cho chủ dự án. Không gửi cho người chấm kia.

## Khi phân vân

- Chọn nhãn bạn thấy **đúng nhất**, rồi ghi lý do ngắn vào `ghi_chu`. Đừng để trống chỉ vì không chắc.
- "Ngang" chỉ dùng khi hai bản thật sự tốt như nhau, hay tệ như nhau; đừng dùng để né một quyết định khó.
- Một mục bị lỗi (thiếu chữ, ảnh không hiện, hai bản giống hệt nhau): ghi `ghi_chu` bắt đầu bằng `LOI:`, rồi chấm phần chấm được.
- Một luật trái với cảm nhận của bạn: **vẫn theo luật**, và ghi điều đó vào sheet Ghi chú chung. Luật được sửa sau đợt, không sửa giữa chừng.

## Không được làm

- Bàn với người chấm kia trước khi cả hai nộp.
- Dùng công cụ AI để đọc, tóm tắt hay chấm.
- Tìm cách biết bản nào là cấu hình nào: mở repo, mở thư mục `artifacts`, hay hỏi người chạy.
- Sửa cột xám, xoá dòng, đổi thứ tự dòng, đổi tên tệp.
- Gửi phiếu hay nội dung sách ra ngoài nhóm.

## Sau khi nộp: hội ý

1. Claude tính độ đồng thuận **trước** hội ý: κ của Cohen kèm phần trăm đồng ý, và Gwet AC1 cho nhãn hiếm như lỗi viết câu, vì κ bị kéo thấp khi nhãn dương hiếm.
2. Claude gửi danh sách các mục hai người chấm khác nhau.
3. Hai người xem từng mục và chốt một **nhãn sau hội ý**. Nhãn gốc của từng người giữ nguyên, vì độ đồng thuận tính trên nhãn gốc.
4. Không chốt được thì ghi cả hai ý kiến; chủ dự án đọc những mục này khi ra quyết định.

## Câu hỏi thường gặp

**Tôi có cần là chuyên gia môn học không?** Không. Bạn chấm theo sách, có PDF để tra. Chỗ nào cần hiểu sâu thì tab của đợt ghi cách làm.

**Tôi nhận ra một bản rõ ràng là "máy chép sách". Có sao không?** Không sao, vẫn chấm như mọi bản. Điều này đã biết trước là không giấu được.

**Chấm sai một mục thì sao?** Trong lúc chấm bạn được sửa nhãn của mình. Sau khi nộp thì không sửa; chỗ khác nhau được bàn ở buổi hội ý.

**Tôi thấy hệ thống sai một cách thú vị. Ghi ở đâu?** Vào `ghi_chu` của mục đó. Những ca như vậy sẽ được trích vào báo cáo.
