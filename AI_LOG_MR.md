# Nhat ky sua file va gop nhanh vao main (AI & Merge Log)

> Quy tac: Moi khi bat ky thanh vien nao sua file bai nhom (report/team/group_report.md hoac TEAM.md) va yeu cau gop vao nhanh main, bat buoc phai copy khung mau duoi day, dien day du thong tin vao cuoi file nay roi moi thuc hien merge. Nhom truong se doi chieu bang nay voi "git log" truoc khi xac nhan.

---

### Khung mau cho cac luot tiep theo:
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

## Danh sach cac luot gop da thuc hien

### Luot gop #001: Nhanh NguyenDucTrung-2A202603423 -> main
- **Nguoi thuc hien:** Nguyen Duc Trung (MSSV: 2A202603423)
- **Nhanh nguon:** NguyenDucTrung-2A202603423
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:58
- **Ma Commit (Git log hash):** ad90b07
- **Thong diep commit:** Cap nhat 3 problem card va 3 cau hoi phan bien vao muc 2.1 pitch trong group_report.md

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/team/group_report.md` (dong 21 den 23, muc 2.1 Pitch), `report/individual/2A202603423_NguyenDucTrung.md` |
| **Noi dung cong viec da lam** | Dien 3 Problem Card ca nhan cua Nguyen Duc Trung (#1 Vincom, #2 Xanh SM, #3 Vinhomes) va 3 cau hoi phan bien nhan duoc tu cac thanh vien Hieu, Lam, Khoa |
| **Muc dich su dung AI** | Ho tro dinh dang bang bieu va tich hop noi dung phan bien vao bao cao nhom |
| **AI da giup duoc gi** | Chuan hoa cau hoi phan bien ro nghia, dung ngu canh tung bai toan |
| **AI da sai hoac hoi hot o dau** | Khong co sai sot |
| **Toi da tu sua lai bang nhan dinh gi** | Tiep nhan cac cau hoi truc tiep tu buoi thao luan that cua cac ban trong nhom |
| **Trang thai kiem tra truoc khi gop** | Da kiem tra khong bi xung dot dinh dang va khong anh huong den cac dong khac |

---

### Luot gop #002: Nhanh buivanlam -> main
- **Nguoi thuc hien:** Bùi Văn Lâm (MSSV: 2A202603400)
- **Nhanh nguon:** buivanlam
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:57
- **Ma Commit (Git log hash):** ecd393c
- **Thong diep commit:** docs: add group report for K5-L3-Day02 Discovery Problem Framing

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603400_BuiVanLam.md`, `TEAM.md`, `report/team/group_report.md` (dong 24 den 26, hang 4-6 muc 2.1 Pitch) |
| **Noi dung cong viec da lam** | Hoan thanh CP1, CP2, dien hang 4-6 trong bang Pitch kem cau hoi phan bien nhan duoc tu Trung, Hieu, Khoa |
| **Muc dich su dung AI** | Ho tro brainstorm 4 lang kinh, dong vai PM hoai nghi de phan bien lo hong cua Problem Card, ho tro format so do quy trinh ASCII |
| **AI da giup duoc gi** | Goi y huong tiep can thuc te trong he sinh thai Vingroup, ho tro cau truc hoa cac chi so đo luong (Metric) va ranh gioi van hanh (Boundary) |
| **AI da sai hoac hoi hot o dau** | AI dua ra cac giai phap "chatbot toan nang" (solution tra hinh), goi y camera AI tu dong phat cu dan (vi pham phap ly), va de xuat multi-agent qua phuc tap |
| **Toi da tu sua lai bang nhan dinh gi** | Tu loai bo solution tra hinh, bo sung 3 bai toan that tu doi song sinh vien, chuyen sang mo hinh Hybrid Workflow (Rule 70% + LLM 30% + CSKH HITL), thong nhat 1 con so baseline duy nhat |
| **Trang thai kiem tra truoc khi gop** | Da kiem tra dong 4-6 khong cham vao cac dong cua thanh vien khac |

---

### Luot gop #003: Nhanh DoMinhHieu -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:59
- **Ma Commit (Git log hash):** f61f5dd
- **Thong diep commit:** group_report 2.1: fill pitch rows 7-9 (Do Minh Hieu)

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603402_DoMinhHieu.md`, `report/team/group_report.md` (dong 27 den 29, hang 7-9 muc 2.1 Pitch) |
| **Noi dung cong viec da lam** | CP1, CP2 bao cao ca nhan; dien 3 Problem Card cua Do Minh Hieu vao bang Pitch (hang 7-9) va cau hoi phan bien nhan duoc tu nhom |
| **Muc dich su dung AI** | Doc repo GAS de lay so lieu that, chon bottleneck, viet Problem Statement va so sanh muc can thiep |
| **AI da giup duoc gi** | Tim cac con so that nam rai rac trong repo; chon bottleneck co so lieu nhat; tach ro v0 va v1 cua Problem Statement |
| **AI da sai hoac hoi hot o dau** | Bang scan do AI soan co nhieu o thoi gian khong co so do; AI de xuat Go khi chua co so phut tiet kiem |
| **Toi da tu sua lai bang nhan dinh gi** | Bo sung lai quy trinh dung thuc te, tu danh gia Card 1 la bottleneck lon nhat; dien day du cau hoi phan bien nhan duoc tu Trung, Lam, Khoa |
| **Trang thai kiem tra truoc khi gop** | Khong cham vao cac dong cua cac thanh vien khac |

---

### Luot gop #004: Nhanh TranDangKhoa -> main
- **Nguoi thuc hien:** Tran Dang Khoa (MSSV: 2A202603364)
- **Nhanh nguon:** TranDangKhoa
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 12:02
- **Ma Commit (Git log hash):** bc17682
- **Thong diep commit:** Add files via upload

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603364_TranDangKhoa.md`, `report/team/group_report.md` (dong 30 den 32, hang 10-12 muc 2.1 Pitch) |
| **Noi dung cong viec da lam** | CP1, CP2 bao cao ca nhan; dien hang 10-12 trong bang Pitch gom 3 candidate kem cau hoi phan bien nhan duoc tu Trung, Hieu, Lam |
| **Muc dich su dung AI** | Ho tro ra soat de bai va dinh hinh cac van de gap phai trong qua trinh hoc tap |
| **AI da giup duoc gi** | Dinh dang cau hoi Job Story ro rang |
| **AI da sai hoac hoi hot o dau** | Khong co sai sot lon |
| **Toi da tu sua lai bang nhan dinh gi** | Chon cac bai toan thuc te ve tiep can de lab, video huong dan va tai lieu nhom chat |
| **Trang thai kiem tra truoc khi gop** | Giu nguyen cac hang 1-9 cua cac ban khac; giu file ca nhan cua Hieu khong bi xoa |

---

### Luot gop #005: Nhanh DoMinhHieu -> main
- **Nguoi thuc hien:** Do Minh Hieu (MSSV: 2A202603402)
- **Nhanh nguon:** DoMinhHieu
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 12:29
- **Ma Commit (Git log hash):** df925a2
- **Thong diep commit:** group_report 2.1-2.2: sync pitch rows from main, fill cluster table

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/team/group_report.md` (muc 2.2 Cluster) |
| **Noi dung cong viec da lam** | Gom 12 candidate thanh 3 cluster (A, B, C) theo pattern chung ve xu ly du lieu, tra cuu va kiem tra ho so |
| **Muc dich su dung AI** | Ho tro nhan dien pattern chung giua cac problem |
| **AI da giup duoc gi** | Phân cum hop ly giua cac bai toan van hanh va bai toan hoc tap |
| **AI da sai hoac hoi hot o dau** | Khong co |
| **Toi da tu sua lai bang nhan dinh gi** | Tu xac lap 3 pattern ro rang theo ban chat quy trinh cong viec |
| **Trang thai kiem tra truoc khi gop** | Khong anh huong den bang Pitch |

---

### Luot gop #006: Nhanh NguyenDucTrung-2A202603423 -> main
- **Nguoi thuc hien:** Nguyen Duc Trung (MSSV: 2A202603423)
- **Nhanh nguon:** NguyenDucTrung-2A202603423
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 12:45
- **Ma Commit (Git log hash):** 7f1439f
- **Thong diep commit:** Hop nhat CP3 hoan chinh: thong tin nhom, pitch 12 hang, cluster, OST, shortlist va quyet dinh chon bai toan #1

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/team/group_report.md` (muc 1, 2.1, 2.2, 2.3, 2.4), `AI_LOG_MR.md`, `TEAM.md` |
| **Noi dung cong viec da lam** | Hop nhat toan bo noi dung cua Trung, Hieu, Lam; xac dinh bai toan chinh thuc cua nhom la Vincom Retail (#1) |
| **Muc dich su dung AI** | Ho tro tong hop so lieu, doi chieu git log va xu ly conflict giua cac nhanh |
| **AI da giup duoc gi** | Gop sach se tat ca dong khong lam mat bat ky bai nao cua thanh vien |
| **AI da sai hoac hoi hot o dau** | Khong co |
| **Toi da tu sua lai bang nhan dinh gi** | Nhóm trưởng truc tiep ra soat va quyet dinh giu bai toan Vincom Retail lam de tai chung |
| **Trang thai kiem tra truoc khi gop** | Da kiem tra toan bo conflict da duoc xu ly triet de |

---

### Luot gop #007: Nhanh TranDangKhoa -> main
- **Nguoi thuc hien:** Tran Dang Khoa (MSSV: 2A202603364)
- **Nhanh nguon:** TranDangKhoa
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 14:37
- **Ma Commit (Git log hash):** 8a6378f
- **Thong diep commit:** Cap nhat bao cao ca nhan va bao cao nhom

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603364_TranDangKhoa.md`, `report/team/group_report.md` (muc 2.3 Cay OST rut gon) |
| **Noi dung cong viec da lam** | Sua dinh dang bang Problem Card #1 trong bao cao ca nhan; trau chuot lai cau chu Outcome, 3 Opportunity va phan ly do gach bo Solution cho bai toan Vincom Retail o muc 2.3 |
| **Muc dich su dung AI** | Ho tro ra soat ngu phap va dien dat chat che cho cay OST |
| **AI da giup duoc gi** | Dien dat lai cac Opportunity thanh cac noi dau cua khach hang mot cach ro rang |
| **AI da sai hoac hoi hot o dau** | Khong co sai sot |
| **Toi da tu sua lai bang nhan dinh gi** | Tu kiem tra va can chinh lai ly do gach bo cac giai phap cong nghe tra hinh |
| **Trang thai kiem tra truoc khi gop** | Clean merge 100%, khong bi xung dot |

---

### Luot gop #008: Nhanh NguyenDucTrung-2A202603423 -> main
- **Nguoi thuc hien:** Nguyen Duc Trung (MSSV: 2A202603423)
- **Nhanh nguon:** NguyenDucTrung-2A202603423
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 15:34
- **Ma Commit (Git log hash):** 4f7c3ec
- **Thong diep commit:** hoan thanh bai nhom duoc phan cong va bai ca nhan

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603423_NguyenDucTrung.md` (muc 4, 5, 6, 7), `report/team/group_report.md` (muc 6, 7, 8, 9, 10), `TEAM.md`, `AI_LOG_MR.md` |
| **Noi dung cong viec da lam** | Hoan thanh bao cao ca nhan cua Nguyen Duc Trung: nhat ky tham gia CP3-CP7, bang su dung AI, reflection hon 200 tu va giai thich chuoi 6 mat xich; Hoan thien Goi 4 bao cao nhom: ma tran mo ho x phuc tap, so sanh 4 muc can thiep, AI Canvas, Google PAIR, Problem Statement v1 kem so sanh v0, tieu chi eval, bo 10 test case eval mau cho Bonus B3, 4 rui ro san pham, quyet dinh Go va nguong dung |
| **Muc dich su dung AI** | Ho tro ra soat tieu chi Rubric, cau truc bang bieu chuan format va kiem tra tinh nhat quan cua cac con so baseline |
| **AI da giup duoc gi** | Chuan hoa cau truc AI Canvas va dinh dang bang 10 test case eval ro rang tung truong |
| **AI da sai hoac hoi hot o dau** | AI danh gia rui ro Feasibility la Cao vi nghi can train model rieng; AI goi y cac chi so thanh cong chung chung |
| **Toi da tu sua lai bang nhan dinh gi** | Dinh luong hoa tat ca success metric (50 phut -> 2 phut, chenh lech chi phi < 10%); tu viet toan bo reflection ca nhan; thiet lap nguong dung ro rang cho pilot |
| **Trang thai kiem tra truoc khi gop** | Da kiem tra dong sua chinh xac o Goi 4, khong cham vao Goi 1, 2, 3 cua cac thanh vien khac |

---

### Luot gop #009: Hop nhat toan bo noi dung cac thanh vien (Khoa, Hieu, Lam, Trung) -> main
- **Nguoi thuc hien:** Nguyen Duc Trung (MSSV: 2A202603423) - Nhom truong
- **Nhanh nguon:** TranDangKhoa, DoMinhHieu, buivanlam, NguyenDucTrung-2A202603423
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 17:05
- **Ma Commit (Git log hash):** 00e7053
- **Thong diep commit:** Hop nhat toan dien group_report.md: Khoa (3.1-3.2), Hieu (3.3), Lam (4-5), Trung (6-10), dong bo TEAM.md

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/team/group_report.md` (toan bo cac muc tu 1 den 10), `TEAM.md`, `AI_LOG_MR.md` |
| **Noi dung cong viec da lam** | 1. Tich hop Muc 3.1 (Assumption Map) va 3.2 (3 Interview Snapshots The Mom Test co tin hieu phan bac) tu nhanh TranDangKhoa.<br>2. Tich hop Muc 3.3 (Research 3 giai phap: Google Maps, Tripadvisor, ShopeeFood/Grab kem link) tu nhanh DoMinhHieu.<br>3. Tich hop Muc 4 (Quy trinh truoc/sau) va Muc 5 (Problem Statement v0 kem phan hoi AI Coach) tu nhanh buivanlam.<br>4. Dong bo logic: lam sach toan bo icon/emoji trong so do Mermaid (Rule 10), thong nhat dia diem TTTM Vincom Mega Mall Smart City va ghep noi chi so thoi gian Before/After.<br>5. Cap nhat day du phan dong gop ca nhan cua ca 4 thanh vien trong TEAM.md. |
| **Muc dich su dung AI** | Ho tro doi chieu bat dong giua cac nhanh, kiem tra regex emoji Unicode va can chinh xung dot format bang bieu |
| **AI da giup duoc gi** | Phat hien cac diem cấn ve dia diem va don vi do thoi gian giua cac muc; ho tro lam sach emoji trong Mermaid |
| **AI da sai hoac hoi hot o dau** | Khong co |
| **Toi da tu sua lai bang nhan dinh gi** | Nhom truong truc tiep thong nhat logic thanh 1 kich ban nhat quan tu Muc 1 den Muc 10 |
| **Trang thai kiem tra truoc khi gop** | Clean merge 100%, 0 loi xung dot, 0 emoji, day du 10/10 muc trong group_report.md |
