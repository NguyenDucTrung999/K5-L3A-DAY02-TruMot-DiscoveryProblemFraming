# Báo cáo cá nhân — 2A202603402_DoMinhHieu

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Đỗ Minh Hiếu
- MSSV: 2A202603402
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: tru-mot
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

-

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
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: tra tay địa chỉ → tên cửa hàng → mã chuẩn trên emap/FamilyMart (Google/DeepL, đôi khi Google Maps). Số phút **chưa đo** |
| Impact (nếu không giải thì sao) | **8–18 lượt/ngày** (user-stated, `SCOPE.md`); phút/lượt **chưa đo** |
| Success metric (baseline → target) | Lượt tra tay/ngày: 8–18 → ≤ 4 (đề xuất, chưa phải số đo); đo bằng số dòng trong danh sách "cần bạn" của `daily.py` |
| Phương án không dùng AI | Rule: API tra cửa hàng của 7-11/Fam + chấm điểm theo đường/số nhà + bảng alias mã cũ. **Đã xây và đo** |
| Giả thuyết về AI (nếu có) | LLM chỉ dịch địa chỉ chữ Latin sang tiếng Hoa để Rule tra tiếp; người duyệt kết quả |
| Cảm nhận nhanh | Rule là chính, Workflow có một bước AI cho phần dư |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 7 bước, tổng thời gian: 

[1 Export KiotViet: chưa đo] → [2 GAS làm sạch: tự động]
→ [3 Tra tay cửa hàng: 8–18 lượt/ngày] ← BOTTLENECK
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
| Bottleneck (bước nào, mất bao nhiêu phút) | Phát hiện lỗi sau khi upload (mã cửa hàng, SĐT). Số phút **chưa đo** |
| Impact (nếu không giải thì sao) | 17,1–21,4% dòng bị từ chối mỗi lô (3 ngày: 10-03, 10-04, 10-05) |
| Success metric (baseline → target) | 17,1–21,4%/lô (3 ngày) → lỗi phòng được trước upload = 0 (target là mục tiêu đề xuất) |
| Phương án không dùng AI | Rule: kiểm trước khi upload (SĐT, ký tự cấm, hạn mức, chia kiện) |
| Giả thuyết về AI (nếu có) | Chưa có |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:

```text
Chưa vẽ riêng; dùng bước 5–7 của quy trình ở Card #1.
Thời gian từng bước:
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi đồng nghiệp nhắn Zalo nhờ lên gấp một đơn, tôi muốn đơn đó đi ngay trong ngày, để khách không phải chờ lô hôm sau |
| Actor | Đồng nghiệp (3–5 người), người vận hành |
| Thời điểm / bối cảnh | Trong ngày, khi đồng nghiệp nhắn Zalo |
| Quy trình hiện tại (3–7 bước) | Chưa vẽ |
| Bottleneck (bước nào, mất bao nhiêu phút) | Phải ngồi canh Zalo. |
| Impact (nếu không giải thì sao) | Khách phải chờ lô hôm sau. |
| Success metric (baseline → target) | Baseline |
| Phương án không dùng AI | Chưa ghi |
| Giả thuyết về AI (nếu có) | Chưa đủ dữ kiện; rủi ro ban tài khoản Zalo |
| Cảm nhận nhanh | Agent, nhưng chưa đủ dữ kiện nên không chọn |

Quy trình nháp hiện tại:

```text
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Actor rõ, quy trình vẽ được, impact đo bằng lượt/ngày, đã có benchmark
- Câu hỏi muốn nhóm phản biện:

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
| CP1 Scan | Nhờ AI đọc repo GAS (`orchestration/SCOPE.md`, `PROGRESS.md`, log chạy) và lập bảng 7 problem dạng Job Story kèm dấu hiệu thật | Tìm ra các con số thật nằm rải rác trong repo: 8–18 lượt tra tay/ngày, tỉ lệ từ chối upload 17,1–21,4% qua 3 ngày, 5 mã cửa hàng không tồn tại ngày 10-09 | Bảng do AI soạn từ tài liệu, **không phải do tôi tự scan trước** như đề yêu cầu. Ba dòng (#3 Zalo, #4 hủy đơn, #7 ghép CM) không có số phút, chỉ có mô tả | `[BẠN ĐIỀN: ý nào bạn viết lại theo trải nghiệm thật của mình; ý nào bạn bổ sung hoặc bỏ]`. Đã ghi rõ trong bảng dòng nào "chưa đo" thay vì để AI đoán số |
| CP2 Problem Card | Nhờ AI chọn top 3, viết Problem Card #1 và tóm tắt #2, #3; vẽ quy trình nháp hiện tại | Chọn bottleneck có số liệu nhất (tra tay `取件門市`), chỉ ra bước nghẽn và các phương án No AI / Rule | Số phút từng bước không có trong repo, nên các ô phút phải ghi "chưa đo". AI chọn card #3 (Zalo) nhưng chính nó cũng thừa nhận chưa đủ dữ kiện | `[BẠN ĐIỀN: bạn có đồng ý với thứ hạng top 3 không? Nếu bạn nhớ số phút thật mỗi lượt tra tay thì điền]`. Giữ "chưa đo" cho đến khi bấm giờ thật |
| CP4 Research | Chưa dùng AI | | | Chưa làm. Chưa phỏng vấn ai, chưa tìm công cụ tương tự, nên chưa ghi link nào |
| CP5 Quy trình | Nhờ AI vẽ quy trình trước/sau từ code `daily.py`, `fill_template.py`, `validate.py` | Phân bước nào Rule, bước nào AI, bước nào người; đối chiếu được với những gì đã chạy thật ngày 10-09 (132 đơn, 10 dòng cần người) | Phiên đầu ghi nguồn benchmark là "session 5" mà không kiểm lại; bước đọc file kết quả (Phase 3b) trong repo **chưa xây** nhưng bản đầu dễ đọc như đã có | AI tự rà lại và sửa nguồn thành "benchmark 10-03", đánh dấu bước 7 là **CHƯA XÂY**. Đây là sửa của AI, không phải của tôi. `[BẠN ĐIỀN: bạn đã kiểm lại điều gì trong quy trình này?]` |
| CP5–6 Problem Statement | Nhờ AI viết Problem Statement v0 rồi v1 | Tách được v0 và v1 với lý do đổi rõ ràng (thêm "chọn nhầm = 0" vì chọn nhầm cửa hàng tệ hơn để trống) | Mục tiêu "≤ 4 lượt/ngày" và các ngưỡng dừng là con số **AI đề xuất**, không phải số đo; metric thời gian chưa có baseline | AI đã gắn nhãn "đề xuất" cho các số này. `[BẠN ĐIỀN: bạn chấp nhận, đổi số nào, và vì sao]` |
| CP6 Mức can thiệp / quyết định | Nhờ AI so sánh 4 mức, chấm 4 rủi ro, đề xuất quyết định "Go, phạm vi nhỏ" | Lý do không chọn mức đơn giản hơn dựa trên số thật (benchmark còn 3 dòng dư đều là chữ Latin; ngày 10-09 có 4/10 dòng cần người là chữ Latin) | Quyết định "Go" là đề xuất của AI khi chưa có số phút tiết kiệm được (Value chấm "Trung bình" chỉ dựa trên số lượt/ngày). Chính sách gửi địa chỉ khách cho Gemini chưa được kiểm tra | `[BẠN ĐIỀN: bạn có đồng ý Go không? Nếu chính sách dữ liệu không cho phép thì quyết định đổi thế nào]` |
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
