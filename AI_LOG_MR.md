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

### Luot gop #001: Nhanh buivanlam -> main
- **Nguoi thuc hien:** Bùi Văn Lâm (MSSV: 2A202603400)
- **Nhanh nguon:** buivanlam
- **Nhanh dich:** main
- **Thoi gian:** 2026-11-09 11:10
- **Ma Commit (Git log hash):** 55552bc
- **Thong diep commit:** Nop bao cao ca nhan CP1-CP2 va cap nhat thong tin TEAM.md

| Muc thong tin | Chi tiet khai bao |
|---|---|
| **Cac file da sua / tao moi** | `report/individual/2A202603400_BuiVanLam.md` (tao moi toan bo CP1, CP2), `TEAM.md` (dien thong tin dong 2 va muc BuiVanLam-2A202603400), `AI_LOG_MR.md` (append luot gop #001) |
| **Noi dung cong viec da lam** | Hoan thanh CP1 (Scan 10 problem dat tieu chuan Bonus B1), CP2 (Top 3 Problem Cards co so phut va bottleneck ro rang), thiet lap quy tac tranh conflict voi main |
| **Muc dich su dung AI** | Ho tro brainstorm 4 lang kinh, dong vai PM hoai nghi de phan bien lo hong cua Problem Card, ho tro format so do quy trinh ASCII |
| **AI da giup duoc gi** | Goi y huong tiep can thuc te trong he sinh thai Vingroup, ho tro cau truc hoa cac chi so đo luong (Metric) va ranh gioi van hanh (Boundary) |
| **AI da sai hoac hoi hot o dau** | AI dua ra cac giai phap "chatbot toan nang" (solution tra hinh), goi y camera AI tu dong phat cu dan (vi pham phap ly), va de xuat multi-agent qua phuc tap |
| **Toi da tu sua lai bang nhan dinh gi** | Tu loai bo solution tra hinh, bo sung 3 bai toan that tu doi song sinh vien, chuyen sang mo hinh Hybrid Workflow (Rule 70% + LLM 30% + CSKH HITL), thong nhat 1 con so baseline duy nhat |
| **Trang thai kiem tra truoc khi gop** | Da merge origin/main moi nhat, khong co conflict nao xay ra |

