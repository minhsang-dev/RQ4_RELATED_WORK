# COVERAGE (v2)

**"Đã kiểm chứng"** = trạng thái OK / FIX applied: đã kiểm ở REF_CHECK, hoặc trang nguồn đã mở, hoặc mục từ `rq2_REFS_v2_1.bib` có phần phương pháp đã đọc theo PRIOR_ART_1 (mức đọc T) / NOVELTY_AUDIT_2. **Không tính** provisional (mức đọc A hoặc S của PRIOR_ART_1, hoặc chỉ tóm tắt/một phần ở RQ4), NOT_FOUND, [VERIFY]. Việc thay STUB bằng mục bib đầy đủ không tự nâng mức đọc. Nhóm do tôi đặt; NCS chỉnh theo cấu trúc tiểu luận.

| Nhóm nhỏ | Đã kiểm chứng / số khóa | Cờ |
|---|---|---|
| Khảo sát trôi dạt khái niệm | 4 / 4 | đủ |
| Đánh giá theo thời gian / rò rỉ trong bảo mật | 5 / 5 | đủ |
| Nhãn trễ | 3 / 3 | đủ |
| Lỗi nhãn / hạn chế của bộ dữ liệu NIDS | 5 / 5 | đủ |
| Bộ dữ liệu NetFlow | 6 / 6 | đủ |
| Kiến trúc mô hình nền dạng bảng | 7 / 7 | đủ |
| Chi phí suy luận của mô hình nền dạng bảng | 1 / 1 | **<3** |
| Mô hình nền dạng bảng dưới trôi dạt / luồng | 3 / 3 | đủ |
| Mô hình nền dạng bảng cho IDS | 2 / 2 | **<3** |
| Chọn/truy xuất ngữ cảnh cho mô hình nền dạng bảng | 3 / 8 | đủ |
| Replay / bộ nhớ trong học liên tục | 2 / 7 | **<3** |
| Khai thác mẫu âm khó / chọn theo độ khó | 2 / 5 | **<3** |
| Học liên tục cho IDS có bộ nhớ | 2 / 5 | **<3** |
| Active learning cho luồng / ngân sách nhãn | 7 / 7 | đủ |
| Giảm lỗi kỳ vọng (expected error reduction) | 1 / 1 | **<3** |
| Active learning gắn với mô hình nền dạng bảng | 1 / 1 | **<3** |
| Phương pháp nhãn nhiễu / làm sạch nhãn | 3 / 4 | đủ |
| Đầu độc nhãn trên NIDS / malware | 0 / 6 | **<3** |
| Đầu độc ngữ cảnh ICL / mô hình nền dạng bảng | 3 / 7 | đủ |
| Chứng nhận độ bền trước đầu độc | 1 / 4 | **<3** |
| Kiểm toán nguồn / chất lượng người gán nhãn | 1 / 8 | **<3** |
| Chống đầu độc ở mức cập nhật (học liên kết, tiếng Việt) | 2 / 3 | **<3** |
| Ảnh hưởng mẫu / định giá dữ liệu | 0 / 3 | **<3** |
| Phương pháp đánh giá (tiền đăng ký, phương sai) | 4 / 4 | đủ |
| Thống kê (kiểm định, bootstrap khối) | 5 / 5 | đủ |

## Nhóm dưới 3 tài liệu đã kiểm chứng: khóa còn ở mức provisional và việc cần làm

Các khóa liệt kê đã có mục bib nhưng mới đọc tóm tắt/đoạn trích/một phần; việc cần làm là đọc phương pháp. Tiêu đề [TO OPEN] chọn từ hiểu biết của tôi, chưa mở trang nguồn, không phải tài liệu đã xác minh.

- **Chi phí suy luận của mô hình nền dạng bảng** (1/1): provisional/khác: —. [TO OPEN] phần chi phí trong bản gốc TabPFN v2 và TabICL (đã có `hollmann2025`, `qu2025tabicl`, cần đọc); chi phí suy luận trong `kong2026tabfm`.
- **Mô hình nền dạng bảng cho IDS** (2/2): provisional/khác: —. Đọc nội dung `aldahmani2026` (mới thấy tóm tắt); tìm thêm đánh giá TabPFN/TabICL cho IDS ngoài `garcia2025` (chưa tìm).
- **Replay / bộ nhớ trong học liên tục** (2/7): provisional/khác: `aljundi2019mir`, `shim2021aser`, `bang2021rainbow`, `mai2022survey`, `rebuffi2017icarl`. [TO OPEN] "Experience replay for continual learning" (Rolnick et al., NeurIPS 2019); "A continual learning survey: Defying forgetting in classification tasks" (De Lange et al., TPAMI 2022).
- **Khai thác mẫu âm khó / chọn theo độ khó** (2/5): provisional/khác: `xuan2020hard`, `serra2025uncertainty`, `sung1998bootstrap`. [TO OPEN] bài gốc Sung & Poggio 1998 (mô tả hiện chỉ qua OHEM/Felzenszwalb).
- **Học liên tục cho IDS có bộ nhớ** (2/5): provisional/khác: `ariffin2026`, `faber2022active`, `xu2026coreset`. 
- **Giảm lỗi kỳ vọng (expected error reduction)** (1/1): provisional/khác: —. [TO OPEN] "Bayesian active learning for classification and preference learning" (Houlsby et al., 2011); "Deep Bayesian active learning with image data" (Gal et al., ICML 2017). `roy2001eer` mới đọc trang tóm tắt.
- **Active learning gắn với mô hình nền dạng bảng** (1/1): provisional/khác: —. NOVELTY_AUDIT_2 đã đọc `treerath2026tabaicl`; nhóm RQ3 cần đọc lại đối chiếu với KT3.
- **Đầu độc nhãn trên NIDS / malware** (0/6): provisional/khác: `ariffin2026`, `lan2025`, `dolejs2026`, `severi2021`, `taheri2020`, `aryal2022`. Đọc đầy đủ `ariffin2026`, `lan2025`, `dolejs2026`; [TO OPEN] "Poisoning attacks against support vector machines" (Biggio et al., ICML 2012).
- **Chứng nhận độ bền trước đầu độc** (1/4): provisional/khác: `rosenfeld2020`, `levine2021dpa`, `steinhardt2017`. [TO OPEN] "Dataset security for machine learning: Data poisoning, backdoor attacks, and defenses" (Goldblum et al., TPAMI 2023); đọc phương pháp `rosenfeld2020`, `levine2021dpa`, `steinhardt2017`.
- **Kiểm toán nguồn / chất lượng người gán nhãn** (1/8): provisional/khác: `miao2018`, `fang2021`, `dawid1979`, `zhang2025peer`, `cao2022fltrust`, `vejling2025`, `xu2016`. Đọc toàn văn `dawid1979`, `zhang2025peer`, `cao2022fltrust`; [TO OPEN] "Learning from crowds" (Raykar et al., JMLR 2010); Shnayder et al. 2016 (peer prediction).
- **Chống đầu độc ở mức cập nhật (học liên kết, tiếng Việt)** (2/3): provisional/khác: `sameera2025`. `luong2023fedls`, `ha2024` mới đọc bản ghi Crossref (chưa đọc nội dung); `sameera2025` đã đọc một phần.
- **Ảnh hưởng mẫu / định giá dữ liệu** (0/3): provisional/khác: `ghorbani2019`, `jia2019knnshap`, `pruthi2020`. [TO OPEN] "Understanding black-box predictions via influence functions" (Koh & Liang, ICML 2017); đọc phương pháp `ghorbani2019`, `jia2019knnshap`, `pruthi2020`.

## Kiểm tra danh mục tài liệu của đề cương (50 mục) so với danh sách gộp

- Đã có sẵn trong danh sách gộp: 29 mục (trong đó provisional: [24], [25], [34], [35], [36], [37]; đây không phải mục thiếu). Thiếu và đã thêm sau khi mở trang nguồn: 21 mục, liệt kê dưới đây.

| [n] | Khóa | Nguồn đã mở | Trạng thái |
|---|---|---|---|
| [1] | `gupta2025netguard` | arXiv abs | OK (opened: arXiv abs page) |
| [4] | `ndichu2026stral` | arXiv abs | OK (opened: arXiv abs page) |
| [10] | `googleblog2026tabfm` | trang blog Google Research | OK (opened); outline claims [VERIFY] |
| [15] | `kurashkin2026` | Crossref | OK (opened: Crossref) |
| [16] | `priorlabs2025tabpfn25` | arXiv abs | FIX applied |
| [18] | `macia2018ugr16` | Crossref | OK (opened: Crossref) |
| [19] | `goldschmidt2025` | arXiv abs | FIX applied |
| [20] | `cantone2024` | arXiv abs | FIX applied |
| [22] | `aldahmani2026` | arXiv abs | OK (opened: arXiv abs page) |
| [27] | `gonzalez1985` | Crossref | OK (opened: Crossref) |
| [29] | `barbero2022` | Crossref (kết quả tìm) | OK (opened: Crossref) |
| [39] | `nguyen2026cdahal` | Crossref | OK (opened: Crossref) |
| [40] | `thai2022` | Crossref (kết quả tìm) | FIX applied |
| [41] | `nguyen2025sefed` | Crossref | OK (opened: Crossref) |
| [42] | `nguyen2025adisrae` | trang VJOL | OK (opened: VJOL page) |
| [43] | `vu2024` | Crossref (kết quả tìm) | OK (opened: Crossref) |
| [44] | `tran2023` | Crossref | FIX applied |
| [45] | `luong2023fedls` | Crossref | OK (opened: Crossref) |
| [46] | `ha2024` | Crossref | OK (opened: Crossref); volume/issue [VERIFY] |
| [47] | `lipton2018` | trang PMLR | OK (opened: PMLR page) |
| [48] | `gomes2017arf` | Crossref | OK (opened: Crossref) |

Điểm lệch giữa đề cương và nguồn đã mở (không sửa đề cương; NCS quyết định): [10] blog Google không nêu giới hạn 10 lớp / 500 đặc trưng hay giấy phép mà phần Tổng quan gán cho [10]; [16] đề cương ghi tác giả "Prior Labs", arXiv ghi Grinsztajn, Flöge, Key và 23 tác giả khác; [19] có bản tạp chí Comput. Secur. 156 (2025) 104510; [20] có bản IEEE Access 12:144489–144508 (2024); [40] DOI trong đề cương bị cụt, Crossref: 10.1109/rivf55975.2022.10013926; [44] Crossref: IEEE IoT-J vol. 10 no. 10, 2023, pp. 8578–8589; [41] Crossref ghi năm 2025; [46] vol./no. chưa xác nhận.

Các khóa trong danh sách gộp nhưng **không** nằm trong đề cương (Bài 1, RQ4, RQ2) không liệt kê.

## Tổng số
- Khóa trong thư mục gộp: 167; đã kiểm chứng (OK/FIX): 91; provisional: 74; khác ([VERIFY]/NOT_FOUND, không tính ở trên): 2; STUB: 0.
- Nguồn của 55 mục thay STUB (`rq2_REFS_v2_1.bib`): 13 ở mức OK (mức đọc T hoặc NOVELTY_AUDIT_2), 42 ở mức provisional (mức đọc A/S).
- "Vejling" ([34]) và "Xu" ([35]) nằm trong danh sách (`vejling2025`, `xu2016`); `xu2024mixturepfn` và `xu2026coreset` không phải [35].
