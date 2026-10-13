# Gợi ý nâng cấp — rà soát 2026-10-13

> Lấy từ đợt rà soát chéo 19 repo của chủ sở hữu (ma trận vệ sinh ở [seeker19110/stored, mục 23 §8.1](https://github.com/seeker19110/stored/blob/main/23-own-repos-lessons/README.md); gợi ý tích hợp ở §7b của cùng file). Số liệu đo bằng lệnh trên HEAD (đếm `uses:` ghim SHA 40 ký tự, khối `permissions:`, `dependabot.yml`, `.claude/settings.json`), không suy ra từ văn xuôi. Đây là **đề xuất**, chưa sửa code. Mỗi mục kèm bằng chứng để kiểm lại trước khi làm; mục nào đã xử lý thì đánh dấu hoặc xoá.

## Hiện trạng đo được

| HEAD đọc | Action ghim SHA | Workflow thiếu `permissions:` cấp đầu | Dependabot | LICENSE · SECURITY | File test |
|---|---|---|---|---|---|
| `9d83887` (2026-08-12) | không có workflow | – | **không có** | không · không | 0 |

## Đề xuất (🔴 cao · 🟠 trung bình · 🟢 nhẹ)

| # | Mức | Đề xuất | Bằng chứng | Kiểm xong khi |
|---|---|---|---|---|
| 1 | 🟠 | Xử lý bản quyền: chuyển repo sang **private**, hoặc gỡ ảnh chụp từ sách và chỉ giữ ghi chú tự viết, có dẫn nguồn | README dẫn sách *System Design Interview* (Alex Xu), repo có 392 ảnh; không có LICENSE; git log cho thấy tác giả là Gaurav Kumar (bản web ở pagefy.io) | Repo private, hoặc không còn ảnh trích từ sách |
| 2 | 🟢 | Ghi rõ nguồn gốc fork / upstream trong README | Upstream GitHub chưa xác định được | README có dòng nguồn |

## Giữ nguyên (điểm mạnh)

- 25 link tới paper gốc rất có ích để tra cứu.

## Gợi ý tích hợp từ catalog `stored`

- Dựng knowledge graph (Graphify) để tra chéo chương ↔ paper (stored mục 16 §2d).

## Ghi chú chung

- Ghim action theo SHA bằng [pinact](https://github.com/suzuki-shunsuke/pinact) hoặc [ratchet](https://github.com/sethvargo/ratchet), giữ comment tag (`# v7.0.1`), rồi để Dependabot `github-actions` tự nâng SHA. Đây là cách projects-template, xboss và Sales-Hunter đang làm.
- Chuẩn tham chiếu là `seeker19110/projects-template`: 25/25 action ghim SHA, mọi workflow có `permissions:` cấp đầu, Dependabot cho npm, github-actions và pip.
