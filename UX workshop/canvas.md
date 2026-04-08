# AI Product Canvas — Vietnam Airlines Chatbot NEO

AI Product Canvas — Ngày 5 — VinUni A20 — AI Thực Chiến · 2026

---

## Canvas

|   | Value | Trust | Feasibility |
|---|-------|-------|-------------|
| **Câu hỏi guide** | User nào? Pain gì? AI giải quyết gì mà cách hiện tại không giải được? | Khi AI sai thì user bị ảnh hưởng thế nào? User biết AI sai bằng cách nào? User sửa bằng cách nào? | Cost bao nhiêu/request? Latency bao lâu? Risk chính là gì? |
| **Trả lời** | User là hành khách Vietnam Airlines cần tra cứu chuyến bay, chính sách vé, hành lý và hỗ trợ nhanh 24/7. Pain chính là tổng đài chờ lâu và thông tin trên website khó tìm, không theo ngữ cảnh cá nhân. NEO giải quyết bằng cách cho phép hỏi bằng ngôn ngữ tự nhiên và trả lời tức thời các câu hỏi phổ biến. | Khi AI sai, user mất thời gian, nhầm thông tin và mất niềm tin vào hệ thống hỗ trợ. User nhận ra AI sai khi câu trả lời không khớp câu hỏi hoặc lặp menu. User sửa bằng cách hỏi lại theo cách khác, quay menu hoặc tự tìm hotline/email (fallback khó tìm). | Chi phí ước lượng thấp–trung bình (~0.001–0.01 USD/request). Latency khoảng 1–3 giây cho câu hỏi chuẩn. Rủi ro chính là AI trả lời sai chính sách ảnh hưởng uy tín/brand và UX vòng lặp làm user bực. |

---

## Automation hay augmentation?

☐ Automation — AI làm thay, user không can thiệp  
☑ Augmentation — AI gợi ý, user quyết định cuối cùng

**Justify:**  
Domain hàng không có rủi ro cao nếu thông tin sai. User có thể nhận ra AI sai nhưng khó sửa hoặc thoát nhanh, nên automation toàn phần là nguy hiểm. NEO nên đóng vai trò hỗ trợ và có fallback con người rõ ràng.

---

## Learning signal

| # | Câu hỏi | Trả lời |
|---|---------|---------|
| 1 | User correction đi vào đâu? | Log phản hồi tiêu cực, câu nói như “không đúng / không hiểu”, hành vi sửa câu hỏi và trigger chuyển tư vấn viên. |
| 2 | Product thu signal gì để biết tốt lên hay tệ đi? | Tỉ lệ chuyển sang tư vấn viên, số vòng lặp trong một session, tỉ lệ abandon chat và phản hồi tích cực/tiêu cực. |
| 3 | Data thuộc loại nào? ☐ User-specific · ☐ Domain-specific · ☐ Real-time · ☐ Human-judgment · ☐ Khác | ☑ Domain-specific · ☑ Real-time · ☑ Human-judgment |

**Có marginal value không?**  
Có. Đây là dữ liệu hội thoại thật và failure cases của hành khách Vietnam Airlines, không có sẵn trên internet và không sản phẩm khác thu được y hệt. Data này giúp cải thiện intent routing và xử lý khi AI sai.