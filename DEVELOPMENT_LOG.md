# Menubar Calendar Landing Page 開發紀錄

## 專案概述
Menubar Calendar macOS 應用程式的官方網站 Landing Page，用於 GitHub Pages 部署，提供產品介紹、功能展示、定價方案及隱私權政策。

- **網站 URL**: `https://lafcadio5th.github.io/Menubar-Calendar-Web/`
- **聯絡信箱**: `kstudio.apps.tw@gmail.com`

---

## 已完成功能

### 網站架構
- [x] 響應式單頁 Landing Page (`index.html`)
- [x] 隱私權政策頁面 (`privacy.html`)
- [x] 支援中心頁面 (`support.html`)
- [x] 多語系支援 (繁體中文/English 切換)
- [x] 深色/淺色主題切換

### SEO 優化
- [x] Open Graph meta tags（社群分享預覽）
- [x] Twitter Card meta tags
- [x] 結構化資料（JSON-LD Schema.org）
- [x] `sitemap.xml` 網站地圖
- [x] `robots.txt` 搜尋引擎爬蟲指引
- [x] Canonical URL 設定

### OG Image（社群分享圖片）
- [x] `images/og-image.png` - 1200x630 標準尺寸
- [x] 灰白漸層背景 + 紅色點綴
- [x] 包含 App icon、標題、功能特色、截圖
- [x] 使用 Python PIL 生成（`generate_og.py`）

### 視覺設計
- [x] 漸層動態背景 (多層 radial-gradient 動畫)
- [x] Apple 風格 UI 設計語言
- [x] 毛玻璃效果 (backdrop-filter blur)
- [x] 響應式佈局 (Desktop/Tablet/Mobile)

### Hero Section
- [x] 主標題 + 副標題
- [x] CTA 按鈕 (Mac App Store / GitHub)
- [x] 主截圖展示

### Mode Showcase Section
- [x] 雙欄卡片展示 (Popover Mode / Desktop Mode)
- [x] 功能特點列表
- [x] 截圖預覽

### Features Section
- [x] Featured Hero Card - 會議一鍵加入功能
  - [x] 淡綠色漸層背景卡片
  - [x] 雙欄佈局 (左文字/右截圖)
  - [x] 「最受歡迎功能」徽章
  - [x] 裁切後的 App 截圖展示
- [x] 6 個功能卡片 Grid
  - [x] Scroll 觸發入場動畫 (Intersection Observer)
  - [x] Icon Hover 雙狀態切換效果
  - [x] 用戶利益導向文案

### Smart Features Section
- [x] 會議連結一鍵加入（Zoom/Meet/Teams/Webex）
- [x] 導航整合（Apple Maps/Google Maps 路線預覽）

### Theme Showcase Section
- [x] 淺色/深色主題互動切換展示
- [x] 即時預覽圖片切換

### Premium Section
- [x] 豪華深色漸層背景
- [x] 雙定價卡片 (月訂閱 $0.99/年訂閱 $7.99)
- [x] 玻璃擬態卡片設計
- [x] 「最划算」金色光暈動畫效果
- [x] 功能對比列表
- [x] 信任徽章 (Apple 安全審核/無廣告/本地處理)

### FAQ Section
- [x] 11 題常見問題
- [x] 手風琴展開/收合效果
- [x] 完整中英文翻譯

### Footer
- [x] 台灣國旗 🇹🇼 標示
- [x] 社群連結 (GitHub/Email)
- [x] 頁面內導航連結
- [x] 版權聲明

### 多語系 (i18n)
- [x] data-i18n 屬性系統
- [x] JavaScript 翻譯物件
- [x] 語言切換器 UI
- [x] 完整中英文翻譯

---

## 待開發功能

### 高優先
- [ ] **GitHub 連結** - 目前是 placeholder (`https://github.com/user/mac-calendar`)，需更新為實際 repo
- [ ] **App Store 連結** - 上架後需更新實際連結

### 中優先
- [ ] **天氣動畫展示** - 考慮用 App 實際截圖替代（CSS 動畫效果不佳已移除）
- [ ] **更多截圖素材** - 可增加更多功能展示圖

### 低優先
- [ ] 效能優化 - 圖片壓縮、lazy loading
- [ ] Analytics - 加入 Google Analytics 或其他追蹤工具
- [ ] 客戶見證/評價區塊
- [ ] 更新日誌頁面

---

## 技術架構

### 前端技術
- 純 HTML5 + CSS3 + Vanilla JavaScript
- 無框架依賴，輕量化設計
- CSS Variables 主題系統
- CSS Grid + Flexbox 佈局

### 動畫效果
- CSS @keyframes 動畫
- Intersection Observer API (scroll 觸發)
- CSS transitions (hover 效果)

### 部署
- 目標平台：GitHub Pages
- 靜態網站，無需後端

---

## 檔案結構

```
Mac Calendar Github Web/
├── index.html          # 主頁面
├── privacy.html        # 隱私權政策
├── support.html        # 支援中心
├── sitemap.xml         # 網站地圖
├── robots.txt          # 爬蟲指引
├── development_log.md  # 開發紀錄（本文件）
└── images/
    ├── Icon.png
    ├── og-image.png
    ├── 01-main-light.png
    ├── 01-main-dark.png
    ├── 02-widget-light.png
    └── 02-widget-dark.png
```

---

## 更新紀錄

### 2026-01-16（下午）
- 新增 SEO 優化（Open Graph、Twitter Card、JSON-LD、sitemap.xml、robots.txt）
- 新增 OG Image 生成腳本與圖片
- 新增支援中心頁面 (`support.html`)
- 新增 FAQ Section（11 題常見問題）
- 新增 Smart Features Section（會議連結 + 導航整合）
- 圖片檔名標準化（空格改為連字號）
- 更新聯絡信箱為 `kstudio.apps.tw@gmail.com`
- 移除天氣動畫區塊（效果不佳，改用截圖展示）

### 2026-01-16（上午）
- 建立初始網站架構
- 完成 Hero/Mode/Features/Premium/Footer 各區塊
- 實作多語系切換功能
- 實作深淺色主題切換
- 品牌更名：Mac Calendar → Menubar Calendar
- 新增台灣國旗標示
- 升級 Premium 區塊為豪華設計
- 重新設計 Featured Card (會議一鍵加入)
- 優化截圖裁切與背景處理
