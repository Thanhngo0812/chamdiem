# SA-20 · Chấm tên và mô tả module

Phần 1 khoảng 4,5 giờ (162 module), phần 2 khoảng 1 giờ (60 mô tả). Chấm thử 8 module trước. Đọc tab Luật chung trước.

## Việc này để làm gì

Ta muốn biết cách đặt tên module nào tốt nhất theo mắt người. Lộ trình chia sách thành các module, mỗi module 3–8 khái niệm, và mỗi module cần một **tên** và một **mô tả ngắn**: đó là thứ người học thấy đầu tiên.

## Bạn nhận được gì

Một tệp `cham-sa20-<mã>.xlsx`, không có tệp HTML. Ngoài sheet Hướng dẫn và Ghi chú chung:

| sheet | nội dung |
| --- | --- |
| **Chấm** | phần 1: tên module |
| **Chấm mô tả** | phần 2: mô tả module |
| **Khái niệm** | **bị khoá**: mọi khái niệm của các module trong phiếu, kèm mã module, câu định nghĩa trong sách và trang |

## Phần 1: xếp hạng tên

**Mỗi module là một nhóm 2–4 dòng liền nhau,** mỗi dòng một tên, nhãn A–D theo thứ tự ngẫu nhiên. Hai cách đặt tên ra cùng một chữ thì chỉ hiện một dòng, nên có nhóm chỉ 2 hay 3 dòng.

Cột xám ở dòng đầu mỗi nhóm:

| cột | nghĩa |
| --- | --- |
| `ma_phieu` | mã module trong phiếu |
| `cuon` | cuốn sách |
| `khai_niem` | các khái niệm của module, theo thứ tự trong sách |
| `module_truoc`, `module_sau` | **các khái niệm** của hai module kề, không phải tên của chúng, để không thiên về một cách đặt tên |
| `nhan`, `ten` | nhãn A–D và tên cần chấm, ở mọi dòng |

Cột vàng, ghi ở **mọi dòng** của nhóm:

| cột | giá trị | nghĩa |
| --- | --- | --- |
| `hang` | 1–4 | 1 là tốt nhất; **được để bằng hạng**. Hạng tính trong nhóm, không so với module khác |
| `dung_noi_dung` | `dat` / `khong` | tên nói đúng điều module dạy; `khong` nếu rộng hẳn ("Phần II", tên cả chương) hay hẹp hẳn (một khái niệm trong 6) |
| `phan_biet` | `dat` / `khong` | đọc tên thì biết module này khác hai module kề ở đâu |
| `ngan_gon` | `dat` / `khong` | không thừa mã, số đánh mục, dấu `·` nối hai mẩu, mẩu câu cụt; dài tới khoảng 8 từ vẫn có thể `dat` |
| `tu_nhien` | `dat` / `khong` | là cụm tiếng Việt người dạy có thể viết làm tiêu đề; thuật ngữ tiếng Anh được nếu sách dùng |

**Cách làm một nhóm:**

1. Đọc `khai_niem`; chưa rõ module dạy gì thì tra sheet Khái niệm.
2. Liếc `module_truoc` và `module_sau` để biết module nằm giữa cái gì.
3. Chấm bốn cột `dat`/`khong` cho từng tên.
4. Xếp hạng theo cảm nhận chung của bạn với tư cách người học: muốn thấy tên nào trên lộ trình. Hạng không bắt buộc theo số ô `dat`, nhưng tên sai nội dung khó có thể đứng hạng 1.

**Ví dụ minh hoạ** (bịa để giải thích, không có trong phiếu). Module gồm: Đơn ánh, Toàn ánh, Song ánh, Ánh xạ ngược.

| nhãn | tên | nội dung | phân biệt | gọn | tự nhiên | hạng |
| --- | --- | --- | --- | --- | --- | --- |
| A | Phân loại ánh xạ | dat | dat | dat | dat | 1 |
| B | Ánh xạ · Đơn ánh | khong (hẹp) | khong | khong (dấu `·`) | khong | 3 |
| C | Đơn ánh, toàn ánh, song ánh và ánh xạ ngược | dat | dat | khong (liệt kê dài) | dat | 2 |
| D | Chương 1: Tập hợp và ánh xạ | khong (rộng) | khong | khong (số chương) | dat | 3 |

## Phần 2: mô tả module

Sheet **Chấm mô tả** có 60 module chọn theo tầng. Mỗi module có một mô tả, tách sẵn thành từng câu, mỗi câu một dòng.

| cột | giá trị | nghĩa |
| --- | --- | --- |
| `duoc_do` | `tron` / `mot_phan` / `khong` | câu được nội dung module chống đỡ trọn vẹn, một phần, hay không; căn cứ là các khái niệm của module và câu định nghĩa của chúng (sheet Khái niệm) |
| `sai_nang` | `co` / `khong` | câu nêu một khái niệm **không có** trong module, hay nói ngược với sách |
| `huu_ich` | `co_ich` / `binh_thuong` / `khong` | **chỉ ở dòng đầu** mỗi module: đọc xong có biết module dạy gì và cần gì trước không |

`mot_phan` dùng khi câu có hai ý mà chỉ một ý được chống đỡ, hay khi câu nói rộng hơn điều sách nói.

## Ca khó

- **Tên dùng tiêu đề của tác giả:** nếu tiêu đề mục khớp đúng nội dung module thì là tên tốt, dù nghe khô.
- **Tên đúng nhưng chung chung** ("Các khái niệm cơ bản"): thường `dung_noi_dung = dat`, `phan_biet = khong`.
- **Hai tên khác nhau một chữ:** vẫn xếp hạng; được để bằng hạng nếu thật sự không thấy khác.
- **Lỗi chính tả:** `tu_nhien = khong`, ghi lỗi vào `ghi_chu`.
- **Module trộn hai chủ đề:** tên nêu được cả hai thì `dung_noi_dung = dat`, dù hơi dài.

## Kết quả của bạn được dùng thế nào

Từ thứ hạng, Claude tính trong mỗi cặp cách đặt tên, cách nào thắng ở bao nhiêu module; luật quyết định đã viết trước khi đo. Phần 2 quyết định có giữ mô tả do mô hình viết không: cần ít nhất 95% câu `tron` và không câu nào `sai_nang`.
