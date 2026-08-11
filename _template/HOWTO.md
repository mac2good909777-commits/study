# 怎麼做一份新的 Study 檔案

## 步驟

1. `cp -r _template 0NN-topic-slug`（slug 用純 ASCII 小寫連字號）
2. 從 `001-urban-agricultural-zone/index.html` 複製一份當 HTML 骨架 —— 樣式已定義好，直接改內容即可
3. 寫 `README.md`（GitHub 直讀版）＋ `index.html`（互動版）
4. 在根目錄 `README.md` 與 `index.html` 各加一列索引
5. commit & push

## 版面規範（已固定，不要改）

- 品牌：**中性通用**（無 Logo、無品牌色）
- 風格：**極簡灰階** — 頁面底 `#FAFAFA`、卡片 `#FFFFFF`、標題 `#374151`、內文 `#6B7280`
- 強調色：琥珀棕 `#B45309`（僅用於法條符號、口訣 code、連結）
- 功能色：綠 `#059669`（可／優）、紅 `#DC2626`（不可／劣）
- 圓角 12px、陰影 `0 1px 3px rgba(0,0,0,.04)`、內文 line-height 1.8
- 支援 `prefers-color-scheme: dark`
- 字體：Inter + Noto Sans TC + JetBrains Mono（法條編號與數字用等寬）

## 內容規範

- **法條一律逐字擷取**，放在 `<details class="law">` 可展開區塊，並附全國法規資料庫連結
- 條號用正式寫法：`§17Ⅰ⑥`（條、項、款）
- 每個數字、稅率、門檻都要指得出來源
- 優缺點必須分欄並列，不藏缺點
- 結尾一定要有免責聲明

## 可重用的 HTML 元件

| class | 用途 |
|---|---|
| `.card` | 每個章節一張卡 |
| `details.law` + `.quote` | 法條原文展開區 |
| `.call` / `.call.key` / `.call.danger` | 一般提示／關鍵推論／風險警告 |
| `.map .step` | 步驟式學習地圖 |
| `.mn .row` | 記憶口訣（左口訣、右說明） |
| `.q` + JS toggle | 自我測驗題（點擊翻答案） |
| `.g2` + `.box.good` / `.box.bad` | 優缺點雙欄 |
| `.kpis .kpi` | 數字重點卡 |
| `.tw > table` | 可橫向捲動的表格（行動裝置必要） |
