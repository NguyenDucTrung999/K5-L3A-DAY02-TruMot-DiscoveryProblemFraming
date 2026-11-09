# Nhat ky sua file va gop nhanh vao main (AI & Merge Log)

> Quy tac: Moi khi bat ky thanh vien nao sua file bai nhom (report/team/group_report.md hoac TEAM.md) va yeu cau gop vao nhanh main, bat buoc phai copy khung mau duoi day, dien day du thong tin vao cuoi file nay roi moi thuc hien merge. Nhom truong se doi chieu bang nay voi "git log" truoc khi xac nhan.

---

### Luot gop #___: Nhanh [Ten-Nhanh] -> main
- **Nguoi thuc hien:** [Ho va Ten] (MSSV: [MSSV])
- **Nhanh nguon:** [Ten-Nhanh-Cua-Ban]
- **Nhanh dich:** main
- **Thoi gian:** YYYY-MM-DD HH:MM
- **Ma Commit (Git log hash):** [Dung lenh "git log -n 1 --oneline" de lay ma hash]
- **Thong diep commit:** [Noi dung commit message]

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | [Ghi ro ten file va dong hoac muc nao, vi du: report/team/group_report.md muc 2.3] |
| **Noi dung cong viec da lam** | [Tom tat ngan gon noi dung da lam o checkpoint nao] |
| **Muc dich su dung AI** | [Dung AI de lam gi trong lan sua nay?] |
| **AI da giup duoc gi** | [Ket qua tot ma AI ho tro] |
| **AI da sai hoac hoi hot o dau** | [Chi ra cho AI noi chung chung, sai so lieu hoac thieu logic] |
| **Toi da tu sua lai bang nhan dinh gi** | [Ban da tu viet lai hoac sua lai the nao?] |
| **Trang thai kiem tra truoc khi gop** | [Da pull main moi nhat chua? Co bi xung dot khong?] |


---

### Luot gop #1: Nhanh [DoMinhHieu] -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:23
- **Ma Commit (Git log hash):** db97689 (commit moi nhat chua bao cao ca nhan; truoc do a450eae)
- **Thong diep commit:** Update individual report 2A202603402_DoMinhHieu (CP1 AI note, section 5 log)

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | report/individual/2A202603402_DoMinhHieu.md (muc 2, 3, 5). Khong sua report/team/group_report.md va TEAM.md |
| **Noi dung cong viec da lam** | CP1: bang scan 7 problem dang Job Story. CP2: top 3, Problem Card #1 day du, #2 va #3 tom tat, quy trinh nhap, bang AI phan bien. Muc 5: nhat ky dung AI (chi tiet ben duoi). CP7 (muc 4, 6) chua lam |
| **Muc dich su dung AI** | Doc repo GAS de lay so lieu that, lap bang scan, chon top 3, ve quy trinh nhap, viet Problem Statement v0/v1 va so sanh muc can thiep cho workflow GAS ca nhan, dinh dang lai cau truc .md de upload |
| **AI da giup duoc gi** | Tim cac con so that nam rai rac trong repo; chon bottleneck co so lieu nhat (tra tay cua hang); tach ro v0 va v1 cua Problem Statement; lap luan khong chon muc don gian hon dua tren so that |
| **AI da sai hoac hoi hot o dau** | Bang scan do AI soan tu tai lieu khong con dung voi thuc te; nhieu o thoi gian khong co so do nen phai ghi "chua do"; ban dau ghi sai nguon benchmark; muc tieu "<= 4 luot/ngay" va nguong dung la de xuat cua AI, khong phai so do; quyet dinh "Go" khi chua co so phut tiet kiem |
| **Toi da tu sua lai bang nhan dinh gi** | Bo sung lai quy trinh dung thuc te, bo 1 dong quy trinh deprecated; tu danh gia Card 1 la bottleneck lon nhat roi moi den Card 3; giu "chua do" cho den khi bam gio that. Cac o chua dien o CP5-6 va CP6 duoc de trong dung nhu muc 5 cua bao cao ca nhan |
| **Trang thai kiem tra truoc khi gop** | Da fetch group/main truoc khi commit, khong co commit moi va khong xung dot. Luu y: hai commit a450eae va db97689 da duoc push thang len main truoc khi tao nhanh DoMinhHieu (nhanh DoMinhHieu hien dang tro cung commit db97689). Chua pull lai sau thoi diem do |

**Nhat ky dung AI chi tiet:**

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI đọc repo GAS (log chạy công việc hiện tại) và lập bảng 7 problem dạng Job Story kèm dấu hiệu thật | Tìm ra các con số thật nằm rải rác trong repo | Ba dòng không có số phút, chỉ có mô tả | Tôi đã bổ sung lại quy trình đúng thực tế, và bỏ 1 dòng quy trình deprecated. Đã ghi rõ trong bảng dòng nào "chưa đo" thay vì để AI đoán số |
| CP2 Problem Card | Nhờ AI chọn top 3, viết Problem Card #1 và tóm tắt #2, #3; vẽ quy trình nháp hiện tại | Chọn bottleneck có số liệu nhất (tra tay `取件門市`), chỉ ra bước nghẽn và các phương án No AI / Rule | Số phút từng bước không có trong repo, nên các ô phút phải ghi "chưa đo". AI chọn card #3 (Zalo) nhưng chính nó cũng thừa nhận chưa đủ dữ kiện | Cá nhân tôi đánh giá Card 1 là bottleneck lớn, rồi mới đến 3. Giữ "chưa đo" cho đến khi bấm giờ thật |
| CP4 Research | Chưa dùng AI | | | Chưa làm. Chưa phỏng vấn ai, chưa tìm công cụ tương tự, nên chưa ghi link nào |
| CP5 Quy trình | Nhờ AI vẽ quy trình trước/sau từ code `daily.py`, `fill_template.py`, `validate.py` | Phân bước nào Rule, bước nào AI, bước nào người; đối chiếu được với những gì đã chạy thật ngày 10-09 (132 đơn, 10 dòng cần người) | Phiên đầu ghi nguồn benchmark là "session 5" mà không kiểm lại; bước đọc file kết quả (Phase 3b) trong repo **chưa xây** nhưng bản đầu dễ đọc như đã có | AI tự rà lại và sửa nguồn thành "benchmark 10-03", đánh dấu bước 7 là **CHƯA XÂY**. Đây là sửa của AI, không phải của tôi. |
| CP5–6 Problem Statement | Nhờ AI viết Problem Statement v0 rồi v1 | Tách được v0 và v1 với lý do đổi rõ ràng (thêm "chọn nhầm = 0" vì chọn nhầm cửa hàng tệ hơn để trống) | Mục tiêu "≤ 4 lượt/ngày" và các ngưỡng dừng là con số **AI đề xuất**, không phải số đo; metric thời gian chưa có baseline | AI đã gắn nhãn "đề xuất" cho các số này. |
| CP6 Mức can thiệp / quyết định | Nhờ AI so sánh 4 mức, chấm 4 rủi ro, đề xuất quyết định "Go, phạm vi nhỏ" | Lý do không chọn mức đơn giản hơn dựa trên số thật (benchmark còn 3 dòng dư đều là chữ Latin; ngày 10-09 có 4/10 dòng cần người là chữ Latin) | Quyết định "Go" là đề xuất của AI khi chưa có số phút tiết kiệm được (Value chấm "Trung bình" chỉ dựa trên số lượt/ngày). Chính sách gửi địa chỉ khách cho Gemini chưa được kiểm tra | App Script vẫn còn dư địa xử lý data, việc implement AI còn cần tính chi phí và mức độ scale nên chưa quyết định GO|

---

### Luot gop #2: Nhanh [DoMinhHieu] -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:59
- **Ma Commit (Git log hash):** f61f5dd
- **Thong diep commit:** group_report 2.1: fill pitch rows 7-9 (Do Minh Hieu)

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | report/team/group_report.md muc 2.1 (dong 7, 8, 9 cua bang Pitch) |
| **Noi dung cong viec da lam** | CP3: dien 3 Problem Card cua Do Minh Hieu vao bang Pitch, va cau hoi phan bien nhan duoc tu nhom |
| **Muc dich su dung AI** | Chi dung de sao chep noi dung 3 card tu bao cao ca nhan vao bang, va ho tro commit/push len nhanh |
| **AI da giup duoc gi** | Sao chep dung noi dung tu bao cao ca nhan; kiem tra khong co thong tin nhay cam truoc khi commit; rebase/kiem tra xung dot khi push |
| **AI da sai hoac hoi hot o dau** | Ban dau AI de trong cot cau hoi phan bien va ghi them so phut "chua do" cho dong 7, 8; sau do da duoc chinh lai |
| **Toi da tu sua lai bang nhan dinh gi** | Toi tu viet lai y tuong cua cac dong 7-9 va dien cau hoi phan bien nhan duoc tu thanh vien nhom (tren cot "Cau hoi phan bien nhan duoc") |
| **Trang thai kiem tra truoc khi gop** | Da fetch group truoc khi push. Nhanh DoMinhHieu khong co xung dot; group/main co them commit 3a1b945 (file ca nhan cua Khoa), khong cham file nao toi sua. Chua pull main moi nhat vao nhanh |

---

### Luot gop #3: Nhanh [DoMinhHieu] -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 12:29
- **Ma Commit (Git log hash):** 6ef228e
- **Thong diep commit:** group_report 2.1-2.2: sync pitch rows from main, fill cluster table

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | report/team/group_report.md muc 2.1 (dong 1-6 va 10-12 dong bo tu main, dong 7-9 giu nguyen) va muc 2.2 (bang Cluster A, B, C) |
| **Noi dung cong viec da lam** | CP3: dong bo bang Pitch day du 12 dong tu main; dien bang Cluster 2.2 |
| **Muc dich su dung AI** | AI goi y cach gom 12 candidate thanh 3 cluster (A, B, C) tu bang Pitch tren main; ho tro commit va push len nhanh |
| **AI da giup duoc gi** | Dua ra ban nhap 3 cluster kem pattern chung; chi ra #7 co the nam o A hoac B va #1 la ung vien khop yeu nhat o B |
| **AI da sai hoac hoi hot o dau** | Ban nhap cua AI chi dua tren noi dung bang Pitch, chua qua thao luan nhom nen chua phai ket luan chung cua nhom |
| **Toi da tu sua lai bang nhan dinh gi** | Toi tu viet lai ten cluster va pattern chung theo cach hieu cua minh (vi du doi ten cluster A, doi cach goi cho #5), khong chep nguyen ban nhap cua AI |
| **Trang thai kiem tra truoc khi gop** | Da fetch group truoc khi commit. Nhanh DoMinhHieu chua duoc cap nhat voi main (commit d2e6cbc va 3a1b945); noi dung dong 1-6 va 10-12 duoc dong bo tay tu main, chua merge nen khi gop co the can xu ly xung dot |


---

### Luot gop #4: Nhanh [DoMinhHieu] -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 16:25
- **Ma Commit (Git log hash):** 8c6b984
- **Thong diep commit:** group_report 3.3: research Google Maps, Tripadvisor, ShopeeFood/Grab

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | report/team/group_report.md muc 3.3 (bang research 3 cong cu) |
| **Noi dung cong viec da lam** | CP4: dien bang research giai phap da co cho Google Maps, Tripadvisor, ShopeeFood/Grab, kem link da mo duoc |
| **Muc dich su dung AI** | Goi y 3 cong cu va suggest chuc nang + dinh dang van ban + push len branch |
| **AI da giup duoc gi** | Cung cap thong tin can thiet de viet muc 3.3 |
| **AI da sai hoac hoi hot o dau** | - |
| **Toi da tu sua lai bang nhan dinh gi** | Toi tu viet lai noi dung cac cot cua bang va thay doi link nguon |
| **Trang thai kiem tra truoc khi gop** | Da fetch group truoc khi commit. Chua pull main moi nhat vao nhanh nen khi gop co the can xu ly xung dot |
