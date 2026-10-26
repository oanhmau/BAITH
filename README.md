🌈✨ FinTrack — Ứng dụng Quản lý Chi tiêu Cá nhân Thông minh ✨🌈
<div align="center">
💸 Chi tiêu thông minh — Tương lai rạng ngời 💸
https://img.shields.io/badge/status-active-brightgreen
https://img.shields.io/badge/React-19-61DAFB
https://img.shields.io/badge/Node.js-Express-339933
https://img.shields.io/badge/AI-Gemini_3.8_Flash-4285F4
https://img.shields.io/badge/Queue-RabbitMQ_Pattern-FF6600

🔗 📦 Repository · 🎬 Demo Video · 📊 Slide Báo cáo · 🐛 Report Bug

🎓 Môn học: Lập trình Web Nâng cao
🏷️ Đề tài: Personal Finance Tracker — Quản lý chi tiêu cá nhân
⭐ Điểm nổi bật: AI Gemini · Event-Driven (RabbitMQ Pattern) · Validation 2 lớp · Trực quan hóa dữ liệu

</div>
📑 Mục lục
🎯 1. Giới thiệu & Bài toán

⚡ 2. Cài đặt & Khởi chạy

🏗️ 3. Kiến trúc Hệ thống

🔌 4. REST API

🔬 5. Kỹ thuật nổi bật

👥 6. Phân công

🎯 1. Giới thiệu & Bài toán giải quyết
🧩 Bài toán
🎯 Hỗ trợ người dùng (sinh viên 🎒, nhân viên văn phòng 💼) ghi chép thu/chi hàng ngày nhanh chóng ⚡, trực quan hóa dòng tiền 📈, và cảnh báo chủ động 🔔 khi chi tiêu vượt hạn mức ngân sách tháng.

✨ Tính năng chính
<table> <tr> <td width="50%">
📝 1. CRUD Giao dịch & Ảnh Locket
Thêm/Sửa/Xóa thu-chi với:

💰 Số tiền · 📂 Danh mục

🕐 Ngày giờ (GMT+7)

📝 Ghi chú · 💳 Phương thức thanh toán

📸 Ảnh hóa đơn kiểu Locket

📅 2. Dạng xem theo Lịch
🗓️ Lịch biểu từng ngày trong tháng

➕➖ Hiển thị thu (+) / chi (−)

🖼️ Icon ảnh Locket

📋 Ngăn kéo chi tiết khi click

🖼️ 3. Locket Moments
🌟 Tab thư viện ảnh chi tiêu

🎨 Widget Locket sinh động

📊 4. Thống kê & Biểu đồ
🍩 Donut chart theo danh mục

📊 Bar chart Thu vs Chi theo ngày

💵 Số dư ròng & Savings Rate

</td> <td width="50%">
💰 5. Ngân sách & Cảnh báo
Thiết lập ngân sách tổng & từng danh mục:

🟢 <70% — An toàn

🟠 70–90% — Cảnh giác

🔴 >90% / vượt — Báo động!

🤖 6. AI Gemini 3.8 Flash ⭐
Nhập tự nhiên:

💬 "Ăn trưa 50k"

💬 "Đổ xăng 70k"

💬 "Nhận lương 15 triệu"

→ 🪄 AI tự trích xuất số tiền + danh mục!
→ 🔗 Google AI Docs

🔀 7. Message Queue Simulation ⭐
📤 Topic Exchange

🎯 budget-evaluation-queue

🔔 notification-queue

🛡️ 8. Defense Mode
Nút demo cho Giảng viên:

🚫 Thử số âm

🚫 Thử nhập chữ cái

🚫 Thử bỏ trống danh mục

</td> </tr> </table>
⚡ 2. Cài đặt & Khởi chạy nhanh
<div align="center">
🚀 Chỉ cần 1 lệnh duy nhất
bash
npm install && npm run dev
🌐 Truy cập ngay
✨ http://localhost:3000 ✨

⚙️ Ứng dụng full-stack (Backend Express REST API + Frontend React Vite) tự động khởi động!

📚 Tài liệu tham khảo
📖 React 19 Documentation

📖 Vite Guide

📖 Express.js Guide

📖 Gemini API Quickstart

📖 RabbitMQ Tutorials

</div>
🏗️ 3. Kiến trúc Hệ thống
text
    ╔═══════════════════════════════════════════════════════════════╗
    ║              🎨  F R O N T E N D  (React 19)                 ║
    ║  ┌─────────────────────────────────────────────────────────┐ ║
    ║  │  🔤 Plus Jakarta Sans  ·  🎨 Tailwind CSS               │ ║
    ║  │  🎯 Lucide Icons       ·  📊 SVG Donut & Bar Charts     │ ║
    ║  │  ⚡ Client-side Realtime Input Validator                │ ║
    ║  └─────────────────────────────────────────────────────────┘ ║
    ╚═════════════════════════════╤═════════════════════════════════╝
                                  │
                       📡 HTTP / REST API (JSON)
                                  │
    ╔═════════════════════════════▼═════════════════════════════════╗
    ║              ⚙️  B A C K E N D  (Node.js / Express)           ║
    ║  ┌─────────────────────────────────────────────────────────┐ ║
    ║  │  🔌 REST: /api/transactions  ·  /api/budgets            │ ║
    ║  │  🛡️ Strict Validator (amount > 0, numeric, ISO)         │ ║
    ║  │  🌏 Timezone Normalizer (Asia/Ho_Chi_Minh · GMT+7)      │ ║
    ║  └─────────────────────────────────────────────────────────┘ ║
    ╚═══════════╤═══════════════════════════════════╤═══════════════╝
                │                                   │
    ╔═══════════▼═══════════════════╗  ╔════════════▼═══════════════╗
    ║   🤖 A I   S E R V I C E      ║  ║  🔀  M E S S A G E         ║
    ║  ┌──────────────────────────┐ ║  ║       Q U E U E            ║
    ║  │  ✨ Google GenAI SDK      │ ║  ║  ┌──────────────────────┐ ║
    ║  │  🧠 Gemini 3.8 Flash      │ ║  ║  │  📤 Topic Exchange    │ ║
    ║  │  📋 JSON Schema Extract   │ ║  ║  │  🎯 Budget Eval Q     │ ║
    ║  └──────────────────────────┘ ║  ║  │  🔔 Notification      │ ║
    ╚═══════════════════════════════╝  ║  └──────────────────────┘ ║
                                        ╚═══════════════════════════╝
🔗 Xem sơ đồ chi tiết: docs/architecture.md

🔌 4. REST API chính
📚 Swagger UI đầy đủ: http://localhost:3000/api-docs (nếu đã cấu hình)
🧪 Postman Collection: Tải về

🎯 Method	🛣️ Endpoint	📖 Mô tả
🟢 GET	/api/health	❤️ Kiểm tra trạng thái server & kết nối AI
🟢 GET	/api/transactions	📋 Danh sách giao dịch (lọc month/category/type/search)
🔵 POST	/api/transactions	➕ Tạo giao dịch (validate > 0, phát event Queue)
🟡 PUT	/api/transactions/:id	✏️ Cập nhật giao dịch
🔴 DELETE	/api/transactions/:id	🗑️ Xóa giao dịch
🟢 GET	/api/budgets	💰 Danh sách hạn mức & tiến độ chi tiêu %
🔵 POST	/api/budgets	⚙️ Thiết lập / cập nhật ngân sách
🟢 GET	/api/stats	📊 Thống kê số dư, Savings Rate, dữ liệu biểu đồ
🔵 POST	/api/ai/classify	🤖 AI phân tích NLP → entity giao dịch
🟢 GET	/api/queue	📬 Trạng thái hàng đợi & log worker
🟢 GET	/api/test/run	🧪 Chạy bộ kiểm thử tự động (6/6 cases)
🔵 POST	/api/reset	🔄 Khôi phục dữ liệu mẫu để demo lại
🔬 5. Kỹ thuật nổi bật (Phục vụ phản biện)
🛡️ 5.1 Validation 2 lớp cực chặt
text
        🚫 Số âm (≤ 0)      🚫 Ký tự chữ (NaN)      🚫 Bỏ trống danh mục
              │                    │                        │
              ▼                    ▼                        ▼
    ┌─────────────────────────────────────────────────────────────┐
    │  🎨 [Frontend Validator](https://github.com/your-org/fintrack/blob/main/src/components/TransactionModal.tsx)                          │
    │              ────────►                                       │
    │  🛡️ [Backend Controller](https://github.com/your-org/fintrack/blob/main/server.ts) (HTTP 400 Bad Request)                        │
    └─────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
                        ✅ Dữ liệu sạch 100%
💡 Form tích hợp cụm nút "🧪 Thử nghiệm Validate Nhanh" để Giảng viên kiểm chứng tức thì!

🌏 5.2 Xử lý Múi giờ (Timezone Isolation)
🕐 Lưu UTC timestamp trên server

🔄 Quy đổi sang Asia/Ho_Chi_Minh khi lọc theo tháng

✅ Tránh lỗi lệch giao dịch qua ngày mới (VD: 23:30 hôm nay ≠ 00:30 hôm sau)

📖 Tham khảo: MDN — Intl.DateTimeFormat

🧪 5.3 Bộ Test Runner Tự Động
🎯 Tab kiểm thử 1-click xác minh toàn diện — truy cập /api/test/run

🧪 Test	📋 Mô tả	✅ Kết quả
🚫	Validate số âm	PASS
🔤	Validate chữ cái	PASS
💰	Tính số dư	PASS
📬	Message Queue event-driven	PASS
🤖	AI Parsing	PASS
🛡️	Validation 2 lớp	PASS
👥 6. Phân công & Lộ trình Commit GitHub
⚠️ Yêu cầu chấm thi: Mỗi thành viên dùng tài khoản GitHub cá nhân để commit phần tương ứng — lịch sử commit phải khớp phân công để đạt điểm tối đa tiêu chí Kiểm thử & Đóng góp cá nhân (hệ số 1.0) 🏆

📊 Xem commit history: /commits/main

🌸 Thành viên 1 — Nguyễn Yến Nhi 24100372
📌 Nhiệm vụ	Khởi tạo repo · Backend Express · Data Models · CRUD Giao dịch & Validation 2 lớp
📂 Files	server.ts · src/types.ts · src/services/api.ts · package.json
👤 GitHub	@your-github-nhi
📊 Đóng góp	████████████░░░░░░░░ 25%
🌺 Thành viên 2 — Hoàng Nhật Bảo Trâm 24100260
📌 Nhiệm vụ	Giao diện React 19 · Header · Form thêm/sửa · Cụm nút demo · Danh sách & Export CSV
📂 Files	App.tsx · Header.tsx · TransactionModal.tsx · TransactionList.tsx · constants.ts
👤 GitHub	@your-github-tram
📊 Đóng góp	████████████░░░░░░░░ 25%
🌼 Thành viên 3 — Nguyễn Thuỳ Dương 24107946
📌 Nhiệm vụ	Biểu đồ SVG Donut & Bar · Module Ngân sách · Calendar View · Locket Gallery
📂 Files	CalendarView.tsx · LocketGalleryView.tsx · PhotoDetailModal.tsx · ChartsView.tsx · BudgetView.tsx
👤 GitHub	@your-github-duong
📊 Đóng góp	████████████░░░░░░░░ 25%
🌷 Thành viên 4 — Nguyễn Thị Kim Oanh 24100459
📌 Nhiệm vụ	AI Gemini 3.8 Flash & NLP Parser · Message Queue Monitor · Test Suite Runner · Slide & Báo cáo
📂 Files	AIQuickEntry.tsx · QueueMonitorModal.tsx · DefenseHubModal.tsx · README.md
👤 GitHub	@your-github-oanh
📊 Đóng góp	████████████░░░░░░░░ 25%
🧩 7. Công nghệ sử dụng
<div align="center">
🎨 Frontend	⚙️ Backend	🤖 AI & Queue	🛠️ Tooling
React 19	Node.js	Gemini 3.8 Flash	Vite
Tailwind CSS	Express	Google GenAI SDK	Git
Lucide Icons	TypeScript	RabbitMQ Pattern	npm
Plus Jakarta Sans	REST API	JSON Schema	ESLint
</div>
📞 8. Liên hệ & Hỗ trợ
<div align="center">
👤 Kênh	🔗 Link
📧 Email nhóm	fintrack.team@example.com
🐛 Bug Report	GitHub Issues
💡 Feature Request	GitHub Discussions
📖 Wiki	Project Wiki
🎬 Demo Video	YouTube Demo
📊 Slide thuyết trình	Google Slides
</div>
<div align="center">
🚀💎 FinTrack — Quản lý chi tiêu thông minh, minh bạch & trực quan 💎🚀
🌟 "Tiền không mua được hạnh phúc — nhưng quản lý tốt thì mua được sự an tâm!" 🌟

Made with ❤️ by Team FinTrack · 2024–2025

⬆️ Về đầu trang

text
💰 ═══════════════════════════════════════════════════════ 💰
     ✨ Track Smart · Spend Wise · Live Bright ✨
💰 ═══════════════════════════════════════════════════════ 💰
</div>
⚙️ 9. Ghi chú — Cách thay link thật
📌 Các link hiện tại là placeholder (dạng your-org, your-github-xxx, your-demo-id). Để biến thành link thật, các bạn tìm–thay toàn bộ (Ctrl+H / Cmd+H):

🔍 Placeholder	✅ Thay bằng
your-org/fintrack	<tên-org-hoặc-user>/fintrack (VD: nhom-fintrack/fintrack)
your-github-nhi	Username GitHub của Yến Nhi
your-github-tram	Username GitHub của Bảo Trâm
your-github-duong	Username GitHub của Thuỳ Dương
your-github-oanh	Username GitHub của Kim Oanh
your-demo-id	ID video YouTube demo
your-slide-id	ID Google Slides / Drive
your-slide-id (Google Drive)	ID file Drive báo cáo
