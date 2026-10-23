# SA-21 · Chấm bài giảng

Phần 1 khoảng 7,5 giờ (50 khái niệm), phần 2 khoảng 2,5 giờ; nên chia 8–10 buổi. Chấm thử 2 khái niệm trước. Đọc tab Luật chung trước.

## Việc này để làm gì

Khi người học bấm vào một khái niệm, hệ thống mở một bài giảng ngắn. Ta muốn biết bốn điều:

- bài do mô hình viết có đúng, trung thực, có ích hơn bản chỉ trích câu sách không;
- đồ thị tiên quyết có giúp bài tốt hơn không;
- cách đặt nhiệt độ của mô hình có làm bài lặp ý không;
- ví dụ ngoài sách có gây sai không.

## Bạn nhận được gì

**`phieu-sa21-<mã>.html` để đọc.** Mỗi khái niệm một mục:

- **phần đầu,** giống nhau cho mọi bản: tên khái niệm, module, câu định nghĩa nguyên văn kèm trang, ảnh công thức nếu có;
- **4–5 bản bài giảng** A, B, C, D (có khi thêm E), thứ tự ngẫu nhiên. Mỗi bản có thể có các khối: gợi lại tiên quyết kèm câu nối, giải thích, ví dụ, phân biệt với khái niệm gần, tiếp theo. Thiếu khối là một phần của bản đó;
- **nhãn nguồn** `[S1]`, `[Q2]`…: bấm vào thì hiện câu trích từ sách kèm trang;
- **ví dụ ngoài sách** nằm trong khung ghi rõ "ngoài sách".

**`cham-sa21-<mã>.xlsx` để ghi,** sheet **Chấm bài** cho phần 1. Phần 2 là tệp riêng, nhận sau khi đã nộp phần 1.

## Phần 1: chấm từng bản rồi xếp hạng

Sheet **Chấm bài**: mỗi khái niệm là một nhóm dòng liền nhau, mỗi dòng một bản.

**Bước 1: đọc và chấm từng bản.**

| cột | giá trị | nghĩa |
| --- | --- | --- |
| `so_y_sai` | `0`, `1`, `2`, `3+` | số ý **sai so với sách**: nói ngược sách, nhầm khái niệm, công thức sai. Ý sách không nói nhưng không sai thì không tính ở đây |
| `su_pham` | 1–5 | bản này giúp người học hiểu khái niệm tới đâu |
| `doc_duoc` | 1–5 | mạch lạc, đúng tiếng Việt, không lặp ý |
| `do_dai` | `ngan_qua` / `vua` / `dai_qua` | so với lượng cần để hiểu khái niệm này |
| `cau_noi` | `dat` / `co_loi` / trống | chỉ khi bản có câu nối; `co_loi` nếu **một** câu nối sai quan hệ, trích sai nguồn, hay bịa |
| `goi_lai_tiep_theo` | `co_ich` / `trung_tinh` / `thua` / trống | chỉ khi bản có khối gợi lại hay khối tiếp theo |
| `ngoai_sach` | `dung` / `gay_hieu_lam` / `sai` / trống | chỉ khi bản có ví dụ ngoài sách; **chấm bằng hiểu biết chung** |

Thang `su_pham`:

- **5:** hiểu rõ hơn hẳn so với chỉ đọc câu định nghĩa: gợi lại đúng nền, giải thích làm sáng ý khó, ví dụ hay phần phân biệt thật sự có ích.
- **3:** có ích, nhưng phần lớn chỉ nhắc lại định nghĩa, hoặc có khối thừa.
- **1:** không giúp gì, hoặc làm rối thêm.

Thang `doc_duoc`: **5** trôi chảy như người dạy viết, không lặp; **3** đọc được nhưng có chỗ vụng, lặp ý hay câu cụt; **1** khó đọc, lủng củng, lặp nhiều. Dùng 2 và 4 cho mức giữa.

**Bước 2: xếp hạng** (cột `hang`, ghi ở mọi dòng của nhóm). Nếu bạn là người học và muốn hiểu khái niệm này, bạn **muốn đọc bản nào nhất**? 1 là tốt nhất, được để bằng hạng. Xếp hạng sau khi đã chấm cả nhóm; một bản có ý sai khó có thể đứng hạng 1.

## Phần 2: từng ý có được nguồn đỡ không

**Mở phần 2 sau khi đã nộp phần 1**, trong tệp riêng `cham-sa21-y-<mã>.xlsx` kèm `phieu-sa21-y-<mã>.html`. Mỗi dòng là **một ý** của một bài giảng, cùng các câu trích nguồn mà ý đó dẫn, không có nhãn bản. Bạn có thể nhận ra bài đã đọc ở phần 1; điều đó không sao.

| cột | giá trị | nghĩa |
| --- | --- | --- |
| `duoc_do` | `tron` / `mot_phan` / `khong` | theo các câu trích **mà ý này dẫn**, có thể nói như vậy không |

- `tron`: mọi điều ý nói đều suy ra được từ câu trích.
- `mot_phan`: một phần ý được đỡ; phần còn lại thêm điều câu trích không nói.
- `khong`: câu trích không nói điều đó, hay nói khác đi.

Chỉ xét câu trích mà ý dẫn. Ý đúng theo phần khác của sách nhưng **không** theo câu trích nó dẫn là `khong`: trích dẫn sai là lỗi.

## Ca khó

- **Bản chỉ gồm câu trích nguyên văn:** thường `so_y_sai = 0` và `doc_duoc` không cao. Chấm `su_pham` thật: chép đúng câu sách có thể vẫn ít giúp người học.
- **Bản ngắn hơn hẳn:** ngắn không phải lỗi; `ngan_qua` chỉ khi thiếu điều cần để hiểu.
- **Công thức:** so với ảnh công thức gốc ở phần đầu; chép sai ký hiệu là ý sai.
- **Hai bản gần giống hệt:** có thể xảy ra; chấm từng bản, được để bằng hạng.
- **Câu nối nói đúng nhưng không dẫn đúng tiên quyết:** `cau_noi = co_loi`, ghi lý do.

## Kết quả của bạn được dùng thế nào

Từ thứ hạng, Claude tính bản thiết kế chính thắng từng bản so sánh ở bao nhiêu khái niệm. Luật quyết định đã viết trước khi đo:

- tỉ lệ ý không được nguồn đỡ (phần 2) phải ≤ 5%;
- bản theo nhiệt độ khác thắng ở chấm mù thì đề xuất đổi nhiệt độ;
- ví dụ ngoài sách sai hoặc gây hiểu lầm quá 5% thì đề xuất tắt.
