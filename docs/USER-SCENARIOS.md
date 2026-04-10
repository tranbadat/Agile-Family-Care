# User Scenarios - Family Health Chatbox

Tài liệu này dùng để hỗ trợ:
- thiết kế màn hình
- vẽ user flow
- chuẩn bị wireframe/prototype
- align giữa BA, Designer, Dev

Format mỗi kịch bản:
- `Actor`
- `Goal`
- `Trigger`
- `Pre-condition`
- `Main Flow`
- `Alternative / Exception`
- `Screens Involved`
- `Design Notes`

## 1. Kịch bản: Bệnh nhân mở app và dùng màn hình chính

### Actor

- Bệnh nhân cao tuổi

### Goal

- thực hiện nhanh một hành động quan trọng mà không bị rối

### Trigger

- bệnh nhân mở app vào đầu ngày hoặc khi cần hỗ trợ

### Pre-condition

- đã đăng nhập hoặc app đang giữ phiên

### Main Flow

1. Bệnh nhân mở app
2. App hiển thị `Home`
3. Trên Home có 4 nút lớn:
   - `Gọi người thân`
   - `Nhắn tin`
   - `Nhờ y tá`
   - `SOS`
4. Bên dưới là thông tin phụ:
   - lịch thuốc tiếp theo
   - trạng thái hôm nay
   - tên y tá đang trực
5. Bệnh nhân chọn một hành động chính

### Alternative / Exception

- nếu có alert quan trọng, Home hiển thị banner ưu tiên
- nếu sắp đến giờ thuốc, card thuốc được đẩy lên trên cùng

### Screens Involved

- Splash
- Home
- Alert Banner / Notification Center

### Design Notes

- Home phải là `action-first`
- không nhồi dashboard chi tiết lên trên cùng
- chữ lớn, CTA rõ, không quá 5 lựa chọn chính

## 2. Kịch bản: Bệnh nhân nhận nhắc thuốc

### Actor

- Bệnh nhân

### Goal

- biết ngay phải uống thuốc gì và xác nhận dễ dàng

### Trigger

- đến giờ uống thuốc

### Pre-condition

- y tá/admin đã cấu hình lịch thuốc

### Main Flow

1. App hiện card hoặc màn hình nhắc thuốc
2. Hiển thị:
   - tên thuốc
   - giờ uống
   - trước ăn / sau ăn
   - liều dùng
3. Bệnh nhân bấm:
   - `Đã uống`
   - hoặc `Nhắc lại sau`
4. Hệ thống cập nhật trạng thái
5. Gia đình/y tá thấy được kết quả

### Alternative / Exception

- nếu bệnh nhân không phản hồi, hệ thống tạo nhắc lại
- nếu bỏ lỡ nhiều lần, hệ thống có thể tạo alert cho người thân/y tá

### Screens Involved

- Medication Reminder Popup / Screen
- Medication History
- Alert Center

### Design Notes

- chỉ nên có 2 CTA chính
- thông tin phải cực ngắn
- tránh bắt bệnh nhân đọc đoạn mô tả dài

## 3. Kịch bản: Bệnh nhân gọi người thân

### Actor

- Bệnh nhân

### Goal

- gọi cho người thân nhanh nhất có thể

### Trigger

- bệnh nhân nhớ con cháu hoặc muốn trao đổi nhanh

### Pre-condition

- đã có contact người thân chính

### Main Flow

1. Bệnh nhân vào Home
2. Bấm `Gọi người thân`
3. App hiển thị:
   - người thân chính
   - hoặc 2-3 contact ưu tiên
4. Bệnh nhân chọn một người
5. Cuộc gọi được bắt đầu

### Alternative / Exception

- nếu người thân không bắt máy, app gợi ý gọi người tiếp theo
- ở phase sau có thể có `Auto Answer` cho chiều ngược lại

### Screens Involved

- Home
- Quick Call List
- Calling Screen

### Design Notes

- không nên bắt bệnh nhân vào danh bạ quá sâu
- nên có avatar, tên lớn, quan hệ như `Con trai`, `Con gái`

## 4. Kịch bản: Bệnh nhân nhờ y tá hỗ trợ

### Actor

- Bệnh nhân

### Goal

- gửi yêu cầu hỗ trợ mà không cần gõ nhiều

### Trigger

- cần giúp đi lại, cần thuốc, cảm thấy mệt, cần hỗ trợ khác

### Pre-condition

- có mapping phòng và ca trực

### Main Flow

1. Bệnh nhân vào Home
2. Bấm `Nhờ y tá`
3. App hiển thị các lý do chọn nhanh:
   - đau/mệt
   - cần thuốc
   - cần giúp đi lại
   - cần hỗ trợ khác
4. Bệnh nhân chọn lý do
5. Hệ thống gửi request đến ca trực
6. App báo `Y tá đã nhận yêu cầu` hoặc `Đã gửi yêu cầu`

### Alternative / Exception

- nếu bệnh nhân không chọn được lý do, có nút `Gửi nhanh`
- nếu request chưa ai nhận trong thời gian cấu hình, hệ thống escalate

### Screens Involved

- Home
- Care Request Quick Options
- Request Status Screen
- Staff Portal Request Queue

### Design Notes

- màn hình này nên ưu tiên lựa chọn bằng nút lớn
- không bắt nhập text ở bước đầu

## 5. Kịch bản: Gia đình xem tình trạng hôm nay của bố/mẹ

### Actor

- Người thân

### Goal

- hiểu ngay hôm nay bố/mẹ có ổn không

### Trigger

- mở app để kiểm tra tình trạng

### Pre-condition

- bệnh nhân đã được liên kết với tài khoản người thân

### Main Flow

1. Người thân mở app
2. App hiển thị Home của người thân
3. Home có các card:
   - trạng thái hôm nay
   - thuốc gần nhất
   - alert đang mở
   - y tá đang trực
4. Người thân chạm vào card để xem sâu hơn nếu cần

### Alternative / Exception

- nếu có alert đỏ, card alert phải nổi bật trên cùng
- nếu chưa có dữ liệu hôm nay, app hiển thị trạng thái “chưa cập nhật”

### Screens Involved

- Family Home
- Health Dashboard
- Alert Detail
- Family Daily Report

### Design Notes

- card đầu tiên phải trả lời câu hỏi: `Hôm nay có ổn không?`
- không bắt người thân tự diễn giải biểu đồ ở màn hình đầu

## 6. Kịch bản: Gia đình hoặc bệnh nhân chat tư vấn

### Actor

- Bệnh nhân
- Người thân

### Goal

- hỏi nhanh về thuốc, chỉ số hoặc tình trạng

### Trigger

- có thắc mắc nhưng chưa chắc cần bác sĩ/y tá trực tiếp

### Pre-condition

- hệ thống có chat và chatbot tuyến đầu

### Main Flow

1. Người dùng mở `Chat`
2. Chọn `Tư vấn`
3. Chatbot tuyến đầu tiếp nhận câu hỏi
4. Người dùng hỏi bằng text hoặc gửi ảnh đơn thuốc
5. Bot trả lời nếu câu hỏi nằm trong scope an toàn
6. Nếu vượt guardrail, bot chuyển tiếp sang y tá/bác sĩ
7. Người thật tiếp tục trong cùng thread

### Alternative / Exception

- nếu câu hỏi có dấu hiệu nguy cơ cao, bot gợi ý `Nhờ y tá ngay` hoặc `SOS`
- nếu attachment lỗi upload, hệ thống cho phép thử lại

### Screens Involved

- Chat List
- Consultation Thread
- Attachment Preview
- Escalation State

### Design Notes

- phải hiển thị rõ người dùng đang chat với `Bot` hay `Người thật`
- bot cần disclaimer ngắn gọn
- attachment phải dễ gửi với người thân

## 7. Kịch bản: Bác sĩ trao đổi 3 bên với gia đình và bệnh nhân

### Actor

- Bác sĩ
- Gia đình
- Bệnh nhân

### Goal

- trao đổi trong một thread chung, không thất lạc thông tin

### Trigger

- case điều trị cần giải thích hoặc theo dõi sát

### Pre-condition

- bác sĩ có quyền truy cập bệnh nhân
- gia đình đã được liên kết

### Main Flow

1. Bác sĩ tạo hoặc mở `Doctor-Family-Patient Thread`
2. Bác sĩ gửi cập nhật/chỉ dẫn
3. Gia đình đọc và hỏi lại trong cùng thread
4. Bệnh nhân hoặc y tá bổ sung tình trạng thực tế
5. Tất cả lịch sử được lưu cùng một chỗ

### Alternative / Exception

- nếu thông tin chỉ dành cho staff, bác sĩ có thể dùng note nội bộ riêng

### Screens Involved

- Shared Medical Thread
- Patient Context Side Panel
- Internal Note Panel

### Design Notes

- cần phân biệt rõ `message chung` và `note nội bộ`
- cần hiển thị context bệnh nhân ở cạnh thread cho staff

## 8. Kịch bản: Bệnh nhân kích hoạt SOS

### Actor

- Bệnh nhân

### Goal

- gọi hỗ trợ khẩn cấp nhanh nhất

### Trigger

- đau ngực, té ngã, khó thở, hoảng loạn

### Pre-condition

- app đang cài trên thiết bị

### Main Flow

1. Bệnh nhân bấm nút `SOS`
2. App lập tức gửi:
   - thông tin bệnh nhân
   - phòng hoặc vị trí hiện tại
   - thời gian kích hoạt
3. Staff portal nhận alert đỏ
4. Gia đình nhận thông báo nếu rule cho phép
5. App phản hồi:
   - `Đã gửi SOS`
   - `Đã báo ca trực`

### Alternative / Exception

- nếu không lấy được GPS, fallback theo phòng hoặc vị trí cuối
- ở phase sau có thể kích hoạt bằng Siri Shortcut, voice, smartwatch

### Screens Involved

- Home
- SOS Confirmation / Sending
- SOS Success State
- Staff Alert Screen

### Design Notes

- không nên có nhiều bước xác nhận
- có thể dùng hold 1 giây thay vì popup confirm dài dòng
- feedback phải tức thì

## 9. Kịch bản: Staff nhận SOS và đi đến bệnh nhân

### Actor

- Y tá / bác sĩ trực

### Goal

- biết ngay ai cần hỗ trợ, ở đâu, mức độ nào

### Trigger

- có SOS hoặc alert khẩn cấp

### Pre-condition

- staff đang đăng nhập portal/app trực

### Main Flow

1. Staff nhận alert khẩn
2. Màn hình hiển thị:
   - tên bệnh nhân
   - phòng
   - vị trí nếu có
   - loại alert
   - thời gian kích hoạt
3. Staff bấm `Nhận xử lý`
4. Hệ thống cập nhật trạng thái
5. Sau xử lý, staff có thể ghi chú ngắn

### Alternative / Exception

- nếu staff không phản hồi trong thời gian giới hạn, alert được escalate

### Screens Involved

- Alert Center
- SOS Detail
- Map / Location View
- Resolution Form

### Design Notes

- phải tối ưu cho việc đọc rất nhanh
- severity, vị trí và CTA `Nhận xử lý` là quan trọng nhất

## 10. Kịch bản: Tích hợp voice hoặc smartwatch ở phase sau

### Actor

- Bệnh nhân

### Goal

- gọi hỗ trợ mà không cần mở app

### Trigger

- không tiện chạm điện thoại

### Pre-condition

- có cấu hình Siri Shortcut / voice shortcut / wearable

### Main Flow

1. Người dùng nói câu lệnh ngắn hoặc bấm nút trên đồng hồ
2. Hệ thống kích hoạt flow tương ứng:
   - gọi người thân
   - nhờ y tá
   - SOS
3. Alert/call được gửi như flow trong app

### Alternative / Exception

- nếu voice fail, app gợi ý fallback về nút bấm
- nếu wearable mất kết nối, dùng điện thoại làm fallback

### Screens Involved

- Voice Shortcut Setup
- Wearable Integration Setup
- SOS / Care Request receiving screens

### Design Notes

- feature này không phải MVP đầu
- nhưng cần được tính từ sớm trong thiết kế hệ thống và interaction model

## 11. Danh sách màn hình nên vẽ trước từ các kịch bản

P0:
- Patient Home
- Family Home
- Login
- Medication Reminder
- Chat List
- Consultation Thread
- Care Request
- Staff Directory
- SOS Sending / Success
- Staff Alert Center

P1:
- Health Dashboard
- Family Daily Report
- Shared Medical Thread
- Request Status
- Prescription Archive

P2:
- Voice Shortcut Setup
- Wearable Setup
- Auto Answer Settings

