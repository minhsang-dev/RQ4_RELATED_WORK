# Khung tiểu luận tổng quan (v1)

**Đề tài:** Mô hình nền tảng dạng bảng, học trong ngữ cảnh và quản lý dữ liệu có nhãn cho phát hiện xâm nhập thích nghi.
**Phạm vi file này:** chỉ khung và thư mục tham khảo; không viết nội dung đầy đủ. Khóa tham khảo (`khóa`) tra trong `REVIEW_REFS.bib` / `REVIEW_REFS_STATUS.csv`.

**Quy ước trạng thái** (theo STATUS.csv): *OK / FIX applied* = đã kiểm ở REF_CHECK; *OK (opened)* = trang nguồn mở trong lần làm này; *provisional* = mới đọc tóm tắt/một phần; **STUB** = đã được kiểm toán trong PRIOR_ART/NOVELTY_AUDIT nhưng file .bib không đính kèm, cần mở lại trước khi trích [TO OPEN].

**Thiếu đầu vào (ảnh hưởng nội dung):** (i) `rq2_REFS_v2.bib` / `REFS.bib` / `PRIOR_ART.csv` không có trong thư mục đính kèm, nên các công trình của RQ2 chỉ có dạng STUB; (ii) mục "Tổng quan" của đề cương (Bảng 1.1, KT1–KT4) không đính kèm, nên mục 6 chưa gắn được định nghĩa KT; (iii) Bài 1 [9] là bản thảo của NCS chưa công bố (REF_CHECK: NOT_FOUND), không đưa vào danh sách tiểu luận và không trích kết quả của nó.

**Ràng buộc chung:** không nêu kết quả thực nghiệm của NCS (kể cả mức phát triển của HB2). Các mệnh đề "chưa thấy tiền lệ" chỉ phát biểu theo phạm vi tìm kiếm của các bản kiểm toán đính kèm.

---

## 1. IDS dưới trôi dạt và nhãn trễ: giao thức đánh giá theo thời gian, rò rỉ thông tin tương lai

**Mục đích.** Trình bày vì sao đánh giá IDS phải tôn trọng thứ tự thời gian và độ trễ nhãn, và các nguồn rò rỉ thông tin tương lai thường gặp (chia ngẫu nhiên, nhãn đến sau, lỗi nhãn của bộ dữ liệu). Làm nền cho các giao thức ở các mục sau.

**Tài liệu (14):** `gama2014survey`, `lu2019review`, `shyaa2024`, `pendlebury2019`, `arp2022`, `andresini2021`, `botacin2025`, `zliobaite2010`, `grzenda2020`, `gama2013`, `liu2022`, `engelen2021`, `luay2025`, `alahmadi2022`.

**Ghi chú dùng tài liệu.** `engelen2021` chỉ về CIC-IDS-2017; lỗi nhãn của CSE-CIC-IDS2018 dùng `liu2022`. `gama2014survey`/`lu2019review` là khảo sát chung, không dùng để hỗ trợ tuyên bố định lượng về tỷ lệ luồng độc hại.

**Câu hỏi mở.** Giao thức nào vừa tách đúng "chấm điểm trước, học sau" vừa mô phỏng độ trễ nhãn thực tế cho dữ liệu luồng mạng, và đo mức chênh giữa đánh giá theo thời gian với chia ngẫu nhiên thế nào mà không rò thông tin?

## 2. Mô hình nền dạng bảng và học trong ngữ cảnh (TabPFN, TabICL, TabFM), chi phí

**Mục đích.** Tóm lược các mô hình nền dạng bảng hoạt động bằng đọc ngữ cảnh (không cập nhật tham số), điểm mạnh trên dữ liệu nhỏ, và chi phí tính toán/bộ nhớ khi ngữ cảnh lớn; đối chiếu với LightGBM huấn luyện lại.

**Tài liệu (13):** `hollmann2025`, `qu2025tabicl`, `qu2026tabiclv2`, `googletabfm2026`, `kong2026tabfm`, `gangwani2025`, `helli2024`, `garcia2025`, `ke2017`, `thomas2024localpfn` (STUB), `ma2024tabdpt` (STUB), `feuer2024tunetables` (STUB), `xu2024mixturepfn` (STUB).

**Ghi chú dùng tài liệu.** `gangwani2025` đo TabPFN-1.0 và TabICL-base, không phải TabFM. Với TabFM nêu rõ biến thể (TabFM / TabFM+ / TabFM-Auto) [VERIFY]. Giấy phép trọng số TabFM là non-commercial.

**Câu hỏi mở.** Chi phí suy luận theo kích thước ngữ cảnh k của TabFM thay đổi thế nào so với huấn luyện lại LightGBM, và ngữ cảnh nên lớn đến mức nào cho IDS theo ngày?

## 3. Quản lý ngữ cảnh/bộ nhớ: replay trong học liên tục, bộ đệm cân bằng lớp/họ, chọn theo độ khó, CURE/DualFIFO

**Mục đích.** Hệ thống hóa các chính sách giữ/loại mẫu trong bộ nhớ bị chặn (hồ chứa cân bằng lớp, FIFO hai ngăn, cổng entropy, chọn theo độ khó/bất định) và phân biệt "bao nhiêu mẫu mỗi lớp" với "mẫu nào của lớp".

**Tài liệu (15):** `lourenco2026dualfifo`, `lee2026cure`, `chrysakis2020cbrs`, `amalapuram2023ecbrs`, `ariffin2026`, `aljundi2019mir`, `shim2021aser`, `bang2021rainbow`, `serra2025uncertainty`, `felzenszwalb2010`, `shrivastava2016ohem`, `xuan2020hard`, `abdullah2026ctxsamp`, `zhang2025ssf`, `mai2022survey`. Gần-liên quan để đối chiếu khi viết: `xie2025ugsr`, `mei2022hcil`, `rahman2025madar`, `treerath2026tabaicl`, `harun2025grasp`, `zhang2025sclifd`, `yang2025baep` (đều STUB, nằm trong NOVELTY_AUDIT_2).

**Ghi chú dùng tài liệu.** Trừ `chrysakis2020cbrs`, `lourenco2026dualfifo`, `lee2026cure` (đã kiểm ở REF_CHECK), phần lớn là STUB mức đọc tóm tắt (A) hoặc đoạn trích (S); phải mở lại trước khi trích. Theo NOVELTY_AUDIT_2 (RQ2: NARROW_REQUIRED): không viết "chưa có tiền lệ trực tiếp"; phát biểu theo hướng "áp dụng khai thác mẫu âm khó vào bộ nhớ có ngân sách nhãn, chọn theo lớp"; không gọi chọn theo điểm mô hình là đối xứng giữa các lớp (MADAR, UGSR có thiên lệch theo lớp); không viết "đánh giá độc lập". `xuan2020hard` và `abdullah2026ctxsamp` là cảnh báo về chọn khó nhất/chọn có chủ đích.

**Câu hỏi mở.** Giữ riêng một ngăn các dòng benign khó trong bộ nhớ cân bằng theo họ có ích hơn lấy ngẫu nhiên cùng ngân sách hay không, và khó nhất có nên là tiêu chí khi nhãn có thể nhiễu? (Chỉ nêu như câu hỏi; không trích kết quả của NCS.)

## 4. Chọn mẫu gán nhãn có ngân sách (active learning cho luồng, giảm lỗi kỳ vọng)

> **Mục này cần được mở rộng bởi nhóm RQ3.** Hiện chỉ dựa vào file đính kèm và 4 công trình mới mở (≤10 cho phép): `zliobaite2014active`, `cacciarelli2024`, `settles2010`, `roy2001eer`. Hai công trình đầu mới mở bản ghi Crossref, chưa đọc nội dung; `settles2010` mới thấy trang bìa và mục lục; `roy2001eer` mới đọc trang tóm tắt.

**Mục đích.** Đặt bài toán chọn dòng nào để xin nhãn khi ngân sách nhãn hằng ngày hữu hạn và nhãn đến trễ, từ truyền thống chọn mẫu theo bất định đến giảm lỗi kỳ vọng, và điểm khác của bối cảnh luồng có trôi dạt.

**Tài liệu (14):** `settles2010`, `roy2001eer`, `zliobaite2014active`, `cacciarelli2024`, `andresini2021`, `botacin2025`, `grzenda2020`, `zliobaite2010`, `treerath2026tabaicl` (STUB), `faber2022active` (STUB), `amalapuram2024soul` (STUB), `ipas2026lucos` (STUB), `lee2026cure`, `faber2023lifelong` (STUB).

**Ghi chú dùng tài liệu.** `lee2026cure` dùng entropy tính lúc dự đoán, trước khi biết nhãn: là cổng nhận vào bộ nhớ, không phải chọn dòng để xin nhãn. `treerath2026tabaicl` (margin của TabPFN dưới ngân sách nhãn) cần mở lại.

**Câu hỏi mở.** Với mô hình đọc ngữ cảnh, tiêu chí chọn dòng để gán nhãn có nên khác tiêu chí chọn dòng đưa vào ngữ cảnh, và giảm lỗi kỳ vọng có xấp xỉ rẻ được khi "huấn luyện lại" chỉ là đổi ngữ cảnh?

## 5. Nhãn nhiễu và đầu độc nhãn: lọc dòng, kiểm toán nguồn, chứng nhận độ bền

**Mục đích.** Phân biệt nhãn nhiễu ngẫu nhiên với lật nhãn có chủ đích từ nguồn bị chiếm; tổng hợp các tầng phòng thủ (lọc dòng kiểu RONI/kNN/confident learning, kiểm toán nguồn, chứng nhận độ bền) và các tấn công biết cơ chế phòng thủ.

**Tài liệu (15):** `nelson2008`, `northcutt2021`, `paudice2018`, `koh2022`, `jia2022knn`, `rosenfeld2020`, `dawid1979`, `miao2018`, `ma2020`, `fang2021`, `lan2025`, `bilos2026`, `korycki2020`, `liu2022`, `ariffin2026`. Mở rộng khi cần: `levine2021dpa`, `steinhardt2017`, `cao2022fltrust`, `sameera2025`, `priorpoison2026`, `dolejs2026`, `hu2026`, `djilani2025`, `severi2021`, `taheri2020`.

**Ghi chú dùng tài liệu.** `rosenfeld2020`, `levine2021dpa`, `steinhardt2017`, `dawid1979`, `cao2022fltrust` đang ở mức *provisional* (tóm tắt). `priorpoison2026` là kho mã chưa bình duyệt, một bộ dữ liệu, một seed. Chi tiết xếp hạng ở `RQ4_PRIOR_ART.md` (không có công trình nào xếp "same").

**Câu hỏi mở.** Một kiểm toán nguồn ngang hàng trong ngày cộng một bộ lọc dòng theo ảnh hưởng và hạn mức mỗi nguồn có giữ được ngữ cảnh sạch mà không loại nhầm trôi dạt thật và nguồn trung thực có phân phối khác không, kể cả khi đối thủ biết cơ chế?

## 6. Tổng hợp khoảng trống

**Thiếu định nghĩa KT1–KT4:** mục "Tổng quan" của đề cương v14.3 không đính kèm, nên bảng dưới đây ánh xạ theo **hướng nội dung**, không theo nhãn KT. Điền cột KT sau khi có đề cương [NEEDS OUTLINE]. Tôi không suy đoán nội dung KT1–KT4.

| Hướng khoảng trống | Mục & tài liệu chính | Bản kiểm toán đính kèm | Kết luận của bản kiểm toán | KT tương ứng |
|---|---|---|---|---|
| Đánh giá theo thời gian/nhãn trễ cho NIDS với mô hình nền dạng bảng | §1, §2: `pendlebury2019`, `arp2022`, `botacin2025`, `garcia2025`, `helli2024` | REF_CHECK (chỉ kiểm thư mục của Bài 1) | Không có phán quyết về độ mới; chỉ kiểm tính đúng của trích dẫn | [NEEDS OUTLINE] |
| Quản lý ngữ cảnh/bộ nhớ theo lớp, chọn theo độ khó (RQ2) | §3: `lee2026cure`, `lourenco2026dualfifo`, `amalapuram2023ecbrs`, `felzenszwalb2010` | NOVELTY_AUDIT_2, PRIOR_ART_1 | **NARROW_REQUIRED**: chỉ còn là "điều chỉnh có hướng lớp" (xếp hạng riêng benign bằng điểm tấn công trong ngữ cảnh cân bằng theo họ); không dùng cách nói "chưa có tiền lệ" | [NEEDS OUTLINE] |
| Chọn mẫu gán nhãn có ngân sách cho mô hình đọc ngữ cảnh (RQ3) | §4: `settles2010`, `roy2001eer`, `treerath2026tabaicl` | Không có bản kiểm toán đính kèm | Chưa đánh giá; cần nhóm RQ3 | [NEEDS OUTLINE] |
| Đầu độc nhãn có chủ đích và phòng thủ hai tầng cho ngữ cảnh mô hình nền (RQ4) | §5: `bilos2026`, `koh2022`, `miao2018`, `ma2020`, `jia2022knn` | RQ4_GAP.md, RQ4_PRIOR_ART.md | **GAP_NARROW**: các thành phần tồn tại riêng lẻ; chưa thấy tổ hợp nguồn + dòng + hạn mức cho mô hình học trong ngữ cảnh dạng bảng, chưa thấy chặn trên kiểu Mệnh đề 2, chưa thấy đối thủ thích nghi trên cặp này | [NEEDS OUTLINE] |

**Câu hỏi mở tổng.** Sau khi thu hẹp, phần đóng góp còn lại của mỗi hướng là gì và cách viết nào không vượt quá bằng chứng của các bản kiểm toán?
