# Sprint Plan - Family Health Chatbox

## 1. Team Setup

| Member | Role | Trách nhiệm chính |
|---|---|---|
| Member 1 | PO / PM | quản lý roadmap, ưu tiên backlog, làm việc với khách hàng, chốt scope |
| Member 2 | BA / QA | refine requirement, viết user story, acceptance criteria, test case, UAT |
| Member 3 | Tech Lead / Backend Dev | kiến trúc, auth, backend core, database, security |
| Member 4 | Frontend / Mobile Dev | UI cho bệnh nhân và gia đình, accessibility |
| Member 5 | Fullstack / Realtime / Integration Dev | chat, alert, dashboard, integration, CI/CD hỗ trợ |

## 2. Planning Principle

- 1 sprint = 2 tuần
- Sprint 0 để discovery + setup
- 4 sprint để ra MVP pilot
- mỗi sprint đều phải demo được giá trị thật
- không đưa geofence, IoT, auto-answer vào MVP

## 3. Phase Plan

| Phase | Mục tiêu | Scope chính |
|---|---|---|
| Phase 1 | ra MVP pilot nhanh nhất | auth, chat, directory, care request, bridge 3 bên, SOS kèm vị trí, thuốc, dashboard, family report |
| Phase 2 | mở rộng giá trị chăm sóc | video call, chat tư vấn có attachment, lịch sử đơn thuốc, chatbot tuyến đầu, escalation, trend, handover |
| Phase 3 | smart facility | geofence, escort, climate alert, IoT, kiosk |

## 4. Sprint 0 - Discovery & Setup

### Goal

- chốt MVP scope
- chuẩn hóa backlog
- sẵn sàng vào development

### Output

- PRD v1
- backlog đã refine
- empathy map / journey map chính
- wireframe chính
- clickable prototype cho home, chat, care request, SOS
- architecture draft
- environment setup

### Assignment

| Member | Task |
|---|---|
| Member 1 | workshop với khách hàng, chốt pain point và MVP boundary |
| Member 2 | viết BRD/FRD/user stories/AC/test approach |
| Member 3 | thiết kế kiến trúc, DB schema, auth approach |
| Member 4 | wireframe màn hình chính, accessibility rules, prototype usability |
| Member 5 | setup repo, CI/CD, notification/chat POC |

### Design Track bắt buộc trong Sprint 0

- empathy interview với ít nhất 1 nhóm người thân và 1 nhóm nhân viên y tế
- giả lập thao tác với người cao tuổi trên 3 flow:
  - mở app và gọi người thân
  - nhờ hỗ trợ
  - bấm SOS
- review tính khả thi của:
  - nút SOS 1 chạm
  - Siri Shortcut / voice trigger
  - smartwatch / wearable button


## 5. Sprint 1 - Foundation

### Goal

Đưa hệ thống lên khung dùng được với login, role, hồ sơ người dùng.

### Story scope

- UM-01
- UM-02
- UM-03
- UM-04
- UM-05
- UM-06
- UM-07
- UM-08
- UM-09
- UM-10
- CM-10

### Expected Demo

- login theo role
- admin tạo user
- liên kết người thân với bệnh nhân
- UI có accessibility foundation

### Assignment

| Member | Task |
|---|---|
| Member 1 | điều phối sprint, review với stakeholder |
| Member 2 | test case auth, user management, refine sprint 2 |
| Member 3 | auth, RBAC, user APIs, family linking backend |
| Member 4 | login, profile, family linking UI |
| Member 5 | admin UI, session handling, app shell, CI/CD |

## 6. Sprint 2 - Communication Core

### Goal

Ra sản phẩm tương tác thật giữa bệnh nhân, gia đình và y tá/bác sĩ sớm nhất có thể.

### Story scope

- UM-11
- CM-01
- CM-02
- CM-03
- CM-04
- CM-05
- CM-06
- CM-11
- CC-01
- CC-02
- CC-03
- CC-04

### Expected Demo

- bệnh nhân chat với gia đình
- bệnh nhân chat với y tá/phòng trực
- danh bạ theo ca hoạt động
- tạo care request và y tá nhận được
- bác sĩ/gia đình/bệnh nhân có luồng trao đổi chung

### Assignment

| Member | Task |
|---|---|
| Member 1 | chốt communication workflow với bệnh viện/viện dưỡng lão |
| Member 2 | test case chat, care request, role flow |
| Member 3 | chat backend, directory, shift mapping |
| Member 4 | patient/family chat UI, directory UI |
| Member 5 | realtime, care request queue, bridge thread, push notification |

## 7. Sprint 3 - Health Core

### Goal

Bổ sung lớp thông tin sức khỏe để biến sản phẩm giao tiếp thành công cụ chăm sóc có ngữ cảnh.

### Story scope

- HM-01
- HM-02
- HM-03
- HM-04
- HM-05
- HM-06
- HM-07
- HM-08
- HM-09
- RM-01
- RM-02
- RM-03
- RM-04
- RM-07

### Expected Demo

- bệnh nhân nhận nhắc thuốc
- bệnh nhân xác nhận uống thuốc
- y tá cập nhật chỉ số
- gia đình xem dashboard và summary đơn giản

### Assignment

| Member | Task |
|---|---|
| Member 1 | confirm medication flow với khách hàng |
| Member 2 | UAT prototype phần thuốc và dashboard |
| Member 3 | medication API, health check-in API, data rules |
| Member 4 | medication UI, patient dashboard UI |
| Member 5 | family dashboard, alert center, summary engine cơ bản |

## 8. Sprint 4 - Pilot Ready

### Goal

Hoàn thiện vòng MVP để đưa vào pilot thật.

### Story scope

- RM-05
- RM-06
- RM-08
- CC-05
- SE-01
- SE-02
- SE-03
- SE-07
- SE-08
- hardening
- bug fixing

### Expected Demo

- báo cáo ngày cho gia đình
- care request có trạng thái
- SOS hoạt động end-to-end kèm phòng/vị trí
- hệ thống đủ ổn định để pilot

### Assignment

| Member | Task |
|---|---|
| Member 1 | pilot plan, sign-off, release communication |
| Member 2 | regression, UAT, release checklist |
| Member 3 | backend hardening, audit log, performance tuning |
| Member 4 | family report UI, SOS UI, polishing |
| Member 5 | report generation, alert routing, deployment support |

## 9. Post-MVP Sprint Suggestion

## Sprint 5

- CM-07
- CM-08
- CM-12
- CM-13
- CM-14
- CM-15
- CM-16
- HM-14
- HM-15
- HM-16
- HM-12
- HM-13

## Sprint 6

- CM-17
- CM-18
- RM-09
- CC-06
- CC-07
- SE-04
- SE-09

## Sprint 7-8

- CM-09
- SE-05
- SE-06

## Sprint 9+

- FI-01
- FI-02
- FI-03
- FI-04

## 10. Capacity Note

Với team 5 người:
- PO/PM và BA/QA không nên bị dùng như dev capacity
- dev capacity thực tế = 3 người
- nên giữ buffer 15-20% mỗi sprint cho bug fix, refine và thay đổi nhỏ từ khách hàng

## 11. Risk-based Planning

Các hạng mục nên làm sớm vì rủi ro hoặc giá trị cao:
- auth + RBAC
- communication core
- chat and alert flow
- doctor-family-patient bridge
- care request
- SOS + location sharing
- medication reminder

Các hạng mục nên dời sau vì phụ thuộc cao:
- auto-answer
- geofence
- climate/IoT
- siri/voice trigger đa nền tảng
- lock-screen/kiosk theo nền tảng
- chatbot chuyên sâu vượt guardrail y khoa

## 12. KPI theo Sprint

| Sprint | KPI chính |
|---|---|
| Sprint 0 | backlog đã refine đủ cho Sprint 1 và 2 |
| Sprint 1 | login + role + family linking demo được |
| Sprint 2 | chat + care request + directory + bridge demo được |
| Sprint 3 | medication + health dashboard demo được |
| Sprint 4 | family report + SOS + pilot readiness pass |

## 13. MVP Release Checklist

- PRD và backlog được sign-off
- UAT pass cho flow thuốc, dashboard, chat, care request, SOS
- có tài khoản test cho từng role
- có guideline onboarding ngắn cho bệnh nhân/người thân/y tá
- có audit log cơ bản cho hành động nhạy cảm
- có monitoring và rollback plan tối thiểu
