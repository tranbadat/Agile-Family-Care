# Product Backlog - Family Health Chatbox

Lưu ý:
- File này dùng để refinement và estimation
- `SP Draft` là điểm gợi ý ban đầu để team estimate, không phải commit cuối
- `Target Sprint` là sprint đề xuất để lập kế hoạch, có thể thay đổi sau grooming

## 1. Thang Story Point đề xuất

| SP | Ý nghĩa |
|---|---|
| 1 | rất nhỏ, ít phụ thuộc |
| 2 | nhỏ |
| 3 | vừa |
| 5 | tương đối phức tạp |
| 8 | phức tạp, nhiều phụ thuộc |
| 13 | quá lớn, nên tách nhỏ thêm |

## 2. MVP Backlog

## 2.1 Module: User Management

### Feature: Authentication

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| UM-01 | Là bệnh nhân/người thân/nhân viên, tôi muốn đăng nhập bằng số điện thoại hoặc tài khoản được cấp để truy cập đúng vai trò của mình. | đăng nhập thành công; sai thông tin báo lỗi rõ; điều hướng đúng theo role | Must | 5 | Sprint 1 |
| UM-02 | Là hệ thống, tôi muốn duy trì phiên đăng nhập để người dùng không phải đăng nhập lại quá thường xuyên. | phiên còn hiệu lực theo thời gian cấu hình; logout xóa phiên | Must | 3 | Sprint 1 |
| UM-03 | Là người dùng, tôi muốn đăng xuất đơn giản để bảo vệ tài khoản của mình. | logout thành công; quay về màn hình đăng nhập | Must | 1 | Sprint 1 |

### Feature: Role-based Access Control

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| UM-04 | Là admin, tôi muốn hệ thống phân quyền theo vai trò để mỗi nhóm người chỉ thấy chức năng phù hợp. | role bệnh nhân, gia đình, y tá, bác sĩ, admin có menu và quyền khác nhau | Must | 5 | Sprint 1 |
| UM-05 | Là hệ thống, tôi muốn chặn truy cập trái phép vào dữ liệu sức khỏe của bệnh nhân. | API/UI kiểm tra quyền trước khi xem dữ liệu | Must | 5 | Sprint 1 |

### Feature: User Administration

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| UM-06 | Là admin, tôi muốn tạo tài khoản bệnh nhân, người thân và nhân viên để đưa họ vào hệ thống nhanh chóng. | tạo thành công; validate dữ liệu bắt buộc; hiển thị role đúng | Must | 5 | Sprint 1 |
| UM-07 | Là admin, tôi muốn khóa/mở khóa tài khoản để kiểm soát truy cập. | trạng thái thay đổi tức thời; tài khoản bị khóa không đăng nhập được | Must | 3 | Sprint 1 |
| UM-08 | Là admin, tôi muốn cập nhật hồ sơ cơ bản của người dùng. | sửa thông tin thành công; có validate đầu vào | Must | 3 | Sprint 1 |

### Feature: Family Linking

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| UM-09 | Là admin/y tá, tôi muốn liên kết bệnh nhân với người thân để người thân được quyền theo dõi đúng hồ sơ. | tạo liên kết thành công; người thân chỉ thấy bệnh nhân được gắn | Must | 5 | Sprint 1 |
| UM-10 | Là người thân, tôi muốn chỉ xem được thông tin của người thân đã được cấp quyền. | không xem được hồ sơ ngoài phạm vi được gắn | Must | 3 | Sprint 1 |

### Feature: Staff Shift Mapping

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| UM-11 | Là admin, tôi muốn gán y tá/bác sĩ theo phòng và ca trực để bệnh nhân luôn thấy đúng người đang trực. | cấu hình ca trực theo phòng; hiển thị đúng theo thời điểm hiện tại | Should | 5 | Sprint 2 |

## 2.2 Module: Health Management

### Feature: Medication Reminder

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| HM-01 | Là y tá/admin, tôi muốn cấu hình lịch thuốc cho bệnh nhân để hệ thống có thể nhắc đúng giờ. | tạo lịch theo giờ/ngày; gắn đúng bệnh nhân; lưu thành công | Must | 5 | Sprint 3 |
| HM-02 | Là bệnh nhân, tôi muốn được nhắc uống thuốc đúng giờ để không quên thuốc. | nhận được nhắc đúng lịch; màn hình hiển thị rõ tên thuốc và thời gian | Must | 5 | Sprint 3 |
| HM-03 | Là bệnh nhân, tôi muốn xác nhận đã uống thuốc hoặc chưa uống thuốc. | có nút xác nhận; trạng thái được lưu và hiển thị lại | Must | 3 | Sprint 3 |
| HM-04 | Là người thân/y tá, tôi muốn thấy trạng thái đã uống thuốc của bệnh nhân để biết có cần nhắc thêm không. | xem được trạng thái theo từng lịch thuốc | Must | 3 | Sprint 3 |

### Feature: Medication Instruction

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| HM-05 | Là bệnh nhân, tôi muốn thấy thuốc uống trước ăn hay sau ăn bằng câu ngắn gọn để tránh dùng sai. | hiển thị nhãn hướng dẫn rõ ràng, dễ đọc | Must | 2 | Sprint 3 |
| HM-06 | Là y tá/admin, tôi muốn nhập lưu ý dùng thuốc để bệnh nhân được hướng dẫn đúng. | lưu được chỉ dẫn ngắn; hiển thị tại reminder | Must | 2 | Sprint 3 |

### Feature: Prescription Archive

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| HM-14 | Là bệnh nhân hoặc người thân, tôi muốn chụp/gửi ảnh đơn thuốc để lưu lại và xem khi cần. | upload ảnh thành công; gắn đúng bệnh nhân; xem lại được | Should | 5 | Sprint 5 |
| HM-15 | Là người thân, tôi muốn xem lịch sử đơn thuốc để theo dõi việc điều trị qua thời gian. | hiển thị danh sách đơn theo thời gian; mở xem chi tiết được | Should | 5 | Sprint 5 |
| HM-16 | Là y tá/bác sĩ, tôi muốn xem nhanh đơn thuốc gần nhất trong lúc tư vấn để có thêm ngữ cảnh. | truy cập được từ hồ sơ/chat context nếu có quyền | Should | 3 | Sprint 5 |

### Feature: Health Check-in

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| HM-07 | Là y tá, tôi muốn nhập các chỉ số cơ bản của bệnh nhân để hệ thống lưu lịch sử sức khỏe. | lưu được huyết áp, nhịp tim, đường huyết, nhiệt độ hoặc mức đau | Must | 5 | Sprint 3 |
| HM-08 | Là bệnh nhân, tôi muốn tự check-in trạng thái như đau, mệt, khó chịu bằng vài lựa chọn đơn giản. | có form đơn giản; gửi thành công; y tá/gia đình thấy được nếu có quyền | Must | 3 | Sprint 3 |
| HM-09 | Là hệ thống, tôi muốn gắn thời gian và người cập nhật cho mỗi bản ghi sức khỏe. | mỗi bản ghi có timestamp và actor | Must | 2 | Sprint 3 |

### Feature: Symptom Escalation

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| HM-12 | Là hệ thống, tôi muốn tạo cảnh báo nếu bệnh nhân báo triệu chứng bất thường để y tá nhận biết sớm. | symptom cấu hình là nguy cơ cao thì sinh alert | Should | 5 | Sprint 5 |
| HM-13 | Là y tá, tôi muốn nhận được alert khi bệnh nhân báo đau ngực hoặc khó thở. | alert hiển thị realtime hoặc gần realtime | Should | 3 | Sprint 5 |

## 2.3 Module: Reporting & Monitoring

### Feature: Health Dashboard

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| RM-01 | Là người thân, tôi muốn xem dashboard sức khỏe của bố/mẹ trong một màn hình để biết hôm nay có ổn không. | hiển thị chỉ số gần nhất, trạng thái thuốc, alert gần đây | Must | 5 | Sprint 3 |
| RM-02 | Là bệnh nhân, tôi muốn xem trạng thái sức khỏe đơn giản của mình thay vì nhiều biểu đồ khó hiểu. | giao diện ít thông tin, chữ lớn, dễ đọc | Must | 3 | Sprint 3 |

### Feature: Simple Health Summary

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| RM-03 | Là hệ thống, tôi muốn chuyển các chỉ số thành trạng thái dễ hiểu như "ổn", "cần chú ý", "cần báo y tá". | có rules cơ bản; kết quả hiển thị rõ ràng | Must | 5 | Sprint 3 |
| RM-04 | Là người thân, tôi muốn hiểu huyết áp 140/90 là cao hay thấp mà không cần tự diễn giải. | summary giải thích ngắn gọn và nhất quán | Must | 3 | Sprint 3 |

### Feature: Family Daily Report

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| RM-05 | Là người thân, tôi muốn nhận báo cáo ngày về tình trạng của bố/mẹ để cập nhật nhanh. | báo cáo có trạng thái thuốc, check-in, cảnh báo nổi bật | Must | 5 | Sprint 4 |
| RM-06 | Là người thân, tôi muốn mở lại lịch sử báo cáo cũ để theo dõi theo ngày. | xem được danh sách báo cáo đã phát sinh | Must | 3 | Sprint 4 |

### Feature: Alert Center

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| RM-07 | Là người dùng, tôi muốn có một trung tâm thông báo để xem tất cả nhắc thuốc, care request và alert sức khỏe. | thông báo được gom một chỗ; có trạng thái đã đọc/chưa đọc | Must | 5 | Sprint 3 |
| RM-08 | Là y tá/người thân, tôi muốn thấy mức độ ưu tiên của từng alert để xử lý đúng việc trước. | alert có severity hoặc tag phân loại | Must | 3 | Sprint 4 |

### Feature: Trend Visualization

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| RM-09 | Là bác sĩ/y tá, tôi muốn xem biểu đồ lịch sử chỉ số để đánh giá xu hướng. | biểu đồ theo ngày/tuần; lọc theo loại chỉ số | Should | 5 | Sprint 6 |

## 2.4 Module: Communication

### Feature: Family Chatbox

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-01 | Là bệnh nhân, tôi muốn nhắn tin với người thân trong giao diện đơn giản để giữ liên lạc. | gửi/nhận tin nhắn thành công; chữ lớn; dễ dùng | Must | 5 | Sprint 2 |
| CM-02 | Là người thân, tôi muốn gửi tin nhắn cho bệnh nhân mà không cần app ngoài như Zalo/Facebook. | chat hoạt động trong app; có thông báo tin mới | Must | 3 | Sprint 2 |

### Feature: Medical Support Chat

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-03 | Là bệnh nhân, tôi muốn chat với y tá/phòng trực khi cần hỗ trợ để đỡ ngại gọi điện. | gửi tin nhắn tới đúng nhóm hỗ trợ | Must | 5 | Sprint 2 |
| CM-04 | Là y tá, tôi muốn thấy tin nhắn hỗ trợ của bệnh nhân trong cùng luồng để xử lý nhanh. | y tá nhận được và trả lời được | Must | 3 | Sprint 2 |

### Feature: Consultation Chat with Attachments

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-12 | Là bệnh nhân hoặc người thân, tôi muốn gửi ảnh đơn thuốc hoặc ảnh giấy tờ y tế trong chat để được tư vấn dễ hơn. | đính kèm ảnh thành công; hiển thị trong thread chat | Should | 5 | Sprint 5 |
| CM-13 | Là bác sĩ/y tá, tôi muốn xem lại ảnh đính kèm trong hội thoại để trả lời đúng ngữ cảnh. | xem được attachment trong lịch sử chat | Should | 3 | Sprint 5 |
| CM-14 | Là hệ thống, tôi muốn lưu lịch sử hội thoại tư vấn để gia đình và nhân viên y tế có thể xem lại khi cần. | lịch sử chat được lưu và truy xuất theo quyền | Should | 5 | Sprint 5 |

### Feature: Frontline Health Chatbot

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-15 | Là bệnh nhân hoặc người thân, tôi muốn hỏi chatbot các câu hỏi cơ bản về thuốc, chỉ số hoặc cách dùng app để nhận phản hồi nhanh trước khi cần tới người thật. | chatbot trả lời ngắn gọn, dễ hiểu, có disclaimer phù hợp | Should | 8 | Sprint 5 |
| CM-16 | Là chatbot, tôi muốn hỏi thêm một số câu ngắn về triệu chứng hoặc ngữ cảnh để sàng lọc ban đầu trước khi chuyển tuyến. | bot có flow hỏi-đáp kịch bản; không đi ngoài scope an toàn | Should | 8 | Sprint 5 |
| CM-17 | Là hệ thống, tôi muốn chatbot tự động chuyển sang y tá/bác sĩ khi câu hỏi vượt quá phạm vi an toàn hoặc có dấu hiệu nguy cơ. | escalation xảy ra theo rule; hội thoại được chuyển cùng ngữ cảnh | Should | 8 | Sprint 6 |
| CM-18 | Là quản trị/y tá, tôi muốn chatbot không được phép kê đơn, chẩn đoán chuyên sâu hoặc thay đổi thuốc. | có guardrail nội dung; câu trả lời vượt scope bị chặn hoặc chuyển tuyến | Should | 5 | Sprint 6 |

### Feature: Staff Directory by Shift

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-05 | Là bệnh nhân, tôi muốn thấy tên y tá/bác sĩ đang trực theo phòng để biết phải nhờ ai. | hiển thị đúng người theo phòng/ca hiện tại | Must | 5 | Sprint 2 |
| CM-06 | Là bệnh nhân, tôi muốn bấm vào tên y tá/bác sĩ để chat hoặc gửi yêu cầu hỗ trợ ngay. | action 1 chạm từ danh bạ | Must | 3 | Sprint 2 |

### Feature: Simplified Video Call

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-07 | Là bệnh nhân, tôi muốn gọi video cho người thân bằng giao diện tối giản để dễ thao tác. | gọi thành công; màn hình chỉ có nút chính | Should | 8 | Sprint 5 |
| CM-08 | Là người thân, tôi muốn gọi cho bệnh nhân ngay từ hồ sơ bệnh nhân. | gọi từ profile/chatbox được | Should | 5 | Sprint 5 |

### Feature: Auto Answer

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-09 | Là bệnh nhân, tôi muốn thiết lập người thân tin cậy có thể gọi vào và tự động bắt máy. | chỉ danh sách trust mới auto-answer; có on/off setting | Could | 13 | Sprint 7 |

### Feature: Accessible UI

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CM-10 | Là bệnh nhân cao tuổi, tôi muốn toàn bộ app có chữ lớn, nút lớn, ít thao tác để dễ dùng. | áp dụng style accessibility cho màn hình chính | Must | 5 | Sprint 1 |
| CM-11 | Là bệnh nhân, tôi muốn hành động chính luôn nằm ở vị trí dễ thấy như gọi người thân, nhờ hỗ trợ, SOS. | action quan trọng hiển thị nổi bật trên home | Must | 3 | Sprint 2 |

## 2.5 Module: Care Coordination

### Feature: Doctor-Family-Patient Bridge

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CC-01 | Là bác sĩ, tôi muốn có luồng trao đổi chung với bệnh nhân và gia đình để tránh mất thông tin. | tạo thread 3 bên; phân quyền đúng | Must | 8 | Sprint 2 |
| CC-02 | Là người thân, tôi muốn đọc được chỉ dẫn quan trọng của bác sĩ trong cùng luồng trao đổi. | nội dung hiển thị theo thread điều trị | Must | 3 | Sprint 2 |

### Feature: Care Request

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CC-03 | Là bệnh nhân, tôi muốn bấm 1 nút để nhờ y tá hỗ trợ mà không cần gõ dài dòng. | tạo request thành công; request đến đúng phòng trực | Must | 5 | Sprint 2 |
| CC-04 | Là y tá, tôi muốn thấy danh sách yêu cầu hỗ trợ đang chờ xử lý. | có trạng thái pending/in progress/done | Must | 5 | Sprint 2 |
| CC-05 | Là bệnh nhân/gia đình, tôi muốn biết yêu cầu đã được tiếp nhận hay chưa. | request có trạng thái và thời gian cập nhật | Must | 3 | Sprint 4 |

### Feature: Shift Handover Notes

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CC-06 | Là y tá, tôi muốn ghi chú bàn giao ca để ca sau nắm được tình trạng bệnh nhân. | lưu note theo ca và bệnh nhân | Should | 5 | Sprint 6 |

### Feature: Contact Escalation Rules

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| CC-07 | Là admin, tôi muốn cấu hình rule alert nào gửi cho y tá, alert nào gửi thêm gia đình hoặc bác sĩ. | cấu hình được theo loại sự kiện và mức độ | Should | 8 | Sprint 6 |

## 2.6 Module: Safety & Emergency

### Feature: Quick SOS

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-01 | Là bệnh nhân, tôi muốn có nút SOS lớn và dễ thấy để gọi hỗ trợ khẩn cấp ngay. | nút nổi bật; kích hoạt trong 1 thao tác; gửi alert thành công | Must | 5 | Sprint 4 |
| SE-02 | Là y tá/phòng trực, tôi muốn nhận alert SOS có thông tin bệnh nhân và phòng để phản ứng nhanh. | alert hiển thị tên, phòng, thời gian, loại khẩn | Must | 5 | Sprint 4 |
| SE-03 | Là gia đình, tôi muốn được thông báo nếu xảy ra sự cố nghiêm trọng. | gửi thông báo theo rule cấu hình | Must | 3 | Sprint 4 |

### Feature: SOS Location Sharing

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-07 | Là hệ thống, tôi muốn đính kèm vị trí hiện tại hoặc vị trí phòng khi bệnh nhân bấm SOS để ca trực tiếp cận nhanh hơn. | alert SOS có trường vị trí; có fallback theo phòng nếu không lấy được GPS | Must | 5 | Sprint 4 |
| SE-08 | Là y tá/bác sĩ trực, tôi muốn xem vị trí bệnh nhân trên bản đồ hoặc mô tả vị trí để di chuyển ngay. | mở được vị trí hoặc thông tin vị trí từ alert | Must | 5 | Sprint 4 |

### Feature: Voice SOS Trigger

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-09 | Là bệnh nhân, tôi muốn kích hoạt SOS bằng giọng nói hoặc shortcut hệ điều hành để không phải mở app khi đang hoảng loạn. | có ít nhất một cơ chế voice/shortcut khả thi theo từng nền tảng | Should | 8 | Sprint 6 |

### Feature: Fall / Distress Escalation

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-04 | Là bệnh nhân, tôi muốn báo "tôi bị ngã" hoặc "tôi đau ngực" thật nhanh để hệ thống nâng mức ưu tiên. | chọn nhanh symptom nguy cấp; alert severity cao | Should | 5 | Sprint 6 |

### Feature: Voice-guided Assistance

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-05 | Là bệnh nhân, tôi muốn nghe giọng nói hướng dẫn khi bị hoảng loạn để bình tĩnh hơn. | phát được audio hướng dẫn trong case định sẵn | Could | 5 | Sprint 8 |

### Feature: Lock-screen / Kiosk Entry

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| SE-06 | Là bệnh nhân, tôi muốn truy cập nhanh nút SOS hoặc nút gọi hỗ trợ mà không cần mở nhiều lớp ứng dụng. | có lối tắt hoặc mode kiosk theo giới hạn nền tảng | Could | 8 | Sprint 8 |

## 2.7 Module: Care Facility Integration

### Feature: Safe Zone Monitoring

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| FI-01 | Là cơ sở chăm sóc, tôi muốn biết khi bệnh nhân đi ra khỏi khu an toàn để giảm nguy cơ đi lạc. | phát hiện ra khỏi vùng đã cấu hình; sinh alert | Could | 13 | Sprint 9 |

### Feature: Escort Alert

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| FI-02 | Là hệ thống, tôi muốn tự động gọi y tá đến đón khi bệnh nhân đi lạc. | alert gửi đúng nhóm y tá được phân công | Could | 8 | Sprint 9 |

### Feature: Room Climate Alert

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| FI-03 | Là bệnh nhân, tôi muốn được báo nếu phòng quá lạnh hoặc quá ẩm để nhờ hỗ trợ điều chỉnh. | cảnh báo hiển thị rõ; có nút nhờ hỗ trợ | Could | 8 | Sprint 9 |

### Feature: Facility Device Integration

| ID | User Story | Acceptance Criteria | Priority | SP Draft | Target Sprint |
|---|---|---|---|---|---|
| FI-04 | Là hệ thống, tôi muốn tích hợp cảm biến hoặc thiết bị của cơ sở để tự động kích hoạt các cảnh báo môi trường/vị trí. | nhận dữ liệu từ thiết bị; map vào alert engine | Could | 13 | Sprint 10+ |

## 3. Ưu tiên shortlist để estimate trước

Team nên estimate trước các story dưới đây vì trực tiếp tạo ra MVP:
- UM-01 đến UM-10
- HM-01 đến HM-09
- RM-01 đến RM-08
- CM-01 đến CM-06
- CM-10 đến CM-11
- CC-01 đến CC-05
- SE-01 đến SE-03
- SE-07 đến SE-08

Các story estimate ở wave tiếp theo vì tạo lớp hỗ trợ giao tiếp thông minh:
- CM-12 đến CM-18
- HM-12 đến HM-13

## 4. Đề xuất Definition of Ready cho grooming

Một user story chỉ được đưa vào sprint khi:
- có persona rõ
- có value rõ
- có acceptance criteria rõ
- đã xác định dependency
- SP <= 8, nếu > 8 phải tách nhỏ thêm

## 5. Đề xuất Definition of Done

- code hoàn thành
- test case pass
- QA pass
- acceptance criteria pass
- log/audit phù hợp với feature nếu có
- được PO chấp nhận ở demo sprint
