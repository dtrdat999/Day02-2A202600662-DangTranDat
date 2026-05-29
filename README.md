# Day 02 Lab — Tìm đúng bài toán cho AI

**Học viên:** Đặng Trần Đạt
**Mã học viên:** 2A202600662
**Repo:** Day02-2A202600662-DangTranDat

---

## Tổng quan bài nộp

Repo này là bài nộp Day 02 Lab với mục tiêu đi từ **vấn đề thực tế** đến **workflow rõ ràng**, sau đó đánh giá mức độ phù hợp giữa **No AI / Rule / Workflow / Agent**.

Trọng tâm của bài không phải là chọn AI thật “ngầu”, mà là xác định đúng vấn đề, hiểu rõ workflow hiện tại, tìm bottleneck, đặt success metric, xác định boundary và ra quyết định có nên dùng AI hay không.

---

## Cấu trúc bài nộp

| Phần | File                                                             | Nội dung chính                                                                                                                   |
| ---- | ---------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 01   | [01-individual-problem-scan.md](./01-individual-problem-scan.md) | Phần cá nhân: scan 5 problems, chọn top 3 Problem Cards, draft workflow trước/sau cho top 3.                                     |
| 02   | [02-group-problem-statement.md](./02-group-problem-statement.md) | Phần nhóm: group convergence, validation, research, workflow nhóm, Problem Statement, Rule / Workflow / Agent và final decision. |
| 03   | [03-individual-reflection.md](./03-individual-reflection.md)     | Reflection cá nhân: vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ thay đổi gì.                               |

---

## Candidate problem nhóm chọn

```text
Thông tin và hướng dẫn lab bị phân tán, thiếu một source of truth và luồng làm bài thống nhất.
```

---

## Lý do chọn problem này

Nhóm chọn problem này vì nó xuất hiện ở nhiều thành viên với các cách diễn đạt khác nhau. Các vấn đề như đề bài lab khó hiểu, slide/worksheet dài, không rõ phần nào là yêu cầu nộp, câu hỏi format bị lặp lại, hoặc thông tin nằm rải rác ở nhiều nơi đều có chung một pattern:

```text
Thông tin phân tán
→ người học phải tự ghép lại yêu cầu
→ dễ hỏi lại / hiểu lệch / làm thiếu
→ mentor hoặc TA phải giải thích lại
```

Problem này có:

* **Actor rõ:** học viên, nhóm học viên, mentor/TA.
* **Workflow rõ:** nhận bài → đọc nhiều nguồn → tự ghép yêu cầu → hỏi lại → làm bài → tự kiểm → nộp.
* **Bottleneck rõ:** học viên phải tự tổng hợp và xác nhận thông tin đúng từ nhiều nguồn.
* **Impact đo được:** thời gian hiểu yêu cầu, số câu hỏi lặp lại, số mục thiếu khi nộp.
* **Boundary rõ:** AI không tự đổi deadline, không chấm điểm, không tạo yêu cầu mới.

---

## Tóm tắt hướng giải quyết

Nhóm không chọn hướng xây một Agent tự động quyết định toàn bộ quy trình. Thay vào đó, nhóm chọn hướng **Workflow**:

```text
Source of truth
→ Checklist theo phase
→ AI hỗ trợ hỏi đáp theo tài liệu đã duyệt
→ AI hỗ trợ self-check bài nháp
→ Mentor/TA xử lý câu hỏi không chắc hoặc ngoại lệ
```

---

## Rule / Workflow / Agent

| Mức          | Kết luận                                                                                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Rule**     | Hữu ích cho checklist, FAQ, folder structure và các yêu cầu cố định. Nhưng chưa đủ khi học viên hỏi bằng nhiều cách khác nhau hoặc cần đối chiếu nhiều nguồn. |
| **Workflow** | Phù hợp nhất vì bài toán có luồng rõ, AI chỉ hỗ trợ một số bước cụ thể như hỏi đáp theo tài liệu và self-check bài nháp.                                      |
| **Agent**    | Chưa phù hợp vì quá rộng, nhiều rủi ro và chưa cần AI tự lập kế hoạch hay tự quyết định thay mentor/TA.                                                       |

---

## Final decision

```text
Go với scope nhỏ.
```

### Lý do

Problem rõ, actor rõ, workflow vẽ được và impact có thể đo. Tuy nhiên, nhóm không triển khai AI ở phạm vi lớn ngay. Hướng hợp lý là pilot nhỏ với:

1. Một source of truth duy nhất.
2. Checklist theo từng phase.
3. FAQ cho câu hỏi lặp lại.
4. AI hỗ trợ trả lời dựa trên tài liệu đã duyệt.
5. Mentor/TA kiểm tra các câu hỏi không chắc hoặc ngoại lệ.

---

## Pilot nhỏ nhất

```text
1. Gom các nguồn chính thức của một lab: worksheet, slide, README, ví dụ mẫu, checklist nộp bài.
2. Tạo một source of truth duy nhất.
3. Tạo checklist theo phase: cá nhân → nhóm → reflection → nộp bài.
4. Thu thập 20–30 câu hỏi thường gặp của học viên.
5. Cho AI trả lời thử các câu hỏi dựa trên source of truth.
6. Yêu cầu AI luôn gắn nguồn hoặc mục checklist liên quan.
7. Mentor/TA review câu trả lời theo 3 mức: đúng / cần sửa / sai nghiêm trọng.
8. Thử self-check 3–5 bài nháp để xem AI/checklist có phát hiện được phần thiếu không.
```

---

## Bài học chính

Qua bài lab này, tôi học được rằng một problem tốt không phải là problem nghe “AI” nhất, mà là problem có:

```text
Actor rõ
→ Workflow rõ
→ Bottleneck cụ thể
→ Metric đo được
→ Boundary an toàn
→ Decision có lý do
```

AI chỉ nên được dùng sau khi hiểu đúng workflow và xác định rõ phần nào AI được phép hỗ trợ. Trong case này, AI phù hợp nhất ở mức **Workflow**, không phải Agent.
