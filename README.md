<div align="center">

# Mẫu 22 KT PRO

**Phần mềm khai hồ sơ Mẫu 22.KT cho doanh nghiệp xuất nhập khẩu thủy sản**

AI đọc chứng từ (CS, giấy phép, vận đơn, NOAA...) → tự lắp ráp Mẫu 22.KT → tra cứu tàu trên RFMO / IUU / AIS → xuất Word

[![Phiên bản mới nhất](https://img.shields.io/github/v/release/quoctienkdqt-coder/Mau22-Updates?label=phi%C3%AAn%20b%E1%BA%A3n&color=2563EB)](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases/latest)
![Windows](https://img.shields.io/badge/Windows-8.1%20%7C%2010%20%7C%2011%20(64--bit)-0F172A)

### [⬇️ Tải bộ cài mới nhất (mysetup.exe)](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases/latest/download/mysetup.exe)

[Trang giới thiệu](https://quoctienkdqt-coder.github.io/landing-page/) · [Lịch sử phiên bản](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases)

</div>

---

## Tính năng chính

| | |
|---|---|
| 🤖 **Đội AI** | AI đọc toàn bộ chứng từ một lượt; phần mềm kiểm tra lại bằng lớp chữ của PDF rồi lắp ráp Mẫu 22.KT theo bộ quy tắc cố định. Tắt/bật bằng công tắc "🤖 Đội AI" trên thanh công cụ. |
| 🎨 **Tô màu từng ô** | ĐỎ = sai khác cần xử lý · VÀNG = nghi ngờ, nên soi lại · XANH = phần mềm đã tự sửa. Rê chuột vào ô để xem lý do. |
| 💬 **Trợ lý Jarvis** | Hỏi lại những điểm phần mềm chưa chắc chắn. Không tự bật cửa sổ, chỉ hiện khi bạn bấm nút. |
| 🚢 **Tra cứu tàu** | Đối chiếu tàu trên WCPFC, IOTC, ICCAT, IATTC, danh sách tàu IUU và dữ liệu AIS (Global Fishing Watch). Tên tàu / IMO / hô hiệu lệch CSDL được đánh dấu ngay trên bảng. |
| 🧾 **Đối chiếu PDF DVC / eCDT** | So hồ sơ đang mở với file PDF Mẫu 22 tải từ Cổng DVC hoặc eCDT, không cần AI. |
| 📄 **Xuất Word** | Xuất đúng biểu mẫu Mẫu 22.KT song ngữ Anh – Việt. |

## Cài đặt

1. Tải [**mysetup.exe**](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases/latest/download/mysetup.exe) (khoảng 135 MB).
2. Chạy file và làm theo hướng dẫn. Thư mục cài mặc định: `C:\KHAI KN\`.
3. Mở phần mềm, nhập **key bản quyền** (key gắn với từng máy) rồi nhập **API key AI** (Google Gemini hoặc APIZ) trên thanh công cụ.

> Windows SmartScreen có thể hiện "Windows protected your PC" vì bộ cài chưa có chứng thư ký mã của Microsoft. Bấm **More info → Run anyway** nếu bạn tải file từ đúng trang này.

**Yêu cầu:** Windows 8.1 / 10 / 11 bản 64-bit, có kết nối Internet (để gọi AI và tra cứu RFMO).

## Cập nhật

Phần mềm tự kiểm tra bản mới khi khởi động và hỏi bạn trước khi cập nhật. Dữ liệu của bạn (cấu hình, CSDL, danh sách công ty) được giữ nguyên khi cập nhật.

Mỗi bản cập nhật đều được **ký số (Ed25519)** và kèm **mã SHA-256** của bộ cài; phần mềm chỉ cài khi chữ ký và mã khớp, nên file bị sửa đổi hoặc tải lỗi sẽ bị từ chối.

## Có gì mới

**1.2.10** (13/11/2026)
- Giấy phép tàu Indonesia do TỈNH cấp: nhận đúng cơ quan cấp cả khi giấy phép là bản dịch tiếng Anh
- Tự nhận tỉnh từ mã tỉnh trong số giấy phép (VD `45.26.7398...` → Sulawesi Selatan) khi giấy phép không ghi rõ tên cơ quan
- Số giấy phép cấp tỉnh (bắt đầu `45.`) không còn bị ghi nhầm cơ quan cấp là Bộ Thủy sản Indonesia (KKP)

**1.2.9** (11/11/2026)
- Chế độ Đội AI, tô màu ô, trợ lý Jarvis
- Tra cứu IUU nhanh hơn nhiều (tải danh sách một lần cho cả hồ sơ)
- Đối chiếu định danh tàu với CSDL RFMO sau khi tra cứu; bỏ cảnh báo đỏ oan "LỆCH MÃ RFMO" với IOTC / ICCAT / IATTC
- Liệt kê giấy phép tàu nhận chuyển tải; cảnh báo khi chuyển tải ngoài hiệu lực giấy phép

Xem đầy đủ tại [Releases](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases).

---

<details>
<summary><b>Dành cho kỹ thuật: các file trong kho này</b></summary>

Kho này chỉ dùng để **phát hành bộ cài**; mã nguồn không nằm ở đây. Vui lòng không đổi tên hay xóa các file dưới đây vì máy khách các bản cũ vẫn đọc chúng.

| File | Dùng cho |
|---|---|
| `update_manifest.json` | Kênh tự cập nhật từ bản 1.2.x (phiên bản, link tải, SHA-256, chữ ký) |
| `version.json` | Kênh cập nhật cũ của máy bản 1.1.0 |
| `wcpfc_vessels.csv`, `iotc_vessels.xlsx`, `iccat_vessels.csv`, `iattc_vessels.xlsx`, `IUUList.xls` | Dữ liệu tàu RFMO / IUU dạng file của các bản cũ (bản mới tra cứu trực tuyến) |

Bộ cài của mỗi phiên bản nằm trong mục [Releases](https://github.com/quoctienkdqt-coder/Mau22-Updates/releases). Từ bản 1.2.7, bộ cài luôn tên `mysetup.exe` (các bản 1.0.x – 1.1.0 là file chạy `.exe` đơn lẻ).

</details>
