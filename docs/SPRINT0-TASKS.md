# Sprint 0 — Top-MVP Task Breakdown

Tài liệu này tách các story priority cao (MVP) thành task nhỏ để sprint planning.

Format: Feature — link to backlog story — tasks

## User Management

- Authentication — [UM-01](docs/BACKLOG.md#L27)
  - UX: simple login/OTP screen + error states
  - Backend: `POST /auth/login`, `POST /auth/otp`
  - DB: `users`, `sessions` schema
  - Security: rate-limit OTP, store sessions (JWT)
  - Tests + QA: e2e login flows

- Session management — [UM-02](docs/BACKLOG.md#L28)
  - Backend: token refresh/expiry, session store
  - Frontend: silent refresh, logout handling
  - Tests: expiry and logout scenarios

- Logout — [UM-03](docs/BACKLOG.md#L29)
  - Frontend: logout CTA + confirm
  - Backend: revoke session endpoint

- Role-based Access Control — [UM-04](docs/BACKLOG.md#L35) & [UM-05](docs/BACKLOG.md#L36)
  - Design RBAC model and roles table
  - Middleware: check permissions on APIs/UI
  - Tests: forbidden/allowed access cases

- User admin (create/lock/update) — [UM-06](docs/BACKLOG.md#L42), [UM-07](docs/BACKLOG.md#L43), [UM-08](docs/BACKLOG.md#L44)
  - Backend: admin APIs (create, lock/unlock, update)
  - Frontend: admin UI screens
  - Validation and audit logging

- Family linking & visibility — [UM-09](docs/BACKLOG.md#L50) & [UM-10](docs/BACKLOG.md#L51)
  - Backend: relations table (patient↔relative)
  - Frontend: link flow and permission checks
  - Tests: data scoping per relation

## Health Management

- Medication scheduling & reminder setup — [HM-01](docs/BACKLOG.md#L65)
  - Backend: medication schedule model, scheduler worker
  - API: CRUD schedules, assign to patient
  - Integration: push notifications / local reminders

- Patient reminder receive & UI — [HM-02](docs/BACKLOG.md#L66)
  - Frontend: reminder card, confirm actions
  - Backend: deliver reminder events (realtime/push)

- Confirm medication taken — [HM-03](docs/BACKLOG.md#L67)
  - API: confirm endpoint, update adherence record
  - UI: button + feedback

- Family/staff view medication status — [HM-04](docs/BACKLOG.md#L68)
  - API: fetch adherence per patient
  - UI: status in dashboard

- Medication instruction fields — [HM-05](docs/BACKLOG.md#L74) & [HM-06](docs/BACKLOG.md#L75)
  - Data model: instruction text
  - UI: show on reminder card

- Health check-in & vitals — [HM-07](docs/BACKLOG.md#L89), [HM-08](docs/BACKLOG.md#L90), [HM-09](docs/BACKLOG.md#L91)
  - API: record vitals, timestamp + actor
  - UI: simple form for patient, staff input screen
  - Data retention and display in dashboard

## Reporting & Monitoring

- Health Dashboard (family) — [RM-01](docs/BACKLOG.md#L113)
  - API: aggregate latest vitals, adherence, alerts
  - UI: single-screen summary card
  - Metrics: define rules for `Ổn / Cần chú ý / Cần báo y tá`

- Patient-friendly status view — [RM-02](docs/BACKLOG.md#L114)
  - Simplified UI, large text

- Summary rules & reports — [RM-03](docs/BACKLOG.md#L120) — [RM-08](docs/BACKLOG.md#L135)
  - Implement rule engine or mapping table
  - Daily report generation + delivery (push/email)

## Communication

- Family chat (patient↔family) — [CM-01](docs/BACKLOG.md#L149) & [CM-02](docs/BACKLOG.md#L150)
  - Backend: message model, persistence, delivery
  - Realtime: websocket/Push for new messages
  - UI: large-font chat thread, send/receive
  - Tests: message ordering, offline sync

- Medical support chat (patient→nurse) — [CM-03](docs/BACKLOG.md#L156) & [CM-04](docs/BACKLOG.md#L157)
  - Routing rules to correct staff group
  - Notifications for staff portal

- Staff directory & quick-action — [CM-05](docs/BACKLOG.md#L171) & [CM-06](docs/BACKLOG.md#L172)
  - API: staff shift mapping + current on-duty
  - UI: tap-to-chat/call action

- Accessibility & primary actions — [CM-10](docs/BACKLOG.md#L191) & [CM-11](docs/BACKLOG.md#L192)
  - Design system: large font tokens, CTA rules
  - Implement global layout and accessibility checks

## Care Coordination

- 3‑way thread (doctor-family-patient) — [CC-01](docs/BACKLOG.md#L200) & [CC-02](docs/BACKLOG.md#L201)
  - Conversation model with role-based visibility
  - UI: create/join thread, permissions

- Care request flow (patient → nurse) — [CC-03](docs/BACKLOG.md#L207), [CC-04](docs/BACKLOG.md#L208), [CC-05](docs/BACKLOG.md#L209)
  - API: create request, change status (pending/in-progress/done)
  - Staff UI: queue + claim request
  - Notifications & SLA tracking

## Safety & Emergency

- Quick SOS — [SE-01](docs/BACKLOG.md#L229)
  - UI: persistent SOS CTA (1 tap)
  - Backend: SOS event ingestion
  - Notifications: push + high-priority alert routing

- SOS handling for staff — [SE-02](docs/BACKLOG.md#L230) & [SE-03](docs/BACKLOG.md#L231)
  - Staff portal: alert view with patient details
  - Escalation rules + acknowledgements

- SOS Location Sharing — [SE-07](docs/BACKLOG.md#L237) & [SE-08](docs/BACKLOG.md#L238)
  - Capture GPS or fallback to assigned room
  - Display location link / map in staff portal

## Cross-cutting tasks (apply to all features)

- Authentication & RBAC implementation
- API design & OpenAPI spec
- DB schema + migrations
- Realtime infra (WebSocket / PubSub) + Push notifications
- Logging / audit for PHI-sensitive actions
- Unit / integration / e2e tests for critical flows
- Deployment pipeline: staging + prod

---

If you want, tôi có thể:
- tạo issues/PRs cho mỗi task, hoặc
- xuất danh sách này thành GitHub Project cards.
