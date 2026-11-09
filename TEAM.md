# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Trừ Một
- Candidate problem nhóm chọn (1 câu): Gợi ý lộ trình ăn uống và hoạt động giải trí theo ngân sách cho nhóm khách hàng tại TTTM Vincom Retail (Candidate #1).
- Quyết định cuối (Go / Not Yet / No-Go): Go (Triển khai MVP pilot tại Vincom Mega Mall Smart City).

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Đức Trung | 2A202603423 | Nhóm trưởng, Điều phối chung | NguyenDucTrung999 |
| 2 | Bùi Văn Lâm | 2A202603400 | Phụ trách viết Problem Statement & Ranh giới AI | LamBui |
| 3 | Đỗ Minh Hiếu | 2A202603402 | Phụ trách kỹ thuật & quy trình | minhiuss |
| 4 | Trần Đăng Khoa | 2A202603364 | Phụ trách kiểm chứng & phản biện | khoatran134563-2k3 |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Cả nhóm | Trung điều phối | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Đỗ Minh Hiếu | Trần Đăng Khoa | Assumption map, snapshot hoặc survey |
| CP4 — Research | Đỗ Minh Hiếu | Nguyễn Đức Trung | Bảng research có link |
| CP5 — Quy trình trước/sau | Trần Đăng Khoa | Đỗ Minh Hiếu | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Bùi Văn Lâm | Nguyễn Đức Trung | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Đức Trung | Bùi Văn Lâm | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Đức Trung | Cả nhóm | 4 rủi ro + Go/Not Yet/No-Go + ngưỡng dừng |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenDucTrung-2A202603423

**Phần việc phụ trách:**

- Nhóm trưởng điều phối, hợp nhất mã nguồn Git, quản trị file nhật ký `AI_LOG_MR.md`.
- Xây dựng 10 problem scan và Top 3 Problem Cards cá nhân (Vincom Retail, Xanh SM, Vinhomes).
- Phụ trách hoàn thiện Gói 4 của nhóm: Mục 6 (Mức can thiệp AI: ma trận, so sánh 4 mức, AI Canvas, Google PAIR), Mục 7 (Problem Statement v1, tiêu chí eval, 10 test case eval mẫu cho Bonus B3), Mục 8 (4 rủi ro sản phẩm, quyết định Go, pilot nhỏ nhất, ngưỡng dừng), Mục 9 & 10 (Hạn chế, hướng tiếp theo và tài liệu tham khảo).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Khởi tạo quy chuẩn `AI_LOG_MR.md` cho toàn nhóm và thực hiện các lượt hợp nhất nhánh.
- Đóng góp 3 bài toán kèm câu hỏi phản biện tại mục 2.1 bảng Pitch của nhóm.
- Hoàn thiện toàn bộ Mục 6, 7, 8, 9, 10 trong báo cáo nhóm `group_report.md` đạt chuẩn Rubric.
- Xây dựng bộ dữ liệu 10 test case eval mẫu cho bước AI gợi ý lộ trình để đạt điểm Bonus B3 (+3 điểm).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File `report/individual/2A202603423_NguyenDucTrung.md` hoàn chỉnh từ Mục 1 đến Mục 7.
- Hàng 1-3 trong mục 2.1 của `report/team/group_report.md`.
- Toàn bộ Mục 6, 7, 8, 9, 10 của `report/team/group_report.md`.

**Điều mình học được từ phần nhóm:**

- Kỹ năng điều phối nhóm, hợp nhất nhánh Git và lắng nghe các góc nhìn phản biện đa chiều về bài toán thực tế; hiểu sâu sắc chuỗi logic từ xác định vấn đề, phân tích quy trình, đo lường metric, thiết lập ranh giới an toàn cho đến lựa chọn mức can thiệp AI phù hợp.

### BuiVanLam-2A202603400

**Phần việc phụ trách:**

- Viết Problem Statement (v0 và v1), thiết lập tiêu chí Eval và Boundary AI.
- Phân tích rủi ro & lựa chọn mức can thiệp (Rule vs Workflow vs Agent).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thiện báo cáo cá nhân với 10 problem scan và Top 3 Problem Cards chi tiết.
- Đóng góp luận điểm mô hình Hybrid Workflow và các ranh giới an toàn cho bài toán nhóm.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File `report/individual/2A202603400_BuiVanLam.md`.
- Hàng 4-6 trong mục 2.1 của `report/team/group_report.md`.

**Điều mình học được từ phần nhóm:**

- Hiểu sâu sắc về việc tránh bẫy "solution-first" và tầm quan trọng của việc xác lập ranh giới an toàn (Operational Boundary) khi đưa AI vào quy trình thực tế.

### DoMinhHieu-2A202603402

**Phần việc phụ trách:**

- Phụ trách kỹ thuật & quy trình.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thành báo cáo cá nhân với 10 problem scan và Top 3 Problem Cards.
- Đóng góp hàng 7-9 trong mục 2.1 của `report/team/group_report.md`.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File `report/individual/2A202603402_DoMinhHieu.md`.
- Hàng 7-9 trong mục 2.1 của `report/team/group_report.md`.

**Điều mình học được từ phần nhóm:**

- Đang cập nhật.

### TranDangKhoa-2A202603364

**Phần việc phụ trách:**

- Phụ trách kiểm chứng & phản biện.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thành báo cáo cá nhân với 10 problem scan và Top 3 Problem Cards.
- Đóng góp hàng 10-12 trong mục 2.1 của `report/team/group_report.md`.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File `report/individual/2A202603364_TranDangKhoa.md`.
- Hàng 10-12 trong mục 2.1 của `report/team/group_report.md`.

**Điều mình học được từ phần nhóm:**

- Đang cập nhật.
