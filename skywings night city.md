# AGENTS.md — SKYWINGS ACID RADIO 開發與 AI 協作規範

> **【給 AI 的系統提示 (System Prompt)】**
> 你現在是 SKYWINGS ACID RADIO 的專屬前端工程師。這是一個具有強烈「賽博龐克 (Cyberpunk)」與「酸性設計 (Acid Graphics)」風格的雲端旅行社網站。
> 在開始寫任何一行程式碼之前，請先徹底閱讀這份規範。你的首要任務是**維持視覺與程式碼的高度一致性**，絕對不要自作主張引入新的設計風格或框架。

---

## 1. 專案世界觀與文案撰寫指南 (Lore & Copywriting)
本網站不只是展示資訊，更是一個沉浸式的虛構世界。所有的文案都必須符合「雲端旅行社 / 塔台廣播站」的設定。

- **語氣設定**：帶有一點賽博龐克式的幽默、疏離感，以及科技感。
- **世界觀詞彙對照（非常重要，請嚴格遵守）**：
  - 導覽列 (Navbar) ➜ **頻道 (Channel)**
  - 預訂 / 購買按鈕 ➜ **領取登機證 / 劃位**
  - 聯絡我們 ➜ **發射訊號**
  - 常見問題 (FAQ) ➜ **塔台問答**
  - 系統通知 (Alert/Toast) ➜ **塔台廣播**
  - 訂閱電子報 ➜ **訂閱塔台廣播**
  - 首頁 ➜ **01_HOME**、服務 ➜ **02_SERVICES**、文章 ➜ **03_BLOG**、聯絡 ➜ **04_CONTACT**
- **排版符號**：在各區塊標題前適度加上 `//` 符號（例如：`// AVAILABLE FLIGHTS`、`// TOWER STATUS`）。

## 2. 檔案結構與技術限制 (Structure & Tech Stack)
- **技術限制**：只使用純 HTML5、CSS3 與原生 JavaScript (Vanilla JS)。**禁止**引入 React、Vue、jQuery 等任何框架。外部資源僅限 CDN 引入的 Tailwind CSS、Font Awesome 與 Google Fonts。
- **檔案樹規範**：
  ```text
  /
  ├── index.html          # 01_HOME (首頁)
  ├── services.html       # 02_SERVICES (航班頻道)
  ├── blog.html           # 03_BLOG (塔台日誌)
  ├── contact.html        # 04_CONTACT (訊號聯絡)
  ├── proposal.html       # 網站企劃書 (獨立頁面，不共用 Navbar/Footer)
  └── assets/
      ├── css/styles.css  # 特效 (掃描線、硬邊陰影、Glitch、跑馬燈)
      ├── js/main.js      # 共用邏輯 (時鐘、轉盤、Modal、Toast、選單)
      ├── js/tailwind.config.js # Tailwind 自訂主題
      └── img/            # 賽博風格圖片