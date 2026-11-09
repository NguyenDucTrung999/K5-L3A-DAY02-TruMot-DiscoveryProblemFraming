# Báo cáo cá nhân — 2A202603364_TranDangKhoa

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:Trần Đăng Khoa
- MSSV:2A202603364
- Email trường (không bắt buộc, repo có thể để public):26ai.khoatd2@vinuni.edu.vn
- Tên nhóm: tru_mot
- Link repo nhóm:https://github.com/NguyenDucTrung999/K5-L3A-Day02-tru_mot-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận một bài lab gồm nhiều file hướng dẫn, tôi muốn xác định thứ tự thực hiện và đầu ra cá nhân cần nộp, để bắt đầu đúng việc và không bỏ sót yêu cầu. | Học viên mới tiếp cận lab trên GitHub | Trong cuộc trò chuyện chuẩn bị lab, Khoa đã yêu cầu giải thích lại và hướng dẫn từng bước sau khi nhận link. Có 1 trường hợp tự thuật; chưa bấm giờ, chưa có bằng chứng về các học viên khác. |
| 2 | Tốn thời gian | Khi cần ôn lại một thao tác trong video bài học, tôi muốn tìm đúng đoạn giảng, để tiếp tục làm bài mà không phải xem lại toàn bộ video. | Người học khóa online có video ghi hình | Có dự án DeepRecall mô tả khó khăn tương tự [3]. Chưa xác nhận khóa học hiện tại có video và chưa có trải nghiệm của Khoa được cung cấp. |
| 3 | Lặp lại | Khi cần sử dụng tài liệu đã được gửi trong nhóm chat, tôi muốn tìm đúng đường dẫn và phiên bản đang dùng, để tiếp tục công việc mà không phải hỏi lại. | Thành viên nhóm học tập hoặc làm việc | Chuyển thể từ hướng tìm thông tin trong bài mẫu [2]. Chưa có tình huống thật hoặc thời gian đo của Khoa. |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi chuẩn bị ứng tuyển một vị trí, tôi muốn đối chiếu yêu cầu công việc với kinh nghiệm đã có trong CV, để bổ sung phần trình bày còn thiếu mà vẫn đúng sự thật. | Người tìm việc | Dự án Match! có bối cảnh tương tự [4]. Chưa phỏng vấn người tìm việc và chưa xác nhận đây là khó khăn cá nhân. |
| 5 | Tốn thời gian | Khi tổng kết chi phí chuyến đi chung, tôi muốn biết từng khoản chi, người trả và người tham gia, để tính phần tiền mỗi người rõ ràng. | Người quản lý tiền nhóm đi chơi | Đề xuất mở rộng từ bài toán ghi nhận hóa đơn của Receipt [5]. Chưa có hóa đơn, số người hoặc thời gian tổng hợp thực tế. |


**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Khó xác định việc cần làm khi nhận đề lab nhiều file | Có dấu hiệu trực tiếp trong cuộc trò chuyện; có thể hỏi học viên ngoài nhóm và kiểm tra câu trả lời với đề gốc. | Khó vì tài liệu phân tán, thuật ngữ mới hay chưa quen GitHub? |
| 2 | Khó tìm đoạn cần xem lại trong video học | Quy trình hẹp, thời gian tìm kiếm đo được. | Khóa có bản ghi không? Video đã có mục lục, phụ đề hoặc tìm kiếm chưa? |
| 3 | Khó tìm đúng tài liệu trong nhóm chat | Có thể khảo sát bằng một nhiệm vụ tìm đường dẫn cụ thể. | Nhóm đã ghim link hoặc có thư mục chung chưa? Tần suất có đủ lớn không? |

### Problem Card #1
| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận bài lab gồm nhiều file, tôi muốn xác định thứ tự làm và đầu ra cá nhân cần nộp, để bắt đầu đúng việc và không bỏ sót yêu cầu. |
| Actor | Học viên mới tham gia bài lab trên GitHub. |
| Thời điểm / bối cảnh | Sau khi nhận link đề, trước khi bắt đầu báo cáo cá nhân. |
| Quy trình hiện tại (giả thuyết) | Mở README → đọc checkpoints và quy định → tìm mẫu cá nhân → đối chiếu phần cá nhân/nhóm → ghi việc cần làm → hỏi lại điểm chưa rõ. |
| Bottleneck | Dự kiến ở bước đối chiếu các tài liệu để xác định đầu ra. Chưa đo số phút; cần phân biệt với khó khăn thao tác GitHub. |
| Impact | Có thể chậm bắt đầu hoặc bỏ sót mục cần nộp; chưa xác nhận mức ảnh hưởng. |
| Success metric | Baseline chưa đo. Đề xuất đo thời gian từ nhận đề đến lập đúng checklist. Target thử nghiệm: giảm ít nhất 30% thời gian so với baseline, đồng thời không bỏ sót mục bắt buộc. Target là đề xuất, chưa phải kết quả. |
| Phương án không dùng AI | Checklist một trang, gắn link tới từng mục nguồn và mẫu báo cáo. |
| Giả thuyết về AI | Tạo nháp checklist từ tài liệu đã cung cấp, dẫn nguồn từng yêu cầu; học viên đối chiếu và xác nhận. Không tự suy đoán quy định thiếu. |
| Cảm nhận nhanh | Ưu tiên thử No AI; chỉ cân nhắc Workflow nếu checklist tĩnh chưa đủ. |


Quy trình nháp hiện tại:

```text

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi quên một thao tác đã học, tôi muốn tìm đúng đoạn hướng dẫn trong video, để tự thực hiện lại thao tác. |
| Actor | Người học có quyền truy cập video ghi hình của khóa học. |
| Thời điểm / bối cảnh | Làm bài sau buổi học, cần ôn một thao tác cụ thể. |
| Quy trình hiện tại (giả thuyết) | Xác định nội dung → chọn video → tua hoặc tìm từ khóa → nghe kiểm tra ngữ cảnh → ghi mốc và thực hành. |
| Bottleneck | Chọn đúng đoạn trong video dài; chưa đo số phút. |
| Impact | Có thể mất thời gian tìm kiếm hoặc phải nhờ người khác chỉ lại; chưa có số liệu. |
| Success metric | Baseline chưa đo. Đề xuất giảm ít nhất 30% trung vị thời gian tìm đoạn trên các câu hỏi tương đương; ít nhất 4/5 lần tìm đúng đoạn được người học kiểm tra. |
| Phương án không dùng AI | Mục lục thời gian, ghi chú timestamp, tìm trong phụ đề có sẵn. |
| Giả thuyết về AI | Tìm đoạn liên quan từ bản chép lời có timestamp, trả link tới đoạn gốc; người học xem lại để xác minh. |
| Cảm nhận nhanh | Chưa biết; kiểm tra tính năng sẵn có trước, sau đó cân nhắc Workflow. |


Quy trình nháp hiện tại:

```text

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần tài liệu đã gửi trong nhóm chat, tôi muốn tìm đúng link và phiên bản hiện hành, để làm tiếp mà không phải hỏi lại. |
| Actor | Thành viên nhóm học tập hoặc làm việc nhỏ. |
| Thời điểm / bối cảnh | Một thời gian sau khi tài liệu được gửi, có thêm tin nhắn hoặc phiên bản mới. |
| Quy trình hiện tại (giả thuyết) | Nhớ tên tài liệu → tìm từ khóa → mở các link → kiểm tra nội dung/phiên bản → hỏi người gửi nếu chưa chắc → lưu link dùng tiếp. |
| Bottleneck | Phân biệt kết quả tìm kiếm và xác nhận phiên bản; chưa đo số phút. |
| Impact | Có thể làm theo tài liệu cũ hoặc gián đoạn người gửi; chưa xác nhận tần suất. |
| Success metric | Baseline chưa đo. Đề xuất giảm ít nhất 30% thời gian tìm đúng tài liệu; trong 5 lượt kiểm tra không chọn nhầm bản đã được xác nhận là cũ. |
| Phương án không dùng AI | Ghim một trang mục lục; quy ước đặt tên và người cập nhật link hiện hành. |
| Giả thuyết về AI | Tìm trong tập tài liệu được cho phép, trả đường dẫn và nguồn xác nhận phiên bản. Nếu chưa có nguồn xác nhận thì báo chưa rõ. |
| Cảm nhận nhanh | Ưu tiên No AI hoặc Rule; chưa có cơ sở chọn Agent. |


Quy trình nháp hiện tại:

```text

```

### Card muốn pitch nhất

- Card số: 1
- Vì sao:
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Một trường hợp chưa chứng minh vấn đề phổ biến. | Khoa cần tự xác nhận. | Ghi rõ chỉ có một trường hợp tự thuật; cần phỏng vấn ngoài nhóm. |
| Chưa có baseline nên không thể khẳng định tiết kiệm thời gian. | Khoa cần tự xác nhận. | Đánh dấu chưa đo; tách target đề xuất khỏi kết quả. |
| Công cụ sẵn có và checklist có thể đủ giải quyết. | Khoa cần tự xác nhận. | Thêm phương án No AI và thử trước khi chọn AI. |
| Quy trình tìm video và tài liệu chưa được quan sát. | Khoa cần tự xác nhận. | Gắn nhãn giả thuyết; cần sửa theo hành vi người thật. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
