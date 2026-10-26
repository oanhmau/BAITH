🌈✨ FinTrack — Ứng dụng Quản lý Chi tiêu Cá nhân Thông minh ✨🌈
<div align="center">
💸 Chi tiêu thông minh — Tương lai rạng ngời 💸
https://img.shields.io/badge/status-active-brightgreen https://img.shields.io/badge/React-19-61DAFB https://img.shields.io/badge/Node.js-Express-339933 https://img.shields.io/badge/AI-Gemini_3.8_Flash-4285F4 https://img.shields.io/badge/Queue-RabbitMQ_Pattern-FF6600

🎓 Môn học: Lập trình Web Nâng cao
🏷️ Đề tài: Personal Finance Tracker — Quản lý chi tiêu cá nhân
⭐ Điểm nổi bật: AI Gemini · Event-Driven (RabbitMQ Pattern) · Validation 2 lớp · Trực quan hóa dữ liệu

</div>
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
text
✨ http://localhost:3000 ✨
⚙️ Ứng dụng full-stack (Backend Express REST API + Frontend React Vite) tự động khởi động!

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
🔌 4. REST API chính
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
    │  🎨 Frontend Validator  ────►  🛡️ Backend Controller       │
    │                                 (HTTP 400 Bad Request)      │
    └─────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
                        ✅ Dữ liệu sạch 100%
💡 Form tích hợp cụm nút "🧪 Thử nghiệm Validate Nhanh" để Giảng viên kiểm chứng tức thì!

🌏 5.2 Xử lý Múi giờ (Timezone Isolation)
🕐 Lưu UTC timestamp trên server

🔄 Quy đổi sang Asia/Ho_Chi_Minh khi lọc theo tháng

✅ Tránh lỗi lệch giao dịch qua ngày mới (VD: 23:30 hôm nay ≠ 00:30 hôm sau)

🧪 5.3 Bộ Test Runner Tự Động
🎯 Tab kiểm thử 1-click xác minh toàn diện:

🧪 Test	📋 Mô tả	✅ Kết quả
🚫	Validate số âm	PASS
🔤	Validate chữ cái	PASS
💰	Tính số dư	PASS
📬	Message Queue event-driven	PASS
🤖	AI Parsing	PASS
🛡️	Validation 2 lớp	PASS
👥 6. Phân công & Lộ trình Commit GitHub
⚠️ Yêu cầu chấm thi: Mỗi thành viên dùng tài khoản GitHub cá nhân để commit phần tương ứng — lịch sử commit phải khớp phân công để đạt điểm tối đa tiêu chí Kiểm thử & Đóng góp cá nhân (hệ số 1.0) 🏆

🌸 Thành viên 1 — Nguyễn Yến Nhi 24100372
<table> <tr><td width="100%">
📌 Nhiệm vụ: Khởi tạo repo · Backend Express · Data Models · CRUD Giao dịch & Validation 2 lớp

📂 Files phụ trách:
📄 server.ts · 📄 src/types.ts · 📄 src/services/api.ts · 📄 package.json

📊 Đóng góp: ████████████░░░░░░░░ 25%

</td></tr> </table>
🌺 Thành viên 2 — Hoàng Nhật Bảo Trâm 24100260
<table> <tr><td width="100%">
📌 Nhiệm vụ: Giao diện React 19 · Header · Form thêm/sửa · Cụm nút demo · Danh sách & Export CSV

📂 Files phụ trách:
📄 src/App.tsx · 📄 Header.tsx · 📄 TransactionModal.tsx · 📄 TransactionList.tsx · 📄 constants.ts

📊 Đóng góp: ████████████░░░░░░░░ 25%

</td></tr> </table>
🌼 Thành viên 3 — Nguyễn Thuỳ Dương 24107946
<table> <tr><td width="100%">
📌 Nhiệm vụ: Biểu đồ SVG Donut & Bar · Module Ngân sách · Calendar View · Locket Gallery

📂 Files phụ trách:
📄 CalendarView.tsx · 📄 LocketGalleryView.tsx · 📄 PhotoDetailModal.tsx · 📄 ChartsView.tsx · 📄 BudgetView.tsx

📊 Đóng góp: ████████████░░░░░░░░ 25%

</td></tr> </table>
🌷 Thành viên 4 — Nguyễn Thị Kim Oanh 24100459
<table> <tr><td width="100%">
📌 Nhiệm vụ: AI Gemini 3.8 Flash & NLP Parser · Message Queue Monitor · Test Suite Runner · Slide & Báo cáo

📂 Files phụ trách:
📄 AIQuickEntry.tsx · 📄 QueueMonitorModal.tsx · 📄 DefenseHubModal.tsx · 📄 README.md

📊 Đóng góp: ████████████░░░░░░░░ 25%

</td></tr> </table>
<div align="center">
🚀💎 FinTrack — Quản lý chi tiêu thông minh, minh bạch & trực quan 💎🚀
🌟 "Tiền không mua được hạnh phúc — nhưng quản lý tốt thì mua được sự an tâm!" 🌟

Made with ❤️ by Team FinTrack · 2024–2025

text
💰 ═══════════════════════════════════════════════════════ 💰
     ✨ Track Smart · Spend Wise · Live Bright ✨
💰 ═══════════════════════════════════════════════════════ 💰
</div>
