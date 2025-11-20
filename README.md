# Nail Salon Integrated System

簡介
- 一個為美甲店設計的整合系統，包含預約管理、顧客與服務項目管理、營收與報表、員工排班等功能。
- 目標是簡化店務流程、提升顧客體驗並方便店家管理日常營運。

主要功能
- 預約 (建立 / 修改 / 取消)
- 顧客資料管理（連絡資訊、歷史紀錄）
- 服務項目與價格設定

技術棧（範例）
- 後端：Node.js / Express 或 ASP.NET Core（依專案實際使用）
- 前端：React / Vue / Angular（依專案實際使用）
- 資料庫：MySQL / PostgreSQL / SQLite
- 身分驗證：JWT / OAuth（若需）
- 部署：Docker、Heroku、VPS 或 IIS

快速啟動（範例）
1. 先安裝必要環境：Node.js 16+、資料庫（MySQL 等）
2. 複製專案：
   - git clone <repo-url>
3. 安裝相依套件（以 Node 為例）：
   - npm install
4. 建立環境變數檔 .env，範例如下：
   - DB_HOST=localhost
   - DB_PORT=3306
   - DB_USER=root
   - DB_PASS=yourpassword
   - DB_NAME=nail_salon
   - JWT_SECRET=your_secret
5. 初始化資料庫 / migration：
   - npm run migrate 或 使用專案提供的 SQL
6. 啟動開發伺服器：
   - npm run dev
7. 開啟瀏覽器並前往：https://jenny-1014.github.io/Nail_Salon_Integrated_System/

設定說明
- env 檔案：將敏感資訊（資料庫密碼、JWT 金鑰）放在 .env，請勿上傳到版本控制。
- 資料庫：如果使用 migration 工具（如 Sequelize、TypeORM、EF Core），請執行 migration 指令建立資料表。
- 第三方服務（發簡訊、付款等）：將 API 金鑰設定至環境變數並在程式中讀取。

常見指令（範例）
- 安裝：npm install
- 開發：npm run dev
- 建置：npm run build
- 測試：npm run test
- migration：npm run migrate

部署
- 建議使用 Docker 建置映像並在伺服器上運行，或直接部署到支援 Node 的 PaaS。
- 設定環境變數於部署平台，確保資料庫可存取。

貢獻
- 歡迎提出 issue 或 PR，請在 PR 中說明修改內容與原因。
- 請遵守程式碼風格與測試標準。

聯絡
- 若需協助或有需求請留下聯絡方式／ issue。

授權
- 請在此填寫專案授權條款（例如 MIT License）。
