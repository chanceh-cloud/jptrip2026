# 專案行為與開發準則 (Project Guidelines & Agent Rules)

## 1. 專案背景與目標
- **專案名稱**：2026 日本神戶・岡山・京都 11 日五人家庭旅遊 App
- **目標載具**：一律以 **iOS Standalone Web App (PWA)** 為最高驗收與 UI/UX 基準（適應全螢幕、無瀏覽器網址列、支援雙指捏合縮放與拖曳 Modal）。
- **線上網站**：Cloudflare Pages 部署 URL：`https://jptrip2026-7cn.pages.dev/`
- **GitHub 儲存庫**：`https://github.com/chanceh-cloud/jptrip2026.git`

## 2. 溝通與語言規範
- **語言**：一律使用繁體中文（台灣習慣用語）。
- **簡潔高效**：回答保持簡潔、重點明確、格式美觀（使用 Markdown 與 Emoji 增強可讀性）。

## 3. 專案內容與行程標記規範
- **交通座位分類**：只要涉及搭乘 JR、電車或新幹線，必須明確標示：
  - 【只有指定席】（全車對號座，如南海特急 Rapi:t）
  - 【指定席、自由席】（並標明第幾車廂為自由席，如山陽新幹線 Sakura 1~3車廂自由席、JR 新快速 1~8, 10~12車廂自由席）
  - 【只有自由席】（如地鐵、公車、捷運、普通電車）
- **票券購買資訊**：在每日交通說明與票券攻略頁面中，詳細標明各套票的「線上/實體購票與兌換地點」。
- **飯店預約單 Modal**：點擊預約確認單時，顯示內建圖片 Modal（非全頁轉址），支援手勢捏合縮放 (Pinch-to-zoom) 與拖曳移動 (Pan)。

## 4. 版本控制與發布流程 (Git & Cloudflare)
- **版本號更新**：每次修改 `index.html` 的行程或程式碼後，必須同步遞增右上角的版本號（如 `ver 1.05` -> `ver 1.06`），以便使用者在 iOS 上確認是否有載入最新版。
- **儲存庫同步**：修改完畢後，執行 `git add`、`git commit` 並 `git push` 到 GitHub `main` 分支，自動觸發 Cloudflare Pages 秒級建置與 CDN 部署。
