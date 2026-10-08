# 本日作業：3D 鐳射卡牌網頁生成流程 Prompt
> **從訪談到一鍵發布的全流程 Prompt 範本**

本 Prompt 專門設計用來引導大型語言模型（LLM）或 AI 代理人，完整實作兼具 **訪談引導、3D 視差雷射光學渲染、單檔案零依賴、以及 GitHub Pages 免建置部署** 的現代化 TCG 鐳射卡牌生成器。

---

## 📋 完整 Prompt 提示詞（可直接複製繳交或使用）

```markdown
# Role & Mission
你是一位兼具 3D 視覺渲染工程、WebGL/CSS 著色器 (Shaders)、TCG 集換式卡牌美學與資深前端全端架構能力的頂尖工程師。
你的任務是建立一個具備「3D 視差與雷射全息光澤系統」的「卡牌互動鑄造生成器網頁應用」，並嚴格遵循以下三階段規範實作：

---

### 【階段一：引導】啟動卡牌鑄造訪談 (Interview & Specification)
在使用者進入系統時，提供結構化的訪談或步驟嚮導，收集並配置以下要素：
1. 核心屬性與數值：
   - 設定角色名稱、生命能階 HP (如 340)、階級標記 (如 ★ 傳奇 ★)、屬性/主題色系（創發紅、科技金、深海藍、翡翠綠、虛空紫、黑金暗影等）。
2. 視覺立繪與箔膜：
   - 支援本地圖片上傳/拖曳（Drag & Drop）或選擇預設立繪。
   - 動態雷射箔膜材質挑選：宇宙彩虹 (Cosmic Rainbow)、極光全息 (Aurora Holographic)、黑金浮雕 (Black Gold Foil)、星芒碎鑽 (Glitter Sparkle)、賽博霓虹 (Cyber Neon)。
3. 技能與戰鬥機制：
   - 被動特性 (Passive Ability)：特性名稱與戰場效果說明。
   - 普通招式 (Basic Attack)：招式名稱、威力數值與能量消耗。
   - 奧義技能 (Ultimate Move / GX Burst)：金色醒目框、奧義名稱、超高傷害威力 (如 360+) 與毀滅特效敘述。
4. 對抗與印記設定：
   - 弱點 (Weakness)、抗性 (Resistance)、撤退費用 (Retreat Cost)。
   - 創作者署名 (Creator Signature) 與稀有度認證編號 (如 099/100 ★★★ UR)，附帶金屬全息防偽印記。

---

### 【階段二：生成】系統實作與技術規範 (Implementation Standards)
1. 流體響應式佈局 (Fluid Responsive Layout)：
   - 桌面端採優雅雙欄架構：左側為 3D 卡牌視差舞台與互動控制鈕列，右側為即時編輯與訪談面板。
   - 行動端自動轉換為垂直堆疊 (Vertical Stack)。
   - 卡牌嚴格遵循 TCG 黃金比例 (63mm × 88mm，約 1:1.4)。
2. 3D 視差與雷射系統 (3D Parallax & Holographic Engine)：
   - 支援滑鼠動態懸停、觸控滑動及行動裝置陀螺儀 (DeviceOrientation)。
   - 動態計算傾斜角 (rotateX, rotateY, perspective 1200px)。
   - 多層次光學折射：
     * 高光眩光層 (Dynamic Glare)：跟隨指標座標的 radial-gradient color-dodge 高光斑。
     * 雷射箔膜層 (Holographic Foil)：根據傾角即時變化的彩虹折射 (repeating-linear / conic gradients)。
     * 微粒晶鑽噪點層 (Sparkle Mesh)：細緻金屬反光質感。
3. 零依賴單一檔案 (Zero-Dependency Single File)：
   - 產出獨立自洽的 `index.html`，內建原生 HTML5、CSS3 與 Vanilla JavaScript。
   - 整合 Web Audio API 原生音效合成器（翻牌、全息閃光、按鈕點擊，免額外音檔）。
   - 免任何 npm install 或建置步驟，開箱即用。
4. 即時編輯與互動機制 (Real-time Live Editing & Interactivity)：
   - 雙向即時綁定：面板數值修改即刻同步反映於卡面。
   - 支援 180 度翻牌 (3D 翻轉展示精緻奧術/賽博卡背)。
   - 提供「自動巡航 3D 展示」模式與視角重設功能。

---

### 【階段三：發布】成果輸出與部署 (Export & GitHub Pages Deployment)
1. 一鍵高畫質匯出：
   - 整合 html2canvas CDN，提供「一鍵匯出高解析 PNG (正面/背面)」功能，以 3x 超取樣匯出透明背景卡牌圖檔。
2. GitHub Pages 零障礙發布 (Zero-Build Deployment)：
   - 專案純靜態，推送至 GitHub 後，至 Settings ➔ Pages 開啟即可 30 秒自動上線全球。
   - 內建一鍵部署指引彈窗，提供清晰步驟。
3. 專屬傳奇展示：
   - 提供頂級收藏家級別之暗黑玻璃態 (Dark Glassmorphism) 舞台，適合錄製展示短影音或作為個人卡牌專頁。

請輸出完整且可立即執行的單一 HTML 檔案，並確保所有樣式、光澤著色器與邏輯皆完整運作無任何報錯。
```

---

## 🎯 流程重點對照表

| 階段 | 核心內容 | 實作成果 |
| :--- | :--- | :--- |
| **階段一：引導** | 核心數值、立繪箔膜、技能奧義、弱點印記 | 內建「4 步驟訪談精靈」與「即時自訂面板」 |
| **階段二：生成** | 桌面雙欄/行動堆疊、3D 視差、彩虹雷射、零依賴單檔 | 純原生 CSS 3D 變換、多層 Blend-mode 箔膜著色器、Web Audio 合成音效 |
| **階段三：發布** | html2canvas 匯出、GitHub Pages 免建置、傳奇展示 | 3x 高畫質 PNG 正反面匯出、零建置部署引導 |
