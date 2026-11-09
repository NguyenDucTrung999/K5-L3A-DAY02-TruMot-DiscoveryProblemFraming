# Báo cáo cá nhân — 2A202603402_DoMinhHieu

## 1. Thông tin học viên

- Họ tên: Đỗ Minh Hiếu
- MSSV: 2A202603402
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Trừ Một
- Link repo nhóm: https://github.com/NguyenDucTrung999/K5-L3A-Day02-tru_mot-DiscoveryProblemFraming

---

**Nhân vật:** người vận hành một bàn xử lý đơn phía Đài Loan cho shop Việt Nam. Đơn đến từ KiotViet, được làm sạch trong Google Sheet bằng Google App Script, rồi upload lên hệ thống 7-ELEVEN (賣貨便) và FamilyMart (好賣+) để khách nhận hàng tại cửa hàng tiện lợi. Trung bình xử lý khoảng 80–90 đơn/ngày.

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi khách ghi địa chỉ bằng tiếng Việt/Anh/Trung phồn thể lẫn lộn hoặc gửi ảnh (không có copyable text), tôi muốn biết đúng cửa hàng khách muốn nhận, để ô `取件門市` (tên cửa hàng) không bị trống | Người vận hành, khách hàng | 10–20% trong 80–90 đơn/ngày = 8–18 lượt tra tay/ngày |
| 2 | Tốn thời gian | Khi vừa upload file đơn lên sàn, tôi muốn biết trước dòng nào sẽ bị từ chối do vi phạm định dạng của sàn, để không phải sửa rồi upload lại | Người vận hành | Rate từ chối trung bình khoảng 17-22% mỗi first upload |
| 3 | Pain từ người khác | Khi đồng nghiệp nhắn Zalo nhờ lên gấp một đơn, tôi muốn đơn đó đi ngay trong ngày, để khách không phải chờ lô hôm sau | Đồng nghiệp (3–5 người), khách | Tần suất khoảng 5-10 đơn mỗi ngày, vào các thời điểm ngẫu nhiên phát sinh |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi đơn có ghi chú đặc biệt như "2 kiện" hoặc thanh toán một phần, tôi muốn số tiền mỗi kiện được chia đúng, để không bị từ chối.| Người vận hành | 10-09: 1 đơn chia 2 kiện bị bỏ sót khi làm tay (500+418=918); 1 đơn bị giữ lại vì >20.000 trên một kiện  |
| 5 | Tốn thời gian | Khi mã cửa hàng là mã cũ hoặc đã đóng, tôi muốn lấy được mã hiện hành để không bị từ chối | Người vận hành | Rate khoảng 20% số đơn mỗi ngày bị từ chối, yêu cầu user sửa tay mới cho phép reupload |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận file kết quả upload, tôi muốn ghép mã đơn với mã vận đơn tự động, để không dán tay | Người vận hành | Bước này đã tự động một phần bằng userscript, vẫn cần user input raw data thay vì tự động crawl trực tiếp từ sàn |
| 7 | Tốn thời gian | Khi phòng sale tạo đơn sai thông tin và script failed với các đơn này, tôi muốn có phương thức recheck trước khi upload | Người vận hành | Khoảng 3-4 đơn bị nhầm mỗi ngày cần check thủ công |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- AI gợi ý thêm một problem: khi hủy đơn nội bộ trong KiotViet, tôi muốn tồn kho bị giữ được trả lại để không kẹt hàng (bước hủy tự động báo "không thấy nút hủy" 3 ngày liên tiếp 10-07, 10-08, 10-09). Tôi bỏ ý này vì quy trình hủy đơn đó đã deprecated theo thực tế vận hành ở công ty.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | #1 Tra tay cửa hàng cho dòng `取件門市` trống | Actor rõ, quy trình vẽ được, impact đo bằng lượt/ngày, đã có benchmark | Số phút mỗi lượt tra tay chưa đo |
| 2 | #2 Dòng bị từ chối khi upload | Có 3 ngày số liệu thật, 8/12 và 8/13 lỗi phòng được trước | Nhóm lỗi `商品` (từ cấm) không có quy luật, không giải được |
| 3 | #3 Đơn gấp từ Zalo | Pain thật theo lời user | Chưa có số liệu tần suất; rủi ro ban tài khoản Zalo |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi khách ghi địa chỉ bằng tiếng Việt/Anh/Hoa lẫn lộn hoặc gửi ảnh, tôi muốn biết đúng cửa hàng khách muốn nhận, để ô `取件門市` không bị trống |
| Actor | Người vận hành bàn xử lý đơn |
| Thời điểm / bối cảnh | Mỗi sáng, sau khi export đơn `Phiếu tạm` từ KiotViet, trước khi upload |
| Quy trình hiện tại (3–7 bước) | 7 bước: (1) Export đơn từ KiotViet; (2) GAS làm sạch trong Sheet; (3) Tra tay cửa hàng cho dòng trống; (4) Điền template chính thức của sàn; (5) Upload lên 賣貨便 / 好賣+; (6) Đọc kết quả, tìm dòng bị từ chối; (7) Sửa tay dòng lỗi, upload lại, ghi mã về KiotViet |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: tra tay địa chỉ → tên cửa hàng → mã chuẩn trên emap/FamilyMart (Google/DeepL, đôi khi Google Maps). Số phút khoảng 3-4'/đơn |
| Impact (nếu không giải thì sao) | **8–18 lượt/ngày**, tổng khoảng 30-90 phút đối chiếu |
| Success metric (baseline → target) | Lượt tra tay/ngày: 8–18 → ≤ 4 theo kinh nghiệm làm việc |
| Phương án không dùng AI | Rule: API tra cửa hàng của 7-11/Fam + chấm điểm theo đường/số nhà + bảng alias mã cũ. **Đã xây và đo** |
| Giả thuyết về AI (đã có) | LLM chỉ dịch địa chỉ chữ Latin sang tiếng Hoa để Rule tra tiếp; người duyệt kết quả |
| Cảm nhận nhanh | Rule là chính, Workflow có một bước AI cho phần dư |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 7 bước, tổng thời gian: chưa đo (riêng bước 3: khoảng 30-90 phút/ngày tùy khối lượng)

[1 Export KiotViet: chưa đo] → [2 GAS làm sạch: tự động]
→ [3 Tra tay cửa hàng: 3–4 phút/lượt, 8–18 lượt/ngày] ← BOTTLENECK
→ [4 Điền template: chưa đo] → [5 Upload: chưa đo]
→ [6 Đọc lỗi: chưa đo, 17,1–21,4% dòng bị từ chối]
→ [7 Sửa + upload lại + ghi mã về KiotViet: chưa đo]
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi vừa upload file đơn lên sàn, tôi muốn biết trước dòng nào sẽ bị từ chối, để không phải sửa rồi upload lại |
| Actor | Người vận hành |
| Thời điểm / bối cảnh | Sau khi điền template, ở bước upload lên sàn (cùng quy trình hiện tại ở Card #1) |
| Quy trình hiện tại (3–7 bước) | Bước 5–7 của quy trình ở Card #1: upload → đọc kết quả, tìm dòng bị từ chối → sửa tay và upload lại |
| Bottleneck (bước nào, mất bao nhiêu phút) | Phát hiện lỗi sau khi upload (mã cửa hàng, SĐT). Số phút: khoảng 30 phút đối chiếu, +- 10 tùy khối lượng |
| Impact (nếu không giải thì sao) | 17,1–21,4% dòng bị từ chối mỗi lô |
| Success metric (baseline → target) | 17,1–21,4%/lô → lỗi phòng được trước upload = 0 (target là mục tiêu đề xuất) |
| Phương án không dùng AI | Rule: kiểm trước khi upload (SĐT, ký tự cấm, hạn mức, chia kiện) |
| Giả thuyết về AI (nếu có) | Chưa có |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — bước 5–7 của quy trình ở Card #1

[5 Upload lên 賣貨便 / 好賣+: chưa đo]
→ [6 Đọc kết quả, tìm dòng bị từ chối: chưa đo, 17,1–21,4% dòng bị từ chối] ← BOTTLENECK (lỗi chỉ lộ ra sau upload)
→ [7 Sửa tay dòng lỗi, upload lại, ghi mã về KiotViet: chưa đo]

Tổng bước 6–7: khoảng 30 ± 10 phút 
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi đồng nghiệp nhắn Zalo nhờ lên gấp một đơn, tôi muốn đơn đó đi ngay trong ngày, để khách không phải chờ lô hôm sau |
| Actor | Đồng nghiệp (3–5 người), người vận hành |
| Thời điểm / bối cảnh | Trong ngày, khi đồng nghiệp nhắn Zalo |
| Quy trình hiện tại (3–7 bước) | Đồng nghiệp nhắn Zalo nhờ lên gấp một đơn; Người vận hành phải canh Zalo, thấy tin mới xử lý (BOTTLENECK, khoảng 5–10 đơn/ngày, rải ngẫu nhiên); Đơn đi qua quy trình như Card #1 (bước 1–7); Nếu không kịp lô trong ngày thì khách chờ lô hôm sau. Số phút từng bước: nhanh, khoảng 2-3' |
| Bottleneck (bước nào, mất bao nhiêu phút) | Phải ngồi canh Zalo, tin đến ngẫu nhiên, có thể vừa xong 1 tin thì tin khác đến và quy trình các bước lặp lại. |
| Impact (nếu không giải thì sao) | Khách phải chờ lô hôm sau. |
| Success metric (baseline → target) | Automation fully - AI/Bot Zalo tự nhận thông tin và tạo đơn hàng chính xác ngay lập tức trong vòng 10 phút kể từ khi receive information, baseline tôi đặt ra từ kinh nghiệm thực tế |
| Phương án không dùng AI | Thiết kế phương án crawl thủ công trigger theo keyword cùng script, sẽ kém hơn LLM recognition |
| Giả thuyết về AI (nếu có) | Chưa đủ dữ kiện; rủi ro ban tài khoản Zalo |
| Cảm nhận nhanh | Agent, nhưng chưa đủ dữ kiện nên không chọn |


### Card muốn pitch nhất

- Card số: 1
- Vì sao: Actor rõ, quy trình vẽ được, impact đo bằng lượt/ngày, đã có benchmark
- Câu hỏi muốn nhóm phản biện: Tại sao không tích hợp nhiều agent từ nhiều vendor, mỗi agent 1 việc, vì mục đích cuối là tự động hóa hoàn toàn?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| "Đã giải 59/64 dòng (92%)" là số **gộp**, 38 dòng vốn đã có mã trong địa chỉ nên GAS cũng điền được | Đồng ý | Chuyển sang đo **số ròng** (`run_batch.py --baseline`) |
| Lấy mã điền tay làm "đáp án đúng" | Không đúng: 5/8 lỗi quan sát được là **mã điền tay sai** | Đo theo "đúng", không theo "giống người" |
| "Cứ có trong emap là upload được" | Không đủ: có trường hợp emap liệt kê nhưng sàn vẫn từ chối (cửa hàng tạm ngưng/đổi mã) | Xếp nhóm này vào "cần hỏi khách đổi cửa hàng" (D38) |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 Problem Card ở hàng 7–9 mục 2.1 của `group_report.md`: #7 tra tay cửa hàng cho dòng trống (8–18 lượt/ngày), #8 dòng bị từ chối khi upload (17,1–21,4% mỗi lô), #9 đơn gấp qua Zalo (khoảng 5–10 đơn/ngày) | Nhóm cho rằng hơi nội bộ và khó tiếp cận dù khá align với yêu cầu và đủ data |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: hỏi Trung (hàng 1): khách có thể bỏ qua những cửa hàng họ muốn ghé khi đi theo lộ trình cố định không; hỏi Lâm (hàng 5): AI phân biệt lỗi do nhà thầu thi công hay do cư dân làm xước bằng cách nào; hỏi Khoa (hàng 11): thời gian xử lý, token và giá cả | Nhóm đồng ý và chỉnh sửa cách diễn đạt cho chặt chẽ (bản hiện tại) |
| Nhận phản biện | Câu hỏi tôi nhận được: Trung (hàng 7): dùng AI thì tốc độ có nhanh bằng script không; Lâm (hàng 8): AI có đảm bảo bảo mật thông tin khách hàng không; Khoa (hàng 9): API bên thứ 3 của Zalo không hỗ trợ tài khoản cá nhân thì có nhận được thông tin khách hàng và tự orchestrate không | Tôi đã sửa gì: Cơ bản accept phản biện như một đóng góp cải thiện vì ý tưởng của tôi đến từ quy trình thực tế, nhưng có xem xét vấn đề bảo mật của AI và Zalo API |
| Gom cluster / cây OST | Điền bảng Cluster ở mục 2.2: gom 12 candidate thành 3 cụm A (phân loại, định tuyến thông tin), B (tìm đúng thông tin từ nhiều nguồn), C (soạn thảo và kiểm tra hồ sơ trước khi gửi) | Không đổi |
| Chọn candidate problem | Bài #7 của tôi được chấm 31/35, đứng thứ 2 sau #1 Vincom (35/35) ở bảng shortlist mục 2.4. Nhóm ghi lý do loại #7 là domain nội bộ, 3 thành viên còn lại hiểu ít (3/5). Tôi đồng thuận gác bài #7 để làm bài Vincom | Đồng ý với nhóm, như đã nói ở problem card, data nội bộ và process khó tiếp cận |
| Kiểm chứng / research | Làm mục 3.3 `group_report.md`: research 3 công cụ có sẵn là Google Maps (Indoor Maps, Popular times), Tripadvisor (Trips), ShopeeFood/GrabFood (Group Order), kèm link | Phát hiện ra gap: không có tính năng dung hòa sở thích nhóm |


---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI đọc repo GAS (log chạy công việc hiện tại) và lập bảng 7 problem dạng Job Story kèm dấu hiệu thật | Tìm ra các con số thật nằm rải rác trong repo | Ba dòng không có số phút, chỉ có mô tả | Tôi đã bổ sung lại quy trình đúng thực tế, và bỏ 1 dòng quy trình deprecated. Đã ghi rõ trong bảng dòng nào "chưa đo" thay vì để AI đoán số |
| CP2 Problem Card | Nhờ AI chọn top 3, viết Problem Card #1 và tóm tắt #2, #3; vẽ quy trình nháp hiện tại | Chọn bottleneck có số liệu nhất (tra tay `取件門市`), chỉ ra bước nghẽn và các phương án No AI / Rule | Số phút từng bước không có trong repo, nên các ô phút phải ghi "chưa đo". AI chọn card #3 (Zalo) nhưng chính nó cũng thừa nhận chưa đủ dữ kiện | Cá nhân tôi đánh giá Card 1 là bottleneck lớn, rồi mới đến 3. Giữ "chưa đo" cho đến khi bấm giờ thật |
| CP4 Research | Nhờ AI gợi ý 3 công cụ để research (Google Maps, Tripadvisor, ShopeeFood), gợi ý các chức năng cần so sánh, định dạng văn bản bảng 3.3 và push lên nhánh | Cung cấp thông tin cần thiết để viết mục 3.3 | Bản nháp của AI dựa vào nguồn cũ (blog Google 2016, thông cáo Tripadvisor 2018) và trang hướng dẫn Group Order của bản Malaysia. Hai trang AI không mở được (Tripadvisor AI Assistant lỗi 403, shopeefood.vn trống) nên không dùng. AI chưa xác nhận được Vincom có sơ đồ tầng trên Google Maps | Tôi tự viết lại nội dung các cột của bảng và thay đổi link nguồn |
| CP5 Quy trình | Nhờ AI vẽ quy trình trước/sau từ code | Phân bước nào Rule, bước nào AI, bước nào người; đối chiếu được với những gì đã chạy thật | Phiên đầu ghi nguồn benchmark là "session 5" mà không kiểm lại; bước đọc file kết quả (Phase 3b) trong repo **chưa xây** nhưng bản đầu dễ đọc như đã có | Đã kiểm tra và sửa lại cũng như sửa nguồn dữ liệu |
| CP5–6 Problem Statement | Nhờ AI viết Problem Statement v0 rồi v1 | Tách được v0 và v1 với lý do đổi rõ ràng (thêm "chọn nhầm = 0" vì chọn nhầm cửa hàng tệ hơn để trống) | Mục tiêu "≤ 4 lượt/ngày" và các ngưỡng dừng là con số **AI đề xuất**, không phải số đo; metric thời gian chưa có baseline | AI đã gắn nhãn "đề xuất" cho các số này. |
| CP6 Mức can thiệp / quyết định | Nhờ AI so sánh 4 mức, chấm 4 rủi ro, đề xuất quyết định "Go, phạm vi nhỏ" | Lý do không chọn mức đơn giản hơn dựa trên số thật (benchmark còn 3 dòng dư đều là chữ Latin; ngày 10-09 có 4/10 dòng cần người là chữ Latin) | Quyết định "Go" là đề xuất của AI khi chưa có số phút tiết kiệm được (Value chấm "Trung bình" chỉ dựa trên số lượt/ngày). Chính sách gửi địa chỉ khách cho Gemini chưa được kiểm tra | Đồng ý với AI mục này |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Tôi thấy các bạn có ý tưởng rất hay, sáng tạo mà tôi chưa nghĩ đến. Các vấn đề đặt ra nghe tưởng đơn giản nhưng đằng sau là lý do thuyết phục, đều hướng đến một tệp đối tượng nhất định. Vd Trung có ý tưởng về app gợi ý route + quán, nghe có vẻ không cần thiết nhưng Trung có lý do khá hay. 

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Cũng đã có một vài ý tưởng kiểu "tạo vấn đề bán giải pháp", nhưng qua phản biện thì nhóm đã điều chỉnh lại cách tiếp cận để làm rõ vấn đề hiện hữu rồi mới suggest giải pháp. Ban đầu Lâm cho rằng cần AI để xử lý đơn khiếu nại, thực tế thì lượng đơn khiếu nại không nhiều và cũng không phức tạp đến mức cần AI. 

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Có. Problem #9 về Zalo ban đầu tôi chưa nghĩ đến rủi ro bảo mật thông tin và khóa tài khoản từ việc sử dụng unofficial API. Tôi đã nghĩ rằng cứ nhiều người dùng thì mặc nhiên mình cũng dùng được. Nghe phản biện tôi đã thấy đây là vấn đề cần address rõ ràng

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Không quá bất ngờ, vì một tiêu chí chính trong tìm quán ăn uống luôn là giá cả nên việc người được phỏng vấn nhạy cảm về giá là điều bình thường mà cá nhân tôi đã dự đoán trước. 

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Success Metric. Tiêu chí đưa ra cần short and concise nhưng vấn bao quát được core issue. 

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Tôi sẽ giải thích kỹ hơn cho nhóm về pipeline hiện tại vì điểm đánh giá hiểu domain chỉ có 3/5. Tôi cũng muốn phản biện thêm với topic chính của Trung về việc "có thực sự cần đến 1 app hỗ trợ việc di chuyển ăn uống trong TTTM không khi đi chơi hay ăn uống nên được tự do quyết định và đồng thuận chung thay vì nhận gợi ý từ trí tuệ nhân tạo?" 


**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
Nhìn chung bài này muốn học viên biết cách đặt vấn đề và quy trình tìm giải pháp cho vấn đề đó, bằng các tiêu chí cụ thể đã được học thuật hoặc thực tế chứng minh, có đặt giới hạn nghiên cứu và lĩnh vực và xem xét tính khả thi cũng như tính hợp lý của cả quy trình. Cần access xem liệu vấn đề này có thực sự xứng đáng cần hỗ trợ của AI trên các thang đo về chi phí, khả năng, mức độ interfere, hay fallback về predetermined, hardcoded script. 

Plan của nhóm đánh vào pain point là thời gian bỏ ra để quyết định, nhưng phỏng vấn tìm ra pain point chính là giá cả và preferences. Quy trình 5 bước từ bàn luận đến tra map, chốt địa điểm, tìm đường, sau này bổ sung thêm các input về preferences để personalized gợi ý. Dự kiến mục tiêu thống nhất trong 2 phút, trong phạm vi budget, tỉ lệ hài lòng trên 90%. AI sẽ chỉ gợi ý và không thao tác gì thêm trên thiết bị của user, và powered by LLM nhằm thực hiện mục tiêu cốt lõi là chỉ gợi ý trên những context đã có về nhóm. Nhóm quyết định GO, thí điểm trước một thời gian và theo dõi metric trước khi có quyết định tiếp theo. 

---

## 7. Tài liệu tham khảo

Nguồn dùng cho mục 3.3 của `group_report.md`:

- Google Maps: [Indoor maps, sơ đồ tầng](https://support.google.com/maps/answer/2803784)
- Google Maps: [Indoor maps, nơi có hỗ trợ](https://support.google.com/product-documentation/answer/1685827)
- Google Maps: [Popular times, thời gian chờ](https://support.google.com/business/answer/6263531)
- Google: [Blog về độ đông và thời gian ở lại](https://blog.google/products-and-platforms/products/search/know-you-go-google/)
- Tripadvisor: [App Store, tính năng Trips](https://apps.apple.com/gb/app/id284876795)
- ShopeeFood: [App Store VN](https://apps.apple.com/vn/app/shopeefood-%E1%BB%A9ng-d%E1%BB%A5ng-giao-m%C3%B3n/id1137866760?l=vi)
- GrabFood: [Giới thiệu Group Order](https://www.grab.com/vn/en/campaign/gioi-thieu-tinh-nang-dat-don-nhom-group-order-cua-grabfood/)
