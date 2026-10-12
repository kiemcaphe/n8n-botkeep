# n8n trên Botkeep Cloud

Repo cấu hình tối giản để deploy n8n lên Botkeep Cloud theo đường
**Application → Node.js** (panel không hỗ trợ Docker image tùy chỉnh).

- Panel clone repo này, chạy `npm install`, rồi start bằng `npm start` (= `n8n start`).
- Port: n8n mặc định 5678; panel cấp port qua biến môi trường thì cấu hình
  `N8N_PORT` trong panel cho khớp.
- Thư mục dữ liệu n8n (`~/.n8n`, chứa SQLite + credentials mã hoá) nằm trên disk
  của server Botkeep — export workflow JSON định kỳ về Google Drive 5TB để backup.
- Tài khoản owner/admin n8n do chủ sở hữu tự tạo ở lần mở URL đầu tiên.

Không commit secret, API key hay credential nào vào repo này.
