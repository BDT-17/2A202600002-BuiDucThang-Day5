# AI Product Canvas — template

Điền Canvas cho product AI của nhóm. Mỗi ô có câu hỏi guide — trả lời trực tiếp, xóa phần in nghiêng khi điền.

---

## Canvas

|   | Value | Trust | Feasibility |
|---|-------|-------|-------------|
| **Câu hỏi guide** | User nào? Pain gì? AI giải quyết gì mà cách hiện tại không giải được? | Khi AI sai thì user bị ảnh hưởng thế nào? User biết AI sai bằng cách nào? User sửa bằng cách nào? | Cost bao nhiêu/request? Latency bao lâu? Risk chính là gì? |
| **Trả lời** | **HR/Recruiters**<br>• Pain: AI hiring tools có bias (giới tính, trường học, keyword matching nguội)<br>• Giải pháp: Chatbot giải thích lỗi AI và hướng dẫn sửa<br>• Khác biệt: Không chỉ detect bias mà còn hướng dẫn fix cụ thể | **Ảnh hưởng nghiêm trọng:**<br>• Mất ứng viên giỏi (đặc biệt nữ/giỏi từ trường tầm trung)<br>• Giảm diversity, tăng rủi ro pháp lý<br>• User biết qua: tỷ lệ pass/fail theo giới tính, audit định kỳ<br>• User sửa: manual review, retrain model, ẩn thông tin nhạy cảm | **Cost thấp:**<br>• ~$0.001/request (hosting chatbot)<br>• Latency: <1s (client-side)<br>• Risk chính: Đưa advice sai → HR tin tưởng advice xấu<br>• Mitigation: human oversight, disclaimer |

---

## Automation hay augmentation?

☐ Automation — AI làm thay, user không can thiệp
☐ **Augmentation — AI gợi ý, user quyết định cuối cùng**

**Justify:** AI hiring bias rất nhạy cảm - nếu automation thì risk cao (loại nhầm ứng viên giỏi). Augmentation tốt hơn: AI gợi ý solutions, HR quyết định implement. Nếu AI sai, user vẫn có thể intervene.

---

## Learning signal

| # | Câu hỏi | Trả lời |
|---|---------|---------|
| 1 | User correction đi vào đâu? | Corrections từ HR (thêm lỗi mới, feedback về solutions) → update error database và chatbot responses |
| 2 | Product thu signal gì để biết tốt lên hay tệ đi? | • Diversity metrics cải thiện (tỷ lệ nữ tăng, trường non-top tăng)<br>• User satisfaction (survey sau mỗi session)<br>• Usage patterns (nhiều người dùng cùng lỗi = priority cao) |
| 3 | Data thuộc loại nào? ☐ User-specific · ☐ **Domain-specific** · ☐ Real-time · ☐ **Human-judgment** · ☐ Khác: HR feedback | |

**Có marginal value không?** (Model đã biết cái này chưa? Ai khác cũng thu được data này không?)
Model hiện tại chỉ có 5 lỗi phổ biến - marginal value cao vì:
• Không có public dataset về AI hiring bias errors
• Mỗi công ty có context riêng (văn hóa, quy mô)
• Human judgment từ HR experts rất valuable và unique

---

## Cách dùng

1. Điền Value trước — chưa rõ pain thì chưa điền Trust/Feasibility
2. Trust: trả lời 4 câu UX (đúng → sai → không chắc → user sửa)
3. Feasibility: ước lượng cost, không cần chính xác — order of magnitude đủ
4. Learning signal: nghĩ về vòng lặp dài hạn, không chỉ demo ngày mai
5. Đánh [?] cho chỗ chưa biết — Canvas là hypothesis, không phải đáp án

---

*AI Product Canvas — Ngày 5 — VinUni A20 — AI Thực Chiến · 2026*