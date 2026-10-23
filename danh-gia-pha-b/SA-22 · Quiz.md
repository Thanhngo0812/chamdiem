# SA-22 · Chấm câu hỏi trắc nghiệm

Khoảng 320 câu, khoảng 1,5 phút mỗi câu, tức khoảng 8 giờ. Chấm thử 20 câu ngoài mẫu trước. Đọc tab Luật chung trước.

## Việc này để làm gì

Hệ thống sinh câu trắc nghiệm để người học tự kiểm tra sau mỗi module, theo hai kiểu: câu do mô hình viết, và câu điền khuyết dựng từ một câu trong sách. Trước khi đưa cho người học, mô hình kiểm câu một lần nữa. Ta muốn biết:

- câu có đạt chuẩn viết câu trắc nghiệm không;
- bao nhiêu câu có hơn một đáp án đúng;
- lần kiểm của mô hình bắt được bao nhiêu lỗi.

Trong phiếu có trộn cả những câu mà lần kiểm đã loại. Bạn không biết câu nào, và cũng đừng đoán.

## Bạn nhận được gì

- `phieu-sa22-<mã>.html`. Mỗi câu gồm: mã câu, cuốn, module; câu dẫn và các phương án A–C; khối **"Đáp án và nguồn"** gập sẵn, chứa khái niệm câu kiểm, phương án hệ thống đánh dấu đúng, câu trích sách kèm trang, ảnh công thức nếu có.
- `cham-sa22-<mã>.xlsx`, sheet **Chấm**, mỗi dòng một câu.

## Cách chấm một câu

1. **Tự làm câu.** Đọc câu dẫn và phương án, ghi phương án bạn chọn vào `dap_an_cua_ban` **trước khi** mở khối "Đáp án và nguồn". Không chắc thì vẫn chọn, rồi ghi `khong_chac` vào `ghi_chu`. Bạn chọn sai là tín hiệu câu mơ hồ hay đáp án sai, nên đừng mở khối trước.
2. **Mở khối "Đáp án và nguồn",** đọc câu trích, mở PDF nếu cần.
3. **Chấm các cột vàng:**

| cột | giá trị | `co` khi |
| --- | --- | --- |
| `dap_an_dung` | `co` / `khong` | phương án hệ thống đánh dấu đúng thật sự đúng theo câu trích |
| `mot_dap_an` | `co` / `khong` | **chỉ một** phương án đúng theo tài liệu; một phương án nhiễu cũng đúng, hay đúng một phần mà vẫn chấp nhận được, thì `khong` |
| `nhieu_sai` | `co` / `khong` | mọi phương án nhiễu đều sai theo tài liệu |
| `dung_khai_niem` | `co` / `khong` | câu kiểm đúng khái niệm ghi trong khối "Đáp án và nguồn" (tên khái niệm chỉ nằm trong khối gập, vì với câu điền khuyết nó chính là đáp án) |
| `bloom_nguoi` | `nho` / `hieu` / `van_dung` / `phan_tich_tro_len` | mức nhận thức câu đòi hỏi, theo bạn |
| `loi_viet_cau` | mã lỗi cách nhau bằng dấu phẩy, hoặc trống | các lỗi trong bảng L01–L18 ở dưới, ví dụ `L04,L12` |
| `tieng_viet` | 1–3 | 3 tự nhiên; 2 hiểu được nhưng vụng; 1 sai ngữ pháp, khó hiểu |
| `ket_luan` | `dung_ngay` / `sua_nhe` / `bo` | có đưa câu này cho người học không; `sua_nhe` = sửa một hai chữ là dùng được, `bo` = phải viết lại hay câu sai |

## Mức Bloom

| mức | câu đòi hỏi | ví dụ |
| --- | --- | --- |
| `nho` | nhận ra hay nhắc lại điều sách viết | "Khái niệm nào được định nghĩa là …?" |
| `hieu` | diễn đạt lại, phân biệt, giải thích bằng lời khác sách | "Điểm khác nhau giữa đơn ánh và toàn ánh là gì?" |
| `van_dung` | áp dụng vào một trường hợp cụ thể chưa có nguyên văn trong sách | "Ánh xạ f(x) = 2x trên ℝ thuộc loại nào?" |
| `phan_tich_tro_len` | phân tích, đánh giá, so nhiều ý | hiếm gặp |

Câu điền khuyết hầu như luôn là `nho`.

## Bảng lỗi viết câu

Rút từ bảng 19 lỗi của Moore và cộng sự (2023), theo hướng dẫn của Haladyna, Downing và Rodriguez. "Nhiều hơn một đáp án đúng" đã có cột `mot_dap_an` riêng nên không có trong bảng mã.

| mã | lỗi | có lỗi khi |
| --- | --- | --- |
| L01 | mơ hồ | câu dẫn hay phương án hiểu được theo hai cách |
| L02 | câu nhiễu khó tin | người chưa học bài cũng loại được ngay một phương án nhiễu |
| L03 | "không có đáp án nào đúng" | có phương án này |
| L04 | phương án dài nhất là đáp án | đáp án dài hơn hẳn các phương án nhiễu |
| L05 | thông tin thừa | câu dẫn có thông tin không cần để trả lời |
| L06 | thực chất là câu đúng/sai | các phương án chỉ là đúng/sai, có/không |
| L07 | gợi ý hội tụ | đáp án chung nhiều từ nhất với các phương án khác, nên đoán được bằng cách tìm phương án "ở giữa" |
| L08 | gợi ý logic | câu dẫn và đáp án có liên hệ hình thức để đoán, ví dụ hỏi "hai điều kiện" mà chỉ đáp án có hai ý |
| L09 | "tất cả các đáp án trên" | có phương án này |
| L10 | chỗ trống giữa câu | câu dẫn có chỗ trống `___` nằm giữa câu |
| L11 | từ tuyệt đối | phương án có "luôn luôn", "không bao giờ", "mọi", "chỉ" |
| L12 | lặp từ câu dẫn ở đáp án | một từ đặc trưng của câu dẫn chỉ lặp lại ở đáp án |
| L13 | câu dẫn không tập trung | chưa xem phương án thì không biết câu hỏi hỏi gì |
| L14 | dạng tổ hợp | phương án kiểu "1 và 3 đúng" |
| L15 | gợi ý ngữ pháp | phương án nhiễu không khớp ngữ pháp với câu dẫn, đáp án thì khớp |
| L16 | sai thứ tự | phương án là số hay mốc nhưng không xếp theo thứ tự |
| L17 | từ mơ hồ | "thường", "đôi khi", "có thể", "đa số" làm câu không rõ đúng sai |
| L18 | câu dẫn phủ định | câu dẫn hỏi "không", "ngoại trừ" mà không nhấn mạnh rõ |

Câu có 0–1 lỗi viết câu và không có lỗi nặng là **chấp nhận được**. **Lỗi nặng** là `dap_an_dung = khong`, `mot_dap_an = khong`, hay `nhieu_sai = khong`. Bạn không cần tự tính.

## Ca khó

- **Câu điền khuyết:** theo định nghĩa có lỗi L10. Chấm L10 thật, đừng bỏ qua vì "kiểu câu này vốn vậy".
- **Phương án gần đúng:** một phương án nhiễu là khái niệm cha hay con của đáp án, ví dụ "Ánh xạ" khi đáp án là "Song ánh". Câu trích cho phép cả hai thì `mot_dap_an = khong`.
- **Đúng theo hiểu biết chung nhưng sách nói khác:** theo sách.
- **Công thức trong câu:** so với ảnh công thức gốc; ký hiệu chép sai thì `dap_an_dung` hay `nhieu_sai` có thể là `khong`.
- **Bạn làm sai câu ở bước 1:** không có nghĩa câu sai. Xem lại sau khi mở đáp án; câu mơ hồ thì ghi L01.

## Kết quả của bạn được dùng thế nào

Luật quyết định đã viết trước khi đo:

- bản mô hình làm mặc định nếu ≥ 80% câu chấp nhận được và ≤ 3% lỗi nặng;
- lần kiểm của mô hình được giữ nếu nó bắt ≥ 50% số lỗi nặng mà người tìm thấy, với độ chính xác ≥ 0,5.
