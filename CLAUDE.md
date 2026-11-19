# Mokio · Hellfire

## Bối cảnh (context pack)
- Tầm nhìn: Giúp product team đi từ brief đến prototype UI + spec sẵn sàng build cùng Claude mà không cần tách rời thiết kế khỏi yêu cầu (spec sống cùng màn hình trong git)
- Người dùng: Team sản phẩm nhỏ (Owner, Designer, Reviewer, Developer) làm công cụ nội bộ/self-hosted, dùng mỗi vòng thiết kế–review tính năng, đang khó chịu vì thiết kế và yêu cầu trôi lệch nhau, comment review rời rạc dễ sót, AI tự đoán sai rule
- Key journey: (Owner) Điền brief
(Claude) Dựng màn hình + SPEC.md; gặp rule xung đột thì hỏi người thay vì đoán
(Reviewer/Designer) Review theo vòng, gửi comment cho Claude đến khi mọi màn Approved
(Owner) Commit, mở PR, Claude review PR, merge vào main
(Developer) Đọc spec + PR rồi build (chuyển sang Agilab)
- Ràng buộc: Bước 3/6 (Design) của flow "From bid to release", nối Specpop → Agilab; Web (API key) + Desktop (Claude Code), prototype Web/Desktop/Mobile; giữ spec sống trong git cùng màn hình, 4 vai trò phân quyền, Claude hỏi người khi rule xung đột, Review/Spec/git vẫn chạy khi tắt AI
- Ví dụ tốt: Dự án mẫu Kanban tracker trong Mokio: mọi màn đã Approved, SPEC.md có rule mã hoá (T-1, R-1, DR-1, BR-3…) truy được nguồn gốc trong Activity, PR sạch rồi merge vào main và chuyển sang Agilab để build
- Tiêu chí: Tỉ lệ màn hình đã duyệt (vd 14/14 màn Approved), 0 comment nháp và 0 rule "open question"/"Waiting for you" còn mở, PR được Claude review không còn xung đột/rule vỡ/thiếu state trước khi merge, số vòng review đến khi duyệt hết

## Giai đoạn hiện tại
Giai đoạn định hình, trước Gate 1. Bước đang làm: [1–5].