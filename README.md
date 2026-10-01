# AI 助手（AI Assistant Launcher）

一款**單檔、零相依、離線可用**的手機端 AI 導航啟動器。一個 HTML 檔案搞定：開啟即自動進入你的預設 AI，框內切換、自訂 AI、拖動排序、分割畫面，全部都在瀏覽器本機完成，不上傳任何資料。

> © 2026 修哥 (hsiu) — 採 [MIT License](LICENSE) 開源，歡迎自由下載、修改、散佈。

> 🌐 **線上試用**：https://hsiu1214.github.io/ai-assistant-launcher/

## ✨ 特色

- **📦 單檔零相依**：整個 App 就是一個 `index.html`，不用安裝、不用伺服器、離線可開。
- **🚀 開啟即用**：啟動自動載入預設 AI（預設為騰訊元寶，可更改）。
- **🖼 框內顯示**：AI 網頁直接內嵌在 App 框架中，底部切換列永遠在，切換 AI 不跳離頁面。
- **🧩 桌面分割畫面**：電腦寬螢幕（≥820px）可切 1 / 2 / 3 / 4 窗格，每格獨立選 AI、分隔條可拖拉調比例。
- **🎛 自訂 AI**：貼上任意 AI 聊天網址即可新增（可自訂名稱），內建 AI 也能編輯名稱與網址。
- **↕️ 拖動排序**：設定頁拖動把手自由排序，選單與分割窗格順序同步。
- **⭐ 一鍵設預設 / 還原**：任一 AI 可設為啟動預設；誤刪可一鍵還原內建清單。
- **🌙 深色模式**：跟隨手機系統自動切換外殼配色。
- **🔒 隱私本機化**：所有設定存於瀏覽器 localStorage，不會上傳。
- **📱 PWA 可安裝**：附 `manifest.webmanifest` + Service Worker，手機/電腦「加入主畫面」後全螢幕無網址列，外殼可離線開啟。

## 📲 使用方式

1. 下載本倉庫的 [`index.html`](index.html)（點開後另存新檔即可）。
2. 傳到手機（USB / LINE / Email / 雲端皆可），用瀏覽器開啟。
3. 完成——開啟就自動進入你的預設 AI；按返回鍵回到導航頁，點底部膠囊可切換 AI。

> 💡 想像 App 一樣全螢幕無網址列？在瀏覽器選單選「**加入主畫面 / Add to Home Screen**」，桌面就會多一顆圖示。

## 🤖 內建 AI 清單（41 項）

**國內（可框內顯示）**：元寶、豆包、Kimi、文心一言、通义千问、智谱清言、讯飞星火、天工AI、百川智能、腾讯混元、海螺AI、跃问、MiniMax 等 13 項

**國外（部分站點禁止內嵌，會顯示提示卡並提供「在瀏覽器開啟」）**：ChatGPT、Gemini、Claude、DeepSeek、Copilot、Grok、Perplexity、Meta AI、Mistral、Poe、Character.AI、HuggingChat、You.com、Pi、Qwen 等 15 項

> ⚠️ 國外多數 AI 官網（ChatGPT / Gemini / Claude 等）設定 `X-Frame-Options` 禁止被 iframe 內嵌，這是瀏覽器安全機制，非本程式限制。該類站點會顯示提示卡，點「在瀏覽器開啟」即可新分頁開啟。

## 🎨 生圖 AI（13 項，名稱標註「(生圖)」）

這批站點走「**在瀏覽器開啟**」分支（生圖 UI 較複雜，多數禁止 iframe 內嵌，框內易破版；用瀏覽器開啟功能最完整）：

- **國內**：即夢 AI、可靈 AI、文心一格、海藝 AI、美圖 WHEE
- **國外**：Leonardo、Ideogram、Adobe Firefly、Stable Diffusion、Playground、Recraft、Bing 圖像、Craiyon

> 已排除完全付費、無免費額度的 Midjourney，以及無公開網址的妙鴨相機。與現有重複網址的國內站（豆包、通義、訊飛、元寶/混元）不重複加入。

## 🛠 技術規格

- 純 HTML + CSS + JavaScript，**無任何外部依賴**（不連 CDN、無框架）。
- iframe 內嵌 AI 網頁；`prefers-color-scheme` 深色模式；pointer events 拖動排序。
- 桌面分割：Flex 佈局 + 可拖拉分隔條（比例限制 15%–85%），布局與偏好存 localStorage。

## 📄 授權

[MIT License](LICENSE) © 2026 修哥 (hsiu)
