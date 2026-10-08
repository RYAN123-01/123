# 🌟 3D 鐳射全息卡牌生成器 (3D Holographic Card Studio)

> **本日作業成果：從訪談引導到一鍵發布之 3D 鐳射卡牌生成器完整實作**

本專案完全依據作業規格，以 **單一檔案 (Zero-build Single File `index.html`)** 實作，整合 **3D 視差傾角、多層次全息雷射光學反射、自訂立繪上傳、180度翻轉、訪談鑄造精靈與一鍵超高解析 PNG 匯出**。

---

## 📸 功能亮點 (Highlights)

### 1. 階段一：啟動卡牌鑄造訪談 (引導系統)
- **核心屬性與數值**：角色名稱、HP 能階（340）、階級標籤（★ 傳奇 ★）、6 種主題元素色系切換（科技金、創發紅、深海藍、翡翠綠、虛空紫、黑金暗影）。
- **視覺立繪與動態箔膜**：支援點擊/拖曳上傳自訂圖片，並內建 4 款傳奇向量立繪與 5 種 3D 動態箔膜（宇宙彩虹、極光全息、黑金浮雕、星芒碎鑽、賽博霓虹）。
- **技能與戰鬥機制**：特性 (Passive Ability)、普通招式傷害與能量、以及黃金框奧義大招 (BURST GX) 傷害與毀滅特效說明。
- **對抗與印記設定**：弱點倍率、抗性數值、撤退費用、創作者簽名、認證防偽編號與 3D 金屬反光防偽微印。

### 2. 階段二：系統實作與規範 (生成核心)
- **流體響應式佈局**：桌面端雙欄（左側 3D 展示舞台，右側雙模式自訂中心）；行動端自動轉換垂直堆疊；精確維持 TCG 63mm × 88mm (1:1.4) 黃金比例。
- **3D 視差與雷射光學系統**：
  - 游標動態傾角追蹤 (`rotateX`, `rotateY`, `perspective 1200px`)。
  - 行動裝置陀螺儀 (`DeviceOrientation`) 傾角支援。
  - 多層次光澤疊加：高光眩光 (Dynamic Glare)、彩虹全息折射 (Prismatic Foil)、晶鑽微粒網格 (Sparkle Mesh)。
- **零依賴單一檔案**：純 HTML5 + CSS3 + 原生 JavaScript，無需 Node.js、Vite 或安裝任何套件。
- **Web Audio API 合成音效**：內建合成翻牌風聲、全息金屬閃光晶瑩鈴聲與按鈕點擊反饋（可隨時一鍵靜音）。
- **即時編輯與 180 度翻牌**：雙向無延遲即時同步、一鍵翻牌展示精美奧術星軌卡背。

### 3. 階段三：發布與成果輸出 (發布系統)
- **一鍵高畫質匯出**：整合 html2canvas，提供 3x 超取樣匯出（正面/背面卡牌皆可一鍵下載為高解析透明底 PNG）。
- **GitHub Pages 零障礙**：Zero-build 純靜態檔案，直接推送至 GitHub 即可 30 秒自動上線。
- **內建作業 Prompt 一鍵複製**：頁面頂部按鈕點擊即可預覽與一鍵複製完整 Prompt 提示詞。

---

## 🚀 快速開始 (Quick Start)

### 本地直接開啟
本專案為零依賴單一網頁，直接使用任何現代瀏覽器（Chrome、Edge、Safari、Firefox）開啟 `index.html` 即可使用！

雙擊開啟：
```
c:\Users\User\Desktop\22\index.html
```

---

## 🌐 30 秒部署到 GitHub Pages

1. 在 GitHub 上建立一個新的 Public 儲存庫（例如 `3d-holo-card`）。
2. 將此目錄下的 `index.html`、`PROMPT.md`、`README.md` 上傳至儲存庫。
3. 進入儲存庫頁面 ➔ **Settings** ➔ **Pages**。
4. 在 **Build and deployment** 下，將 Source 選擇 **Deploy from a branch**，Branch 選擇 `main` / `/(root)`，點擊 **Save**。
5. 稍等約 1 分鐘，即可在全球以專屬網址瀏覽您的 3D 鐳射卡牌網頁！

---

## 📂 檔案清單

- [`index.html`](file:///c:/Users/User/Desktop/22/index.html) - 3D 鐳射卡牌生成器完整單一檔案應用程式
- [`PROMPT.md`](file:///c:/Users/User/Desktop/22/PROMPT.md) - 本日作業要求之完整 Prompt 提示詞模板
- [`README.md`](file:///c:/Users/User/Desktop/22/README.md) - 專案說明與 GitHub Pages 部署指南
