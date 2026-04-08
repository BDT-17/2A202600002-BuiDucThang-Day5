| Khi nào xảy ra | Chuyện gì xảy ra | Xử lý thế nào (cải thiện) |
|---|---|---|
| Bias giới tính/trường | AI ưu tiên nam/đại học top → loại bỏ ứng viên nữ/giỏi từ trường tầm trung | Ẩn giới tính, trường học khỏi input AI. Audit định kỳ tỷ lệ nam/nữ, trường top/non-top. Retrain nếu chênh lệch >15%. |
| Loại nhầm người giỏi | Ứng viên career switcher (chuyển ngành) bị điểm thấp dù có skill transferable | Flag CV có gap nghề, bootcamp, freelance. Đưa vào "curiosity queue" HR review tay. Weight portfolio > job title. |
| Keyword matching nguội | AI chỉ đếm từ khóa (React, Python) → bỏ qua ứng viên dùng từ đồng nghĩa (frontend, backend) | Dùng semantic search thay keyword matching. Xây synonym dictionary ngành. Test với CV viết "lập trình web" thay "React". |
| Không hiểu context dự án | "Lead team 5 người" bị hiểu như "làm việc nhóm 5 người" → điểm leadership sai | Trích số liệu cụ thể: "tăng revenue 30%", "giảm bug 50%". Weight achievements có metrics > mô tả chức danh. |
| CV format lạ | CV infographic/creative bị parse sai → thông tin missing | OCR confidence <80% → auto-email ứng viên yêu cầu re-upload dạng text. Fallback sang manual queue không auto-reject. |
