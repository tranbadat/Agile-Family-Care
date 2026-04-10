# Design Thinking & UI/UX - Family Health Chatbox

## 1. Mục tiêu tài liệu

Tài liệu này dùng để:
- định hướng thiết kế trải nghiệm theo `design thinking`
- chốt nguyên tắc UI/UX cho người cao tuổi
- mô tả luồng thao tác ưu tiên cho app bệnh nhân/gia đình
- xác định hướng mở rộng sang `voice`, `Siri Shortcut`, `smartwatch`, `hardware SOS`

Lưu ý:
- sản phẩm chính cho bệnh nhân/gia đình là `mobile/tablet app`
- web portal chủ yếu dành cho staff/admin
- trải nghiệm không nên bắt đầu từ dashboard phức tạp, mà bắt đầu từ các hành động rõ ràng: `gọi`, `chat`, `nhờ hỗ trợ`, `SOS`
- chatbot nên xuất hiện như một thành phần trong communication flow, không phải như bác sĩ thay thế

## 2. Design Thinking Framework

## 2.1 Empathize

Cần quan sát và phỏng vấn theo 3 nhóm:
- bệnh nhân/người cao tuổi
- người thân
- y tá/bác sĩ/admin

### Những gì cần quan sát

Đối với bệnh nhân:
- mất bao lâu để tìm đúng nút trên điện thoại
- có đọc được chữ nhỏ hay không
- có hiểu icon mà không có text hay không
- có nhớ đường đi nhiều bước hay không
- phản ứng khi căng thẳng hoặc hoảng loạn

Đối với người thân:
- họ cần biết thông tin gì đầu tiên khi mở app
- họ muốn xem báo cáo, chat hay gọi trước
- họ có sẵn sàng dùng app riêng thay vì Zalo/Facebook không

Đối với y tá/bác sĩ:
- họ cần thông tin gì đầu tiên khi nhận alert
- họ muốn nhận alert theo danh sách, chat thread hay call
- điều gì làm họ mất thời gian nhất trong ca trực

## 2.2 Define

Các bài toán trải nghiệm cốt lõi:

1. Bệnh nhân phải thực hiện được hành động quan trọng trong tối đa 1-2 thao tác.
2. Gia đình phải hiểu được tình trạng người thân trong dưới 10 giây nhìn đầu tiên.
3. Y tá phải biết ngay ai đang cần gì, ở đâu, mức độ khẩn thế nào.
4. Khi khẩn cấp, người dùng không được phụ thuộc vào việc nhớ flow trong app.

## 2.3 Ideate

Các hướng giải pháp ưu tiên:
- home screen theo `action-first` thay vì `information-first`
- nút lớn cho 4 hành động chính:
  - gọi người thân
  - nhắn tin
  - nhờ y tá hỗ trợ
  - SOS
- chatbot tuyến đầu trong màn hình chat để tiếp nhận câu hỏi cơ bản và chuyển tuyến nếu cần
- voice trigger cho tình huống không chạm được màn hình
- wearable/hardware button cho SOS nếu khách hàng có điều kiện triển khai

## 2.4 Prototype

Cần prototype trước 5 flow:
- mở app và gọi người thân
- chat với y tá
- gửi care request
- nhận nhắc thuốc và xác nhận uống thuốc
- SOS kèm vị trí

## 2.5 Test

Chỉ số usability tối thiểu:
- bệnh nhân hoàn thành thao tác `gọi người thân` trong <= 10 giây
- bệnh nhân hoàn thành thao tác `nhờ hỗ trợ` trong <= 8 giây
- bệnh nhân hoàn thành thao tác `SOS` trong <= 3 giây
- người thân hiểu tình trạng cơ bản trong <= 10 giây
- y tá xác định được vị trí và mức độ khẩn của alert trong <= 5 giây

## 3. Thiết kế sản phẩm theo bề mặt sử dụng

## 3.1 Patient App

Đây là bề mặt ưu tiên số 1.

Nguyên tắc:
- không nhồi nhiều thông tin
- ưu tiên text rõ hơn icon
- chỉ giữ 3-4 action chính trên home
- mọi tính năng phụ phải lùi xuống tầng sâu hơn

### 3.1.1 Home đề xuất

4 action chính:
- `Gọi người thân`
- `Nhắn tin`
- `Nhờ y tá`
- `SOS`

Thông tin phụ bên dưới:
- lịch uống thuốc kế tiếp
- trạng thái hôm nay: `Ổn / Cần chú ý / Đã có cảnh báo`
- tên y tá đang trực

## 3.2 Family App

Đây là bề mặt ưu tiên số 2.

Người thân cần thấy ngay:
- bố/mẹ hôm nay ổn không
- có alert nào không
- lịch thuốc có bị bỏ lỡ không
- có thể chat/gọi/tư vấn ngay không

Home family nên có:
- card tình trạng hôm nay
- card thuốc
- card alert
- nút chat/gọi
- nút xem báo cáo ngày

## 3.3 Staff Portal

Portal không cần “đẹp” bằng app người dùng cuối, nhưng phải rõ vận hành.

Y tá/bác sĩ cần thấy:
- danh sách bệnh nhân cần chú ý
- alert mới nhất
- care request đang chờ
- thread chat quan trọng
- vị trí/phòng của ca SOS

## 4. UX Principles cho người cao tuổi

## 4.1 Action-first

Màn hình đầu tiên không nên là dashboard dày đặc.

Đúng hơn:
- hiển thị hành động chính trước
- thông tin sức khỏe dạng tóm tắt sau

## 4.2 One-screen, one-purpose

Mỗi màn hình nên chỉ phục vụ một mục tiêu chính.

Ví dụ:
- màn hình nhắc thuốc: chỉ tập trung vào `uống thuốc nào`, `trước/sau ăn`, `đã uống/chưa uống`
- màn hình SOS: chỉ tập trung vào `kích hoạt`, `đang gửi vị trí`, `đã báo y tá`

## 4.3 Large target area

- nút tối thiểu lớn hơn chuẩn app thông thường
- khoảng cách giữa các nút đủ rộng
- không đặt 2 hành động nguy hiểm cạnh nhau

## 4.4 Text over icon

- icon phải đi kèm nhãn chữ
- không dùng icon “ẩn nghĩa”
- ưu tiên câu ngắn, động từ rõ

Ví dụ:
- đúng: `Nhờ y tá`
- kém rõ: icon chuông không có text

## 4.5 Reduce memory burden

Không bắt người dùng nhớ:
- tên y tá
- quy trình nhiều bước
- đơn thuốc cũ
- menu nằm ở đâu

Hệ thống phải hiển thị sẵn:
- người đang trực
- thuốc cần uống
- action chính
- lịch sử cần thiết

## 4.6 Anxiety-aware UX

Trong tình huống khẩn:
- giảm text dài
- giảm lựa chọn
- tăng feedback tức thì

Ví dụ khi bấm SOS:
- `Đang gửi báo động`
- `Đã gửi tới y tá trực`
- `Đã kèm vị trí/phòng`

## 5. Information Architecture đề xuất

## 5.1 Patient App

Bottom navigation hoặc home shortcuts:
- Home
- Chat
- Thuốc
- Sức khỏe
- Hồ sơ / Cài đặt

Trong đó:
- Home là trung tâm chính
- SOS luôn nổi bật và có thể truy cập từ mọi màn hình

## 5.2 Family App

- Home
- Chat
- Báo cáo
- Thuốc
- Hồ sơ bệnh nhân

## 5.3 Staff Portal

- Dashboard trực
- Care Requests
- Alerts
- Patients
- Chat Threads
- Shift & Directory

## 6. Key User Flows

## 6.1 Flow: Gọi người thân

1. Mở app
2. Bấm `Gọi người thân`
3. Chọn người thân ưu tiên hoặc auto chọn contact chính
4. Bắt đầu call

Thiết kế tốt nếu:
- không cần qua danh bạ phức tạp
- không cần nhập tay

## 6.2 Flow: Nhờ y tá hỗ trợ

1. Mở app
2. Bấm `Nhờ y tá`
3. Chọn nhanh lý do:
   - cần giúp đi lại
   - đau/mệt
   - cần thuốc
   - cần hỗ trợ khác
4. Gửi yêu cầu
5. App báo `Y tá đã nhận yêu cầu`

## 6.3 Flow: Medication Reminder

1. App hiện reminder toàn màn hình hoặc card nổi bật
2. Hiển thị:
   - tên thuốc
   - giờ uống
   - trước/sau ăn
   - liều dùng
3. Bệnh nhân bấm:
   - `Đã uống`
   - `Nhắc lại sau`

## 6.4 Flow: Consultation Chat

1. Người thân hoặc bệnh nhân mở chat tư vấn
2. Chatbot tuyến đầu tiếp nhận câu hỏi đầu tiên
3. Bot trả lời các câu cơ bản hoặc yêu cầu người dùng gửi ảnh đơn thuốc/tài liệu
4. Nếu nhận thấy vượt guardrail, bot chuyển hội thoại sang y tá/bác sĩ
5. Người thật xem lịch sử chat, attachment và tiếp tục tư vấn trong cùng thread

## 6.6 Flow: Chatbot Escalation

1. Người dùng hỏi: thuốc này uống sau ăn hay trước ăn
2. Bot tra thông tin đã được lưu trong hệ thống và trả lời ngắn gọn
3. Nếu người dùng hỏi sâu hơn như đổi thuốc, tăng liều, nghi ngờ bệnh nặng:
4. Bot không trả lời chuyên môn sâu
5. Bot hiển thị:
   - `Tôi sẽ chuyển câu hỏi này cho y tá/bác sĩ`
   - hoặc `Nếu đang khẩn cấp, vui lòng bấm SOS`

## 6.5 Flow: SOS

1. Bấm nút `SOS` hoặc kích hoạt bằng voice/shortcut
2. App gửi:
   - thông tin bệnh nhân
   - phòng hoặc vị trí hiện tại
   - thời điểm kích hoạt
3. Staff portal nhận alert
4. App phản hồi rõ: `Đã báo ca trực`

## 7. Voice & Hands-free Strategy

## 7.1 Quan điểm

Voice là hướng mở rộng quan trọng, nhưng không nên là cơ chế duy nhất.

Thứ tự ưu tiên đúng:
1. nút bấm lớn, dễ thấy
2. shortcut hệ điều hành
3. voice trigger
4. hardware wearable

## 7.2 Siri / Voice Assistant

Có thể nghiên cứu:
- `Siri Shortcut` trên iPhone/iPad
- `Google Assistant / Android shortcut` trên Android

Use cases phù hợp:
- `Gọi con trai`
- `Nhờ y tá`
- `SOS`

Lưu ý:
- phụ thuộc OS/platform
- cần flow fallback nếu voice fail
- nên đưa vào post-MVP gần

## 7.3 Voice UX Requirements

- câu lệnh phải rất ngắn
- phản hồi bằng âm thanh phải rõ
- nếu không hiểu lệnh, app phải chuyển về nút bấm thay vì vòng lặp phức tạp

## 8. Hardware & Wearable Strategy

## 8.1 Smartwatch / Wearable

Use case phù hợp:
- nút SOS trên đồng hồ
- xem tóm tắt sức khỏe cực ngắn
- nhắc thuốc rung hoặc hiển thị lớn

Lợi ích:
- giảm phụ thuộc vào điện thoại
- phù hợp khi bệnh nhân đang di chuyển hoặc không cầm máy

Rủi ro:
- chi phí thiết bị
- pin
- tương thích OS
- quản lý thiết bị cho cơ sở chăm sóc

## 8.2 Dedicated SOS Button

Hướng phần cứng đơn giản hơn wearable:
- nút SOS bedside
- wearable button đeo cổ hoặc cổ tay

Rất phù hợp cho:
- viện dưỡng lão
- bệnh nhân dễ té ngã
- người không dùng tốt smartphone

## 8.3 Indoor Location

Nếu muốn SOS thật sự hiệu quả trong facility:
- GPS ngoài trời là chưa đủ
- trong nhà cần fallback:
  - phòng/giường đã gán
  - Wi-Fi positioning
  - beacon/BLE
  - vị trí cuối cùng

## 9. Thiết kế tính năng SOS theo lớp

## 9.1 MVP

- nút SOS lớn trong app
- gửi phòng hoặc vị trí hiện tại nếu có
- staff portal nhận alert ngay
- gia đình được thông báo theo rule

## 9.2 Post-MVP

- Siri/voice shortcut
- lock-screen shortcut
- smartwatch shortcut
- indoor positioning nâng cao

## 9.3 Phase sau

- wearable button riêng
- tích hợp nurse call system
- phát hiện té ngã qua sensor/device

## 10. Design System Guidelines

## 10.1 Chatbot Interaction Guidelines

- bot phải tự giới thiệu là trợ lý hỗ trợ, không phải bác sĩ
- bot trả lời ngắn, từng bước
- bot nên ưu tiên:
  - giải thích dễ hiểu
  - điều hướng tính năng
  - thu thập thông tin ban đầu
  - chuyển tuyến
- bot không nên:
  - kê đơn
  - thay đổi thuốc
  - khẳng định chẩn đoán bệnh
  - làm người dùng nghĩ rằng đã được tư vấn y khoa đầy đủ

### Typography

- cỡ chữ lớn hơn chuẩn thông thường
- hạn chế dùng text quá dài trên CTA
- dùng font dễ đọc, độ tương phản cao

### Color

- tránh dùng màu mờ, low-contrast
- trạng thái phải nhất quán:
  - xanh: ổn
  - vàng/cam: cần chú ý
  - đỏ: khẩn cấp

### Motion

- animation rất nhẹ
- không làm người cao tuổi mất phương hướng
- ưu tiên feedback rõ hơn là hiệu ứng đẹp

### Sound

- nhắc thuốc nên có âm thanh dễ nhận biết
- SOS nên có feedback âm thanh xác nhận

## 11. Màn hình cần design trước

P0:
- Home bệnh nhân
- Home người thân
- Login
- Chatbox
- Staff Directory
- Care Request
- Medication Reminder
- SOS

P1:
- Dashboard sức khỏe
- Family Daily Report
- Consultation Chat với ảnh đính kèm
- Prescription Archive

P2:
- Video Call
- Voice SOS setting
- Wearable integration setting

## 12. Tiêu chí review UI/UX

Một màn hình chỉ được xem là đạt nếu:
- người cao tuổi hiểu mục tiêu màn hình trong 3 giây
- có 1 CTA chính rõ ràng
- không có quá 5 lựa chọn chính trên cùng màn hình
- không cần đọc nhiều để làm xong việc
- có trạng thái phản hồi sau hành động

## 13. Quyết định thiết kế quan trọng

- không thiết kế app kiểu dashboard-first
- không đẩy biểu đồ chi tiết lên home của bệnh nhân
- không phụ thuộc voice từ MVP đầu
- không phụ thuộc smartwatch/hardware từ MVP đầu
- nhưng phải thiết kế kiến trúc và UX mở để sau này tích hợp được

## 14. Deliverables thiết kế đề xuất

Cho Sprint 0:
- empathy map
- persona card
- current journey map
- future journey map
- information architecture
- wireframe low-fi
- prototype 5 flow chính
- usability checklist cho người cao tuổi

Cho trước cuối Sprint 1:
- UI kit cơ bản
- component rules accessibility
- high-fi prototype cho Home, Chat, Care Request, SOS
