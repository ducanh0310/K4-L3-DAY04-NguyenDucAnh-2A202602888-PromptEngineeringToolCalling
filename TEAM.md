# TEAM — Day04, K4-L3B

**Làm nhóm.** Mỗi người tự viết và commit phần INDIVIDUAL của mình.

## Thông tin bài nộp

- Tên nhóm: Nhóm 2A202602888
- Người đại diện / MSSV: Nguyễn Đức Anh - 2A202602888
- Tên repo: `K4-L3-DAY04-NguyenDucAnh-2A202602888-PromptEngineeringToolCalling`
- URL repo, nhánh nộp, commit chốt: https://github.com/ducanh0310/K4-L3-DAY04-NguyenDucAnh-2A202602888-PromptEngineeringToolCalling, nhánh `main`
- Deadline áp dụng và link thông báo đổi hạn nếu có: 23:59 15/09/2026

## Thành viên

| Họ và tên | MSSV | GitHub | Vai trò và công việc | File/commit/PR |
|---|---|---|---|---|
| Nguyễn Đức Anh | 2A202602888 | ducanh0310 | Trưởng nhóm, xây dựng Agent loop, Tối ưu System Prompt v0-v3, Xây dựng Web UI | starter_v0/server_ui.py, artifacts/system_prompt.md |
| Nguyễn Minh Ngọc | 2A202602530 | ngonguyenminhngoc234it-gif
cnm | Thiết kế bộ 10 test case nhóm (eval_group.json) 5 đơn lượt + 5 nhiều lượt, Tối ưu hóa tools.yaml | data/eval_group.json, artifacts/tools.yaml |
| Đồng Mạnh Hùng | 2A202602412 | Hung23020370
 | Đánh giá an toàn & bảo mật dữ liệu (eval_adversarial.json), Viết báo cáo kỹ thuật REPORT.md | data/eval_adversarial.json, artifacts/REPORT.md |

## Nhận xét chung

- Kết quả và bằng chứng: Đã chạy thành công 4 phiên bản v0-v3 bằng OpenRouter (`gpt-4o-mini`), độ chính xác tăng từ 70% (v0) lên 93.3% (v3). Minh chứng tại `starter_v0/runs/`.
- Thay đổi hiệu quả nhất: Bỏ yêu cầu ép Agent output JSON cứng trong System Prompt ban đầu và thiết lập quy tắc Tool Routing chi tiết.
- Giới hạn còn lại: Một số câu hỏi nhiều thông tin phức tạp cùng lúc vẫn cần thêm lượt hỏi làm rõ qua `clarify`.
- Cách phân công và tích hợp: Nhóm gồm 3 thành viên phân chia các mảng chuyên biệt (Prompt/UI, Tools/Group Cases, Safety/Report), kiểm thử độc lập và tích hợp qua Git.

## INDIVIDUAL

### Nguyễn Đức Anh — 2A202602888

- Phần việc và file/commit/PR: Trưởng nhóm, tối ưu `artifacts/system_prompt.md` qua v0-v3, phát triển Web UI (`server_ui.py`).
- Quyết định, khó khăn và cách xử lý: Loại bỏ định dạng JSON ép buộc trong prompt gốc, chuyển sang Native Tool Calling hoàn toàn. Xây dựng Web UI trực quan hóa Tool Calls.
- Điều đã học: Kỹ thuật Prompt Engineering cho Tool Calling và cách kết nối Agent với Web UI.
- AI/công cụ đã dùng và cách kiểm tra: Antigravity IDE, OpenRouter API.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 21:00 15/09/2026

### Nguyễn Minh Ngọc — 2A202602530

- Phần việc và file/commit/PR: Thiết kế 10 test case nhóm trong `data/eval_group.json` (5 đơn lượt + 5 nhiều lượt) và tối ưu `artifacts/tools.yaml`.
- Quyết định, khó khăn và cách xử lý: Xây dựng các kịch bản thực tế như hủy ticket giữa chừng hay đổi thông tin máy ở lượt 2 để kiểm thử khả năng thích ứng của Agent. Bổ sung enum và mô tả rõ ràng trong `tools.yaml`.
- Điều đã học: Cách viết test case đánh giá chuẩn định dạng JSON cho Agent loop và tối ưu hóa Schema cho LLM.
- AI/công cụ đã dùng và cách kiểm tra: Antigravity IDE, `run_eval.py`.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 21:00 15/09/2026

### Đồng Mạnh Hùng — 2A202602412

- Phần việc và file/commit/PR: Đánh giá an toàn và ranh giới dữ liệu trong `data/eval_adversarial.json`, viết báo cáo kỹ thuật `artifacts/REPORT.md`, tổng hợp bằng chứng thử nghiệm và cập nhật `version_log.csv`.
- Quyết định, khó khăn và cách xử lý: Thống kê chỉ số chính xác và đường dẫn đến từng run file thực tế để minh chứng cho báo cáo; đảm bảo Prompt Injection không phá vỡ ranh giới an toàn.
- Điều đã học: Quy trình báo cáo sản phẩm Agent AI theo chuẩn mực kỹ thuật và nguyên lý kiểm thử an toàn cho LLM.
- AI/công cụ đã dùng và cách kiểm tra: Antigravity IDE, `run_eval.py --suite adversarial`, Git.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 21:00 15/09/2026
