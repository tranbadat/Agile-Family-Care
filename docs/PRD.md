# PRD - Family Health Chatbox

## 1. Product Summary

Family Health Chatbox là nền tảng hỗ trợ chăm sóc sức khỏe và giao tiếp dành cho:
- bệnh viện
- viện dưỡng lão
- bệnh nhân/người cao tuổi
- gia đình bệnh nhân

Mục tiêu sản phẩm:
- giúp bệnh nhân thao tác cực đơn giản trong các nhu cầu thường ngày và khẩn cấp
- giúp gia đình theo dõi tình trạng người thân theo ngôn ngữ dễ hiểu
- giúp y tá/bác sĩ giao tiếp và phản hồi nhanh hơn
- giúp khách hàng tổ chức vận hành chăm sóc tốt hơn trong môi trường đổi ca liên tục

## 2. Business Goal

### Mục tiêu ngắn hạn

- ra MVP trong 4 sprint để pilot
- giải quyết 4 pain point lớn nhất:
  - quên uống thuốc
  - không hiểu tình trạng sức khỏe
  - khó gọi hỗ trợ
  - gia đình thiếu thông tin

### Mục tiêu trung hạn

- tăng tương tác gia đình - bệnh nhân - y tá/bác sĩ
- giảm thời gian phản hồi yêu cầu hỗ trợ
- tạo nền tảng mở rộng cho video call, chatbot, IoT, geofence

## 3. Personas

| Persona | Mô tả | Mục tiêu |
|---|---|---|
| Bệnh nhân cao tuổi | mắt mờ, tay run, dễ quên, ngại thao tác phức tạp | uống thuốc đúng giờ, gọi hỗ trợ nhanh, hiểu sức khỏe đơn giản |
| Người thân | không ở cạnh bố mẹ thường xuyên | biết hôm nay bố/mẹ có ổn không, nhận báo cáo và cảnh báo |
| Y tá | đổi ca liên tục, cần phản hồi yêu cầu chăm sóc | nhận đúng alert, xử lý nhanh, ít mất thời gian tìm thông tin |
| Bác sĩ | cần trao đổi với gia đình và bệnh nhân | có kênh giao tiếp rõ ràng, tránh rời rạc |
| Admin cơ sở chăm sóc | quản lý tài khoản, phân quyền, phòng, ca trực | vận hành trơn tru, kiểm soát truy cập |

## 4. Product Surfaces

Sản phẩm không chỉ là một hệ thống quản trị cho bệnh viện. Đây là hệ sinh thái gồm 2 mặt chính:

### 4.1 Patient & Family App

Đây là bề mặt sản phẩm chính, người dùng trực tiếp sử dụng hằng ngày:
- bệnh nhân/người cao tuổi
- gia đình/người thân

Mục tiêu:
- thao tác cực ít bước
- ưu tiên mobile/tablet app
- chữ lớn, nút lớn, thông điệp ngắn
- hỗ trợ chat, nhắc thuốc, xem tình trạng, gọi hỗ trợ, SOS

### 4.2 Staff & Admin Portal

Đây là bề mặt vận hành dành cho:
- y tá
- bác sĩ
- admin bệnh viện/viện dưỡng lão

Mục tiêu:
- quản lý user, phòng, ca trực
- cập nhật chỉ số sức khỏe
- nhận alert, xử lý care request, theo dõi tình trạng bệnh nhân

## 5. Problem Statement

Phần problem statement cần giữ ở mức đủ tổng quát để tránh lặp và để về sau còn mở rộng giải pháp. Thay vì liệt kê từng tình huống rất cụ thể, nên gom thành các nhóm vấn đề chính.

### 5.1 Nhóm vấn đề 1: Medication Adherence

Bệnh nhân cao tuổi thường:
- quên giờ uống thuốc
- không nhớ cách dùng thuốc
- không nhớ đơn cũ hoặc lịch sử dùng thuốc

Hệ quả:
- uống sai giờ
- uống sai trước/sau ăn
- gia đình và y tá khó kiểm tra tuân thủ thuốc

### 5.2 Nhóm vấn đề 2: Care Communication Continuity

Trong môi trường bệnh viện/viện dưỡng lão:
- y tá và bác sĩ đổi ca liên tục
- bệnh nhân không nhớ ai đang trực
- gia đình, bệnh nhân và bác sĩ nói chuyện qua nhiều kênh rời rạc

Hệ quả:
- chậm phản hồi
- thiếu thông tin ngữ cảnh
- ngại nhờ hỗ trợ

### 5.3 Nhóm vấn đề 3: Health Understanding Gap

Bệnh nhân và gia đình:
- không hiểu chỉ số y khoa
- không biết hôm nay tình trạng là ổn hay đáng lo
- không biết khi nào cần gọi y tá/bác sĩ

Hệ quả:
- lo lắng không cần thiết
- hoặc ngược lại, bỏ qua dấu hiệu quan trọng

### 5.4 Nhóm vấn đề 4: Emergency Access Friction

Khi gặp tình huống khẩn:
- bệnh nhân không thể mở khóa điện thoại rồi tìm đúng app
- tay run, mắt mờ, hoảng loạn
- nếu gọi SOS nhưng không có vị trí thì nhân viên khó tiếp cận nhanh

Hệ quả:
- mất thời gian phản ứng
- tăng rủi ro với ca té ngã, đau ngực, đi lạc

### 5.5 Nhóm vấn đề 5: Emotional Connection & Family Reassurance

Bệnh nhân:
- nhớ con cháu nhưng không dùng tốt app phổ thông

Gia đình:
- muốn biết bố mẹ hôm nay có ổn không
- muốn hỏi nhanh về thuốc, chỉ số, tình trạng hiện tại

Hệ quả:
- giảm kết nối tinh thần
- gia đình liên tục phải gọi thủ công để hỏi tình trạng

### 5.6 Nhóm vấn đề 6: Facility Safety & Environment

Trong viện dưỡng lão hoặc cơ sở chăm sóc:
- bệnh nhân có thể đi ra khỏi khu vực quen thuộc
- phòng có thể quá lạnh hoặc quá ẩm

Hệ quả:
- tăng nguy cơ đi lạc
- giảm sự thoải mái và an toàn trong chăm sóc

## 6. Capability Mapping: Từ vấn đề đến chức năng

| Nhóm vấn đề | Capability cần có | Module | Feature |
|---|---|---|---|
| Medication Adherence | nhắc thuốc đúng lịch | Health Management | Medication Reminder |
| Medication Adherence | hướng dẫn cách dùng thuốc ngắn gọn | Health Management | Medication Instruction |
| Medication Adherence | lưu đơn thuốc, ảnh đơn thuốc, lịch sử đơn thuốc | Health Management | Prescription Archive |
| Care Communication Continuity | hiển thị nhân sự đang trực theo phòng/ca | Communication | Staff Directory by Shift |
| Care Communication Continuity | chatbox giữa bệnh nhân - gia đình - nhân viên y tế | Communication | Family Chatbox / Medical Support Chat |
| Care Communication Continuity | chatbot tham gia tuyến đầu để hỏi đáp cơ bản và sàng lọc trước khi chuyển người thật | Communication | Frontline Health Chatbot |
| Care Communication Continuity | tư vấn qua chat có thể gửi ảnh đơn thuốc/tài liệu | Communication | Consultation Chat with Attachments |
| Health Understanding Gap | dashboard đơn giản | Reporting & Monitoring | Health Dashboard |
| Health Understanding Gap | diễn giải chỉ số thành kết luận dễ hiểu | Reporting & Monitoring | Simple Health Summary |
| Emotional Connection & Family Reassurance | báo cáo tình trạng định kỳ cho người thân | Reporting & Monitoring | Family Daily Report |
| Emergency Access Friction | SOS 1 chạm | Safety & Emergency | Quick SOS |
| Emergency Access Friction | SOS bằng giọng nói hoặc phím tắt hệ điều hành | Safety & Emergency | Voice SOS Trigger |
| Emergency Access Friction | gửi vị trí khi SOS | Safety & Emergency | SOS Location Sharing |
| Facility Safety & Environment | phát hiện đi lạc khỏi khu an toàn | Care Facility Integration | Safe Zone Monitoring |
| Facility Safety & Environment | cảnh báo môi trường phòng | Care Facility Integration | Room Climate Alert |

## 7. Requirement Refinement Notes

Một số nguyên tắc refine requirement:
- Problem statement không nên viết quá chi tiết kiểu từng tình huống lẻ, vì sẽ lặp và khó quản trị scope
- Requirement nên mô tả năng lực sản phẩm cần có
- Feature mới là nơi mô tả giải pháp cụ thể
- Cần phân biệt rõ:
  - `Patient & Family App`: dùng hằng ngày
  - `Staff & Admin Portal`: dùng để quản trị và vận hành

Ví dụ:
- Sai: "người già quên tên y tá nên ngại gọi"
- Đúng hơn: "bệnh nhân thiếu khả năng xác định đúng nhân sự hỗ trợ tại thời điểm hiện tại"
- Feature giải quyết: `Staff Directory by Shift`

Ví dụ:
- Sai: "bệnh nhân đau tim không mở khóa điện thoại được"
- Đúng hơn: "khả năng kích hoạt hỗ trợ khẩn cấp hiện tại có quá nhiều ma sát"
- Feature giải quyết:
  - `Quick SOS`
  - `Voice SOS Trigger`
  - `SOS Location Sharing`

Ví dụ:
- Sai: "chatbot tư vấn như bác sĩ"
- Đúng hơn: "hệ thống cần một lớp hỗ trợ giao tiếp tuyến đầu để giảm tải cho y tá/bác sĩ và hướng người dùng tới đúng kênh"
- Feature giải quyết:
  - `Frontline Health Chatbot`
  - `Consultation Chat with Attachments`
  - `Contact Escalation Rules`

## 8. Product Principles

- ưu tiên thao tác ít bước nhất cho bệnh nhân
- ngôn ngữ phải dễ hiểu, không đẩy biểu đồ y khoa phức tạp lên màn hình chính
- mọi alert quan trọng phải về đúng người, đúng thời điểm
- ưu tiên app cho bệnh nhân/gia đình; web portal cho staff/admin
- thiết kế phải theo logic accessibility-first cho người cao tuổi
- ưu tiên nút bấm trực tiếp trước, sau đó mới mở rộng voice và hardware
- chatbot chỉ đóng vai trò tư vấn cơ bản và điều phối giao tiếp, không thay thế bác sĩ/y tá
- MVP tránh phụ thuộc sâu vào hardware, IoT, wearable
- release sớm để pilot, lấy feedback thật trước khi mở rộng

Chi tiết phần thiết kế trải nghiệm xem thêm tại:
- [DESIGN-UX.md](/Users/tranbadat/Documents/study-projects/agile/docs/DESIGN-UX.md)

## 9. Module / Feature Breakdown

## 9.1 User Management

| Feature | Mô tả | Priority |
|---|---|---|
| Authentication | đăng nhập OTP/tài khoản nội bộ | Must |
| Role-based Access Control | phân quyền bệnh nhân, gia đình, y tá, bác sĩ, admin | Must |
| User Profile | hồ sơ người dùng cơ bản | Must |
| Family Linking | liên kết bệnh nhân với người thân | Must |
| Staff Shift Mapping | ánh xạ nhân viên theo ca trực/phòng | Should |
| User Administration | tạo/sửa/khóa tài khoản | Must |

## 9.2 Health Management

| Feature | Mô tả | Priority |
|---|---|---|
| Medication Reminder | nhắc giờ uống thuốc | Must |
| Medication Instruction | trước ăn/sau ăn/liều lượng | Must |
| Prescription Archive | lưu ảnh đơn thuốc, đơn thuốc hiện tại, lịch sử đơn thuốc | Should |
| Health Check-in | nhập và cập nhật chỉ số sức khỏe cơ bản | Must |
| Symptom Escalation | đẩy cảnh báo nếu có bất thường | Should |

## 9.3 Reporting & Monitoring

| Feature | Mô tả | Priority |
|---|---|---|
| Health Dashboard | dashboard tổng quan cho bệnh nhân/gia đình | Must |
| Simple Health Summary | kết luận dễ hiểu thay cho biểu đồ phức tạp | Must |
| Family Daily Report | báo cáo ngày cho người thân | Must |
| Trend Visualization | biểu đồ chi tiết hơn cho y tá/bác sĩ | Should |
| Alert Center | trung tâm thông báo/cảnh báo | Must |

## 9.4 Communication

| Feature | Mô tả | Priority |
|---|---|---|
| Family Chatbox | chat giữa bệnh nhân và gia đình | Must |
| Medical Support Chat | chat với y tá/bác sĩ/phòng trực | Must |
| Frontline Health Chatbot | chatbot tuyến đầu cho hỏi đáp cơ bản, thu thập triệu chứng ban đầu, chuyển tuyến sang người thật | Should |
| Consultation Chat with Attachments | gửi ảnh đơn thuốc, kết quả khám, tài liệu y tế trong chat | Should |
| Staff Directory by Shift | danh bạ theo ca trực | Must |
| Simplified Video Call | gọi audio/video đơn giản | Should |
| Auto Answer | tự động bắt máy cho người tin cậy | Could |
| Accessible UI | nút lớn, chữ lớn, ít bước | Must |

## 9.5 Care Coordination

| Feature | Mô tả | Priority |
|---|---|---|
| Doctor-Family-Patient Bridge | luồng trao đổi 3 bên | Must |
| Care Request | gửi yêu cầu hỗ trợ | Must |
| Shift Handover Notes | ghi chú bàn giao ca | Should |
| Contact Escalation Rules | rule alert theo mức độ | Should |

## 9.6 Safety & Emergency

| Feature | Mô tả | Priority |
|---|---|---|
| Quick SOS | gọi khẩn cấp 1 chạm | Must |
| SOS Location Sharing | gửi vị trí hiện tại hoặc vị trí phòng khi SOS | Must |
| Voice SOS Trigger | kích hoạt SOS bằng giọng nói hoặc shortcut hệ điều hành | Should |
| Fall / Distress Escalation | báo ngã/đau ngực và escalate | Should |
| Voice-guided Assistance | phát giọng nói hướng dẫn | Could |
| Lock-screen / Kiosk Entry | kích hoạt nhanh không cần flow dài | Could |

## 9.7 Care Facility Integration

| Feature | Mô tả | Priority |
|---|---|---|
| Safe Zone Monitoring | theo dõi ra khỏi khu vực an toàn | Could |
| Escort Alert | gọi y tá đến đón | Could |
| Room Climate Alert | cảnh báo môi trường phòng | Could |
| Facility Device Integration | tích hợp cảm biến/thiết bị | Could |

## 10. Scope Prioritization

### 10.0 Thứ tự ưu tiên đề xuất

Nếu mục tiêu là ra sản phẩm usable nhanh nhất và có tương tác thật giữa bệnh nhân, gia đình và nhân viên y tế, thì thứ tự ưu tiên nên là:

1. `Foundation`
2. `Care Communication`
3. `Emergency & Trust`
4. `Health Insight`
5. `Advanced Care`
6. `Smart Facility`

Lý do:
- `Care Communication` tạo giá trị sử dụng hằng ngày rất sớm và dễ thấy với khách hàng
- chat, danh bạ ca trực, care request và bridge 3 bên tạo ra pilot có tương tác thật
- các tính năng health insight như summary, dashboard, diễn giải chỉ số vẫn rất quan trọng nhưng có thể đến ngay sau khi luồng giao tiếp đã chạy
- `SOS + location` phải ở nhóm rất cao vì đây là tính năng niềm tin, ảnh hưởng trực tiếp đến độ tin cậy sản phẩm

## 10.1 MVP Scope

- Authentication
- Role-based Access Control
- Family Linking
- User Administration
- Staff Directory by Shift
- Family Chatbox
- Medical Support Chat
- Doctor-Family-Patient Bridge
- Care Request
- Quick SOS
- SOS Location Sharing
- Medication Reminder
- Medication Instruction
- Health Check-in
- Health Dashboard
- Simple Health Summary
- Family Daily Report
- Alert Center
- Accessible UI

## 10.2 Post-MVP Near Scope

- Prescription Archive
- Simplified Video Call
- Frontline Health Chatbot
- Consultation Chat with Attachments
- Symptom Escalation
- Trend Visualization
- Shift Handover Notes
- Contact Escalation Rules
- Fall / Distress Escalation
- Voice SOS Trigger

## 10.3 Long-term Scope

- Auto Answer
- Voice-guided Assistance
- Lock-screen / Kiosk Entry
- Safe Zone Monitoring
- Escort Alert
- Room Climate Alert
- Facility Device Integration

## 11. MVP Definition

MVP được xem là đạt nếu:
- bệnh nhân, gia đình và nhân viên y tế có thể tương tác với nhau trên cùng một nền tảng
- bệnh nhân nhận và hiểu nhắc thuốc
- bệnh nhân có thể gửi yêu cầu hỗ trợ thật nhanh
- nếu có SOS thì ca trực nhận được vị trí hoặc phòng để tiếp cận nhanh
- gia đình thấy được trạng thái cơ bản của người thân
- y tá/bác sĩ/gia đình có kênh giao tiếp tập trung

## 12. High-level User Flow MVP

### Flow 1: Medication

1. Admin/Y tá cấu hình lịch thuốc
2. Bệnh nhân nhận nhắc thuốc
3. Bệnh nhân xác nhận đã uống hoặc chưa uống
4. Gia đình/y tá thấy trạng thái cập nhật

### Flow 2: Health Monitoring

1. Y tá nhập chỉ số hoặc bệnh nhân check-in
2. Hệ thống tổng hợp
3. Dashboard hiển thị trạng thái dễ hiểu
4. Gia đình xem báo cáo ngày

### Flow 3: Support Request

1. Bệnh nhân bấm nhờ hỗ trợ hoặc SOS
2. Hệ thống gửi alert kèm phòng hoặc vị trí hiện tại
3. Gia đình được cập nhật nếu là trường hợp quan trọng

### Flow 4: Communication

1. Gia đình chat với bệnh nhân
2. Y tá tham gia trao đổi khi cần
3. Bác sĩ trao đổi 3 bên ở case điều trị quan trọng

### Flow 5: Consultation Support

1. Gia đình hoặc bệnh nhân mở chatbox tư vấn
2. Chatbot tuyến đầu trả lời câu hỏi cơ bản hoặc hỏi thêm triệu chứng/ngữ cảnh
3. Nếu vượt ngưỡng an toàn, chatbot chuyển tuyến sang y tá/bác sĩ hoặc gợi ý bấm SOS
4. Người dùng có thể gửi ảnh đơn thuốc hoặc tài liệu liên quan
5. Nhân viên y tế xem được ngữ cảnh và lịch sử trao đổi
6. Thông tin quan trọng có thể được lưu vào hồ sơ hoặc theo dõi tiếp

## 13.5 AI / Chatbot Safety Boundary

Chatbot chỉ được phép:
- giải thích thông tin đơn giản, dễ hiểu
- hướng dẫn cách dùng tính năng trong app
- nhắc lại thông tin thuốc đã được nhập sẵn trong hệ thống
- thu thập triệu chứng ban đầu theo kịch bản an toàn
- đề xuất chuyển sang y tá/bác sĩ hoặc kích hoạt SOS khi có dấu hiệu nguy cơ

Chatbot không được phép:
- chẩn đoán y khoa chuyên sâu
- kê đơn hoặc thay đổi thuốc
- khẳng định chắc chắn về bệnh lý
- thay thế quyết định chuyên môn của bác sĩ/y tá

## 14. Non-functional Requirements

- bảo mật và phân quyền dữ liệu sức khỏe
- log truy cập và log sự kiện quan trọng
- thông báo realtime hoặc gần realtime
- giao diện tối ưu cho người cao tuổi
- định vị trong SOS phải đủ nhanh, rõ nguồn vị trí và có fallback theo phòng/nơi ở
- chatbot phải có guardrail nội dung và log escalation
- hệ thống pilot phải đủ ổn định để demo thực địa

## 15. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Scope phình to quá sớm | chậm MVP | khóa MVP ngay Sprint 0 |
| Đòi hỏi IoT/geofence từ đầu | lệ thuộc phần cứng | tách phase sau |
| Tính năng auto-answer phụ thuộc nền tảng | rủi ro kỹ thuật | làm POC sau MVP |
| Voice trigger phụ thuộc Siri/Android shortcut | khác nhau theo nền tảng | đưa vào post-MVP và làm theo từng platform |
| Định vị trong tòa nhà có thể không chính xác | ảnh hưởng tốc độ tiếp cận | dùng fallback theo phòng, beacon hoặc vị trí cuối cùng |
| Chatbot trả lời quá phạm vi an toàn | rủi ro nghiệp vụ/pháp lý | giới hạn scope, guardrail, escalation bắt buộc |
| Người cao tuổi khó dùng | adoption thấp | test usability ngay Sprint 1-2 |
| Dữ liệu sức khỏe nhạy cảm | rủi ro bảo mật | RBAC, audit log, hạn chế truy cập |

## 16. Success Metrics

- 80% bệnh nhân pilot nhận được nhắc thuốc đúng giờ
- 70% người thân xem dashboard tối thiểu 3 lần/tuần
- thời gian từ care request đến y tá nhận alert < 10 giây
- thời gian từ SOS đến ca trực nhận được phòng/vị trí < 5 giây
- ít nhất 50% câu hỏi cơ bản được chatbot xử lý xong mà không cần nhân viên tiếp nhận trực tiếp
- giảm số trường hợp bệnh nhân không biết gọi ai khi đổi ca trực
- có ít nhất 1 khách hàng đồng ý pilot phase 2
