# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Trừ Một
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Gợi ý lộ trình ăn uống và hoạt động giải trí theo ngân sách cho nhóm khách hàng tại TTTM Vincom Retail (Candidate #1).
- Quyết định cuối: Go / Not Yet / No-Go (sẽ chốt ở CP6)

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Nguyễn Đức Trung | Khi đến TTTM Vincom cuối tuần cùng nhóm bạn, tôi muốn có lộ trình gợi ý quán ăn và hoạt động phù hợp ngân sách, để không mất cả tiếng đắn đo và trễ giờ xem phim | Khách hàng nhóm bạn trẻ, gia đình | Bàn bạc, so sánh giá (20 phút) và tìm gian hàng giữa các tầng (15 phút). Tổng mất 50 phút | Khách hàng có thể bỏ qua (skip) những cửa hàng tiềm năng họ muốn ghé khi đi theo lộ trình cố định không, ví dụ bỏ qua quầy lưu niệm trên đường đi? (Hiếu hỏi) |
| 2 | Nguyễn Đức Trung | Khi trụ sạc xe điện gặp sự cố hỏng súng sạc, tôi muốn nhanh chóng tìm được trạm lân cận còn trụ trống tương thích, để tiếp tục ca chạy không trễ hẹn khách | Tài xế Xanh SM, điều phối viên vận hành | Tra cứu tọa độ GPS và trạng thái trụ sạc trống thủ công (tốn 8–10 phút/lượt) | Đã có nhiều công cụ và bản đồ hỗ trợ trạm sạc tồn tại rồi, liệu việc dùng AI ở đây có thực sự cần thiết không? (Lâm hỏi) |
| 3 | Nguyễn Đức Trung | Khi tiếp nhận phản ánh hư hỏng từ cư dân qua app, tôi muốn nhanh chóng phân loại đúng lĩnh vực kỹ thuật và phân khu, để giao việc cho đúng tổ phụ trách | Nhân viên trực ban BQL Vinhomes | Đọc hiểu mô tả dân dã và tra cứu lịch trực phân công thủ công (tốn 10 phút/phiếu) | Dữ liệu thông tin cá nhân và phản ánh sự cố của cư dân có được đảm bảo an toàn và bảo mật không? (Khoa hỏi) |
| 4 | Bùi Văn Lâm | Khi phát hiện sự cố hạ tầng/thiết bị trong căn hộ, tôi muốn thông tin được tiếp nhận và giao đúng kỹ thuật viên xử lý để sinh hoạt không bị gián đoạn và không phải gọi điện giục nhiều lần. | Cư dân khu đô thị (CSKH & Kỹ thuật BQL hỗ trợ) | Hàng đợi giờ cao điểm dồn ứ (chờ 10 phút) do CSKH phải đọc hiểu mô tả tự do, xem ảnh và gán việc thủ công (mất 9 phút/ticket). | "Nếu phần lớn sự cố là cơ bản thì dùng form dropdown hoặc Rule là đủ, tại sao cần AI?" (Trung) |
| 5 | Bùi Văn Lâm | Khi nhận bàn giao căn hộ hoặc yêu cầu bảo hành, tôi muốn các lỗi xây dựng được ghi nhận minh bạch và phân rõ trách nhiệm từng nhà thầu kèm hạn hoàn thành để sửa dứt điểm, không đùn đẩy trách nhiệm. | Cư dân nhận nhà (Kỹ sư BQL & Nhà thầu thi công) | Nhập liệu thủ công từ biên bản giấy punch list và đối soát gói thầu (55 phút/căn); tranh chấp trách nhiệm bảo hành kéo dài 3–5 ngày. | "Làm sao AI phân biệt được lỗi do thi công của nhà thầu hay do cư dân tự làm xước khi dọn đồ vào?" (Hiếu) |
| 6 | Bùi Văn Lâm | Khi gặp hành vi vi phạm nội quy chung (đỗ xe chắn lối, tiếng ồn đêm), tôi muốn gửi thông tin đến BQL và nhận được thông báo xử lý văn minh, đúng quy định để giữ môi trường yên tĩnh mà không phải cãi vã. | Chuyên viên CSKH BQL (Cư dân phản ánh & Cư dân vi phạm) | Soạn thảo văn bản nhắc nhở/xử phạt viện dẫn điều khoản nội quy thấu tình đạt lý mất 25 phút/văn bản. | "Văn bản AI soạn thảo có đủ khéo léo để không gây leo thang căng thẳng giữa cư dân với BQL không?" (Khoa) |
| 7 | Đỗ Minh Hiếu | Khi khách ghi địa chỉ bằng tiếng Việt/Anh/Hoa lẫn lộn hoặc gửi ảnh, tôi muốn biết đúng cửa hàng khách muốn nhận, để ô `取件門市 (địa chỉ)` không bị trống bằng AI | Người vận hành bàn xử lý đơn | Tra tay địa chỉ → mã cửa hàng chuẩn: 8–18 lượt/ngày (10–20% trong 80–90 đơn) | Dùng AI thì tốc độ có nhanh bằng script không? (Trung) |
| 8 | Đỗ Minh Hiếu | Khi vừa upload file đơn lên sàn, tôi muốn biết trước dòng nào sẽ bị từ chối, để không phải sửa rồi upload lại | Người vận hành | Chỉ phát hiện lỗi sau khi upload: 17,1–21,4% dòng bị từ chối mỗi lô | AI có đảm bảo bảo mật thông tin khách hàng? (Lâm) |
| 9 | Đỗ Minh Hiếu | Khi đồng nghiệp nhắn Zalo nhờ lên gấp một đơn, tôi muốn đơn đó tự động đi ngay trong ngày, human intervention minimal, để khách không phải chờ lô hôm sau | Đồng nghiệp (3–5 người), người vận hành | Phải ngồi canh Zalo; khoảng 5–10 đơn/ngày, rải ngẫu nhiên trong ngày | Vấn đề của API bên thứ 3 (Zalo) không hỗ trợ tài khoản cá nhân thì có nhận được thông tin khách hàng và orchestrate tool tự động không? (Khoa) |
| 10 | Trần Đăng Khoa | Khi nhận đề lab gồm nhiều file, tôi muốn biết thứ tự thực hiện và đầu ra cá nhân cần nộp, để bắt đầu đúng việc và không bỏ sót yêu cầu. | Học viên mới làm lab trên GitHub | Đối chiếu nhiều file để xác định việc cần làm và đầu ra; điểm nghẽn dự kiến, chưa đo thời gian. | Có nhiều bên làm rồi (Trung) |
| 11 | Trần Đăng Khoa | Khi cần ôn lại một thao tác đã học, tôi muốn tìm đúng đoạn hướng dẫn trong video, để tiếp tục thực hành. | Người học khóa online có video ghi hình | Tìm đúng đoạn trong video dài; điểm nghẽn dự kiến, chưa đo thời gian. | Thời gian xử lý và token, giá cả (Hiếu) |
| 12 | Trần Đăng Khoa | Khi cần tài liệu đã gửi trong nhóm chat, tôi muốn tìm đúng đường dẫn và phiên bản hiện hành, để tiếp tục công việc mà không phải hỏi lại. | Thành viên nhóm học tập hoặc làm việc | Đối chiếu kết quả tìm kiếm để xác nhận đúng tài liệu và phiên bản; điểm nghẽn dự kiến, chưa đo thời gian. | Cần personal AI cá nhân quản lý trong máy vì vấn đề bảo mật nhưng có vấn đề vì AI cá nhân không mạnh bằng AI cloud (Lâm) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A - Phân loại, định tuyến thông tin và dữ liệu | #3 thông tin phản ánh từ người dân, #4 sự cố căn hộ, #7 địa chỉ nhận hàng, #9 yêu cầu qua tin nhắn Zalo | Input là mô tả tự do (chữ viết, chữ đánh máy, hình ảnh), người tiếp nhận cần đọc hiểu và tra cứu để xử lý đúng nơi, đúng người nhận, đúng vấn đề. Bottleneck ở bước đọc hiểu và gán label thủ công. |
| B - Tìm đúng thông tin từ nhiều nguồn | #1 lộ trình tìm quán ăn, #2 trạm sạc trống, #10 đề lab nhiều file, #11 video hướng dẫn dài, #12 tài liệu trôi trong nhóm chat | Thông tin nằm rải rác ở nhiều nơi, người thực hiện phải tìm và nhận đúng nguồn mới nhất và đúng trạng thái. Bottleneck ở việc tra cứu thủ công dữ liệu. |
| C - Soạn thảo và kiểm tra hồ sơ trước khi gửi đi | #5 Văn bản yêu cầu, #6 văn bản nhắc nhở, #8 upload bị từ chối | Soạn thảo, kiểm tra văn bản đúng quy tắc mới gửi. Lỗi thường bị phát hiện muộn làm mất thời gian và có thể cả chi phí. |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian nhóm khách tại TTTM Vincom thống nhất địa điểm ăn uống và tìm đến nơi, đồng thời bảo đảm phù hợp ngân sách và không trễ hoạt động đã lên lịch.
├── Opportunity A: Nhóm khách khó thống nhất lựa chọn ăn uống khi các thành viên có sở thích và mức chi tiêu khác nhau.
├── Opportunity B: Nhóm khách mất công tìm và đối chiếu thông tin món ăn, giá cả để xác định lựa chọn phù hợp.
└── Opportunity C: Nhóm khách chưa quen vị trí gian hàng và đường di chuyển giữa các tầng, nên khó ước lượng thời gian đến nơi.
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- “Chatbot AI trên Zalo”: là lựa chọn công cụ. Nhu cầu cần làm rõ là tìm đủ thông tin và thống nhất lựa chọn phù hợp.
- “Màn hình cảm ứng tra cứu ở mọi tầng”: là phương án thiết bị. Nhu cầu cần làm rõ là xác định vị trí và đường đi.
- “Tự động thanh toán trên app”: là tính năng giao dịch; chưa có bằng chứng cho thấy thanh toán là điểm nghẽn trong phạm vi đang xét.


### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1. Lộ trình trải nghiệm TTTM Vincom (#1 - Trung) | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35** |
| 2. Tra tay địa chỉ nhận hàng Đài Loan (#7 - Hiếu) | 5 | 5 | 5 | 4 | 4 | 5 | 3 | **31** |
| 3. Tìm tài liệu và phiên bản trong nhóm chat (#12 - Khoa) | 4 | 3 | 4 | 3 | 3 | 4 | 5 | **26** |

**Dẫn chứng và nguồn số liệu cho từng candidate:**

- **Candidate 1 (TTTM Vincom):** 
  - Khảo sát "Food Indecision" của OnePoll: người dùng mất 16–20 phút/người để chọn món; đi nhóm tranh luận thêm 15 phút.
  - Nghiên cứu "The Paradox of Choice" (Barry Schwartz) & Khảo sát F&B của Q&Me: đối mặt với trên 40 gian hàng tại TTTM, hiện tượng tê liệt quyết định khiến người trẻ tốn 15–20 phút lướt mạng xã hội so sánh giá.
  - Đo lường thực tế: thời gian lên kế hoạch và tìm đường mất 45–60 phút (baseline trung bình 50 phút).
- **Candidate 2 (Xử lý đơn hàng Đài Loan - #7):**
  - Dữ liệu thực tế từ log vận hành shop hàng Đài Loan: nhật ký xử lý ngày 10-09 có 132 đơn, 10 dòng cần tra tay.
  - Tần suất: trung bình 80–90 đơn/ngày, tỷ lệ địa chỉ trống/lỗi chiếm 10–20% (tương đương 8–18 lượt tra tay/ngày). Tỷ lệ sàn từ chối first upload từ 17,1% đến 21,4%.
- **Candidate 3 (Tìm tài liệu nhóm chat - #12):**
  - Báo cáo khảo sát Microsoft Work Trend Index / McKinsey: nhân viên và học viên tốn trung bình 1,8 giờ/ngày (khoảng 10–15 phút/lần) để tìm kiếm thông tin và tài liệu nội bộ.
  - Trải nghiệm thực tế học viên: tin nhắn nhóm chat Zalo/Discord trôi nhanh, tài liệu chia sẻ qua nhiều phiên bản không rõ bản mới nhất.

**Candidate được chọn:**
Candidate #1 — Gợi ý lộ trình ăn uống và hoạt động giải trí theo ngân sách cho nhóm khách hàng tại TTTM Vincom Retail (do Nguyễn Đức Trung đưa ra).

**Vì sao chọn:**
1. **Tính phổ biến và vừa sức buổi lab (5/5):** Nỗi đau mất 30–50 phút bàn bạc, tranh cãi chọn quán ăn và tìm đường giữa các tầng khi đi đông người là trải nghiệm thực tế của 100% sinh viên và giới trẻ. Nhóm có thể triển khai phỏng vấn The Mom Test ngay lập tức với 5–10 sinh viên xung quanh mà không gặp rào cản truy cập hệ thống.
2. **Cả nhóm cùng hiểu sâu domain (5/5):** Tất cả 4 thành viên đều thường xuyên đi TTTM Vincom, nắm rõ các phân khúc ẩm thực, mức chi tiêu và hành vi tiêu dùng thực tế.
3. **So sánh rõ ràng 4 mức can thiệp AI:** Thể hiện rõ sự khác biệt giữa No AI (bảng chỉ dẫn tầng), Rule (bộ lọc theo giá và loại đồ ăn), Workflow (tổng hợp sở thích đa thành viên trong nhóm), và Agent (tự động đặt bàn và thanh toán).

**Vì sao loại các candidate còn lại:**
1. **Loại Candidate #7 (Chuẩn hóa địa chỉ TMĐT):** Bài toán phụ thuộc vào dữ liệu nội bộ và API sàn cross-border của một doanh nghiệp cụ thể (bạn Hiếu nắm rõ), 3 thành viên còn lại không hiểu sâu domain này (điểm hiểu domain chỉ đạt 3/5) nên khó cùng tham gia phản biện và bảo vệ đồ án.
2. **Loại Candidate #12 (Tìm tài liệu trong nhóm chat):** Bài toán tìm kiếm thông tin ngữ cảnh (RAG / Search) dễ bị trượt thành dự án quá lớn, quy trình tìm kiếm phụ thuộc vào từng nền tảng Zalo/Discord nên khó chuẩn hóa và khó đo lường impact chính xác trong thời gian ngắn của buổi lab.

**Xử lý bất đồng (nếu có):**
- *Diễn biến bất đồng:* Ban đầu bạn Lâm bảo vệ mạnh bài toán Vinhomes vì có cấu trúc ranh giới an toàn (Boundary) rất rõ; bạn Hiếu đề xuất bài toán TMĐT vì đã có sẵn dữ liệu lỗi thực tế; bạn Trung bảo vệ bài toán Vincom Retail vì tính đại chúng và khả thi kiểm chứng.
- *Cách giải quyết:* Nhóm thống nhất không tranh luận theo cảm tính mà sử dụng bảng chấm điểm 7 tiêu chí của Double Diamond. Khi đối chiếu tiêu chí "Vừa sức lab" và "Cả nhóm hiểu domain", bài toán Vincom Retail đạt điểm cao nhất (35/35 điểm). Bạn Lâm và bạn Hiếu đã đồng thuận gác lại bài toán riêng để tập trung toàn lực cùng nhóm triển khai bài toán Vincom cho các checkpoint tiếp theo.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 |Việc chọn chỗ ăn và tìm đường tại Vincom gây chậm trễ hoặc bất tiện đáng kể cho nhóm khách.| Value| 5 | 1 | Ưu tiên|
| 2 |Khác biệt về sở thích và ngân sách khiến nhóm khách khó thống nhất chỗ ăn.|Value |5 |1 |Ưu tiên |
| 3 |Khách mất công tìm và đối chiếu thông tin món ăn, giá cả trước khi quyết định. |Value |4 |1 |Ưu tiên |
| 4 |Khách chưa quen vị trí gian hàng nên mất thời gian tìm đường hoặc ước lượng sai thời gian di chuyển. |Value |4 |1 |Ưu tiên |
| 5 |Nhóm khách có thể xác định ngân sách, sở thích và giờ hẹn đủ rõ để sử dụng hỗ trợ lựa chọn. |Usability |4 |1 |Tìm hiểu sơ bộ |


*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn riêng 3 sinh viên từng đi Vincom cùng bạn bè, mỗi cuộc khoảng 10 phút. Thời gian chọn quán và tìm đường bên dưới là ước lượng theo hồi tưởng của các đối tượng phỏng vấn.

Interview snapshot - P1:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) |P1 - sinh viên, đi Vincom cùng nhóm 4 người, được phỏng vấn trực tiếp |
| Câu nói đáng nhớ nhất (nguyên văn) |“Tụi mình biết quán ở tầng nào rồi, nhưng người muốn ăn lẩu, người lại bảo đắt quá nên chưa chốt được.” |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |Trong một lần đi cuối tuần, nhóm đã mua vé xem phim nhưng chưa chọn chỗ ăn. Nhóm cân nhắc ba quán, đổi lựa chọn sau khi xem giá, cuối cùng phải ăn nhanh để kịp phim. |
| Hiện đang xử lý bằng cách nào (workaround)? |Một người tìm menu trên điện thoại, các bạn còn lại đề xuất quán. Nhóm chốt mức tiền mỗi người rồi chọn lại. |
| Mất bao lâu, bao lần? |Ước lượng khoảng 20 phút bàn bạc và tra giá, sau đó 5 phút đi đến quán. Hai hoạt động bàn bạc và tra giá diễn ra đồng thời. P1 nhớ có 2 trong 3 chuyến đi gần đây gặp tình huống tương tự. |
| Insight / opportunity rút ra |Trong trường hợp P1, khó khăn chính là thống nhất sở thích và ngân sách. Việc tìm đường không phải điểm nghẽn đáng kể. Cần kiểm tra nhu cầu thống nhất mức chi trước khi so sánh quán. |

Interview snapshot - P2:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) |P2 — sinh viên, đi Vincom cùng một người bạn. Phỏng vấn qua cuộc gọi. |
| Câu nói đáng nhớ nhất (nguyên văn) | “Tụi mình chọn quán từ ở nhà rồi, đến nơi thì cứ lên ăn thôi.” |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |Trong lần đi gần nhất, hai người chọn quán quen trước khi đến. Họ xem bảng chỉ dẫn và đến quán thuận lợi, không đổi kế hoạch. |
| Hiện đang xử lý bằng cách nào (workaround)? |Thống nhất quán qua tin nhắn trước chuyến đi; dùng bảng chỉ dẫn tầng tại trung tâm thương mại. |
| Mất bao lâu, bao lần? |Ước lượng 3 phút trao đổi trước chuyến đi và 5 phút tìm đến quán khi đã vào trung tâm thương mại. P2 không nhớ lần gần đây nào gặp khó khăn đáng kể khi chọn quán. |
| Insight / opportunity rút ra |P2 là tín hiệu phản bác giả định rằng mọi nhóm khách đều khó chọn quán hoặc tìm đường. Với người đã chọn quán quen từ trước, cách xử lý hiện tại có thể đã đủ. |

Interview snapshot - P3:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) |P3 — sinh viên, đi Vincom cùng nhóm 5 người. Phỏng vấn trực tiếp. |
| Câu nói đáng nhớ nhất (nguyên văn) | “Mọi người đồng ý ăn buffet, nhưng phải xem giá cuối tuần rồi mới biết có vừa tiền không.” |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |Nhóm thống nhất loại món khá nhanh nhưng phải kiểm tra giá của hai quán. Một hình menu tìm được không rõ còn áp dụng không, nên nhóm gọi hỏi quán trước khi quyết định. |
| Hiện đang xử lý bằng cách nào (workaround)? |Tìm menu trên trang của quán, gửi ảnh vào nhóm chat và gọi điện để xác nhận giá. |
| Mất bao lâu, bao lần? |Ước lượng 5 phút thống nhất loại món, 15 phút tìm và xác nhận giá, sau đó 5 phút đi đến quán. P3 nhớ rõ một lần này, còn lần khác thì không nhớ rõ. |
| Insight / opportunity rút ra |Với P3, điểm nghẽn là xác nhận giá đang áp dụng, không phải gặp bất đồng hay tìm đường. Thông tin giá có nguồn và thời điểm cập nhật rõ là nhu cầu cần tìm hiểu thêm. |


Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
|Phỏng vấn 3 người |3 người kể 3 chuyến đi khác nhau |P1 và P3 đều kể khó khăn trước khi chốt quán. P1 vướng thống nhất ngân sách và sở thích; P3 vướng xác nhận giá hiện tại của quán.|P2 đã chọn quán trước nên không gặp khó khăn đáng kể. Cả ba trường hợp đều không cho thấy tìm đường là điểm nghẽn chính. |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

Ban đầu, nhóm giả định cả việc chọn quán và tìm đường đều làm chuyến đi kéo dài. Trong 3 cuộc phỏng vấn, 2 người gặp khó ở bước chọn quán, còn việc di chuyển không được ghi nhận là trở ngại chính.

Trường hợp P2 cho thấy nếu chọn quán quen có thể không cần hỗ trợ gì mới. Tuy nhiên số người phỏng vấn còn ít, thời gian chỉ là nhớ lại, nên chưa đủ để kết luận mức độ phổ biến của vấn đề.


### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
