# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:Phạm Ngọc Linh 
- **Lớp:K26CNTT3
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):Windows

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv cap_nhat.txt docs
mv logo_gamezone.png media
cp .\media\logo_gamezone.png .\backup\
rm temp_207.tmp
Get-ChildItem -Recurse -Force

```

### Kết quả liệt kê toàn bộ dự án

```text
Directory: C:\Users\TRONG TIN\Downloads\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:33 PM                backup
d-----        10/26/2026   1:33 PM                docs
d-----        10/26/2026   1:32 PM                logs
d-----        10/26/2026   1:33 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:34 PM           1808 bai_lam.md


    Directory: C:\Users\TRONG TIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png


    Directory: C:\Users\TRONG TIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM             61 cap_nhat.txt


    Directory: C:\Users\TRONG TIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
 Get-Content logs/game.log | Select-String "ERROR" > logs/daily_report.txt
 Get-Content .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game

```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [ X] Heading 1
- [X ] Mô tả in đậm + in nghiêng
- [X ] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [X ] Code block lệnh liệt kê
- [X ] Task list (≥2 việc, ≥1 đã xong)
- [ X] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell


```

### Nội dung file logs/auto_report.txt

```text
# Tac gia: Pham Ngoc Linh
# Ngay tao: 26/10/2026

"=== BAO CAO LOI GAMEZONE ===" > "logs/auto_report.txt"
Get-Content logs/game.log | Select-String "ERROR" >> logs/auto_report.txt
Write-Host "Da tao bao cao: logs/auto_report.txt"

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
 Get-Content logs/game.log | Select-String "ERROR" | Measure-Object

```

### Kết quả đếm

```text
Count    : 6
Average  :
Sum      :
Maximum  :
Minimum  :
Property :

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG GAMEZONE ===" > .\logs\tong_hop.txt
Get-Content .\logs\game.log | Select-String "WARNING" >> .\logs\tong_hop.txt
(Get-Content .\logs\game.log | Select-String "ERROR" | Measure-Object).Count >> .\logs\tong_hop.txt
Get-Content .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE ===

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%


6
```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
