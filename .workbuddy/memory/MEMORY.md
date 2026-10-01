# 免費AI聊天 專案（長期記事）

手機端單檔 AI 導航 launcher，主檔 `C:/Users/hsiu/WorkBuddy/Claw/免費AI聊天/index.html`。

- 預設 AI = 元寶；開啟自動跳轉（location.href 同分頁、無彈窗）；用 sessionStorage `launched` 防止「按返回鍵」回來後又重跳。
- 右下角小膠囊選擇器（WorkBuddy 風格）→ 緊湊下拉選單切換 AI。
- 設定頁：貼網址新增/移除自訂 AI、設預設；自訂資料存 localStorage。
- `?noredirect` 停用自動跳轉（預覽/除錯用）。
- 加入桌面/安裝功能暫緩（iPhone 不能用 JS 觸發「加入主畫面」；Android 需 HTTPS+manifest）。
- 本機低 RAM（~0.6GB）：驗證用 node 虛擬 DOM 跑邏輯，不跑 headless Chrome。
