# COVERAGE (v1)

**"Đã kiểm chứng"** = trạng thái OK / FIX applied (REF_CHECK) hoặc OK (opened) (RQ4 / lần mở mới). **Không tính** STUB (bib không đính kèm), provisional (chỉ đọc tóm tắt/một phần), NOT_FOUND, [VERIFY]. Các nhóm do tôi đặt; cần NCS chỉnh theo cấu trúc tiểu luận.

| Nhóm nhỏ | Đã kiểm chứng / số khóa liệt kê | Cờ |
|---|---|---|
| Khảo sát trôi dạt khái niệm | 3 / 3 | đủ |
| Đánh giá theo thời gian / rò rỉ trong bảo mật | 4 / 4 | đủ |
| Nhãn trễ | 3 / 3 | đủ |
| Lỗi nhãn của bộ dữ liệu NIDS | 2 / 2 | **<3** |
| Bộ dữ liệu NetFlow | 6 / 6 | đủ |
| Kiến trúc mô hình nền dạng bảng | 5 / 5 | đủ |
| Chi phí suy luận của mô hình nền dạng bảng | 1 / 1 | **<3** |
| Mô hình nền dạng bảng dưới trôi dạt / luồng | 3 / 3 | đủ |
| Mô hình nền dạng bảng cho IDS | 1 / 1 | **<3** |
| Chọn/truy xuất ngữ cảnh cho mô hình nền dạng bảng | 2 / 5 | **<3** |
| Replay / bộ nhớ trong học liên tục | 1 / 6 | **<3** |
| Khai thác mẫu âm khó / chọn theo độ khó | 0 / 4 | **<3** |
| Học liên tục cho IDS có bộ nhớ | 0 / 4 | **<3** |
| Active learning cho luồng / ngân sách nhãn | 4 / 4 | đủ |
| Giảm lỗi kỳ vọng (expected error reduction) | 1 / 1 | **<3** |
| Active learning gắn với mô hình nền dạng bảng | 0 / 1 | **<3** |
| Phương pháp nhãn nhiễu / làm sạch nhãn | 3 / 4 | đủ |
| Đầu độc nhãn trên NIDS / malware | 0 / 6 | **<3** |
| Đầu độc ngữ cảnh ICL / mô hình nền dạng bảng | 3 / 7 | đủ |
| Chứng nhận độ bền trước đầu độc | 1 / 4 | **<3** |
| Kiểm toán nguồn / đánh giá chất lượng người gán nhãn | 1 / 6 | **<3** |
| Ảnh hưởng mẫu / định giá dữ liệu | 0 / 3 | **<3** |
| Phương pháp đánh giá (tiền đăng ký, phương sai) | 4 / 4 | đủ |
| Thống kê (kiểm định, bootstrap khối) | 5 / 5 | đủ |

## Nhóm dưới 3 tài liệu đã kiểm chứng, và tài liệu cần mở (chỉ tiêu đề, [TO OPEN])

Tiêu đề dưới đây chọn từ hiểu biết của tôi, chưa mở trang nguồn; không phải tài liệu đã xác minh. Mục *(đã có STUB)* là công trình đã được kiểm toán nhưng thiếu bib.

- **Chi phí suy luận của mô hình nền dạng bảng (1):** [TO OPEN] đo thời gian/bộ nhớ của TabPFN v2 và TabICL trong bản gốc (`hollmann2025`, `qu2025tabicl` đã có, cần đọc phần chi phí); báo cáo kỹ thuật `kong2026tabfm` (phần chi phí suy luận).
- **Mô hình nền dạng bảng cho IDS (1):** [TO OPEN] các đánh giá TabPFN/TabICL trên bộ dữ liệu xâm nhập khác ngoài `garcia2025` (tìm kiếm chưa thực hiện).
- **Chọn/truy xuất ngữ cảnh:** *(đã có STUB)* `thomas2024localpfn`, `abdullah2026ctxsamp`, `ipas2026lucos`, `ma2024tabdpt` cần mở lại.
- **Replay trong học liên tục:** *(đã có STUB)* `amalapuram2023ecbrs`, `aljundi2019mir`, `bang2021rainbow`, `shim2021aser`, `mai2022survey`; thêm [TO OPEN] "Experience replay for continual learning" (Rolnick et al., NeurIPS 2019); "A continual learning survey: Defying forgetting in classification tasks" (De Lange et al., TPAMI 2022).
- **Khai thác mẫu âm khó (0 đã kiểm chứng):** *(đã có STUB)* `felzenszwalb2010` (đọc phương pháp), `shrivastava2016ohem` (đọc phương pháp), `xuan2020hard`, `serra2025uncertainty`; thêm [TO OPEN] bài gốc Sung & Poggio 1998 (PRIOR_ART_1 chưa đọc, chỉ qua OHEM/Felzenszwalb).
- **Học liên tục cho IDS (1):** *(đã có STUB)* `amalapuram2023ecbrs`, `zhang2025ssf`, `faber2022active`; `ariffin2026` đã mở.
- **Giảm lỗi kỳ vọng (1) và active learning gắn với mô hình nền dạng bảng (0):** [TO OPEN] "Bayesian active learning for classification and preference learning" (Houlsby et al., 2011); "Deep Bayesian active learning with image data" (Gal et al., ICML 2017); *(đã có STUB)* `treerath2026tabaicl` (NOVELTY_AUDIT_2).
- **Lỗi nhãn của bộ dữ liệu NIDS (2):** [TO OPEN] "Toward generating a new intrusion detection dataset and intrusion traffic characterization" (Sharafaldin et al., ICISSP 2018) làm nguồn gốc CIC-IDS-2017/2018; thêm công trình về nhãn của ToN_IoT/UNSW-NB15 nếu có (chưa tìm).
- **Phương pháp nhãn nhiễu (4, đủ), nhưng thiếu khảo sát:** [TO OPEN] "Learning from noisy labels with deep neural networks: A survey" (Song et al., TNNLS 2023); "Learning with noisy labels" (Natarajan et al., NeurIPS 2013).
- **Chứng nhận độ bền:** chỉ `jia2022knn` đọc phương pháp; `rosenfeld2020`, `levine2021dpa`, `steinhardt2017` mới đọc tóm tắt. [TO OPEN] khảo sát "Dataset security for machine learning: Data poisoning, backdoor attacks, and defenses" (Goldblum et al., TPAMI 2023); cần đọc lại các công trình đã có.
- **Kiểm toán nguồn:** `dawid1979`, `zhang2025peer`, `cao2022fltrust` là provisional. [TO OPEN] toàn văn Dawid–Skene; "Learning from crowds" (Raykar et al., JMLR 2010); "Peer prediction"/correlated agreement (Shnayder et al., 2016) — chưa mở được trong lần trước.
- **Ảnh hưởng mẫu / định giá dữ liệu (0):** tất cả mới đọc tóm tắt (`ghorbani2019`, `jia2019knnshap`, `pruthi2020`); [TO OPEN] "Understanding black-box predictions via influence functions" (Koh & Liang, ICML 2017).
- **Đầu độc NIDS/malware và ICL:** `lan2025`, `dolejs2026`, `ariffin2026` đã đọc một phần; malware mới tìm hai lượt, chưa đầy đủ. [TO OPEN] "Poisoning attacks against support vector machines" (Biggio et al., ICML 2012).
- **Tài liệu RQ2/RQ3 thiếu bib:** 55 STUB trong `REVIEW_REFS_STATUS.csv` (48 từ PRIOR_ART_1, 7 từ NOVELTY_AUDIT_2); cần `rq2_REFS_v2.bib`/`REFS.bib` để chuyển thành mục đầy đủ.
- **Tên "Vejling" và "Xu" trong đề cương RQ4 ([34],[35]):** chưa xác định (xem REPORT trước). PRIOR_ART_1 có hai công trình tác giả đầu "Xu" (`xu2024mixturepfn`, `xu2026coreset`); chưa biết có phải [35] hay không.

## Tổng số
- Khóa trong thư mục gộp: 144; đã kiểm chứng (OK/FIX/OK opened): 57; provisional: 30; STUB: 55; khác ([VERIFY]/NOT_FOUND): 2.
