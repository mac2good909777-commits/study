# 怎麼做一份新的 Study 檔案

## 步驟

1. `cp -r _template 0NN-topic-slug`（slug 用純 ASCII 小寫連字號）
2. 從 `003-rent-vs-buy/index.html` 複製一份當 HTML 骨架
3. 寫 `README.md`（GitHub 直讀版）＋ `index.html`（互動版）
4. 在根目錄 `README.md` 與 `index.html` 各加一列索引
5. commit & push

## 樣式：改 CSS 請改 `assets/study.css`（不要寫內嵌 `<style>`）

全站共用一份樣式。每個頁面 `<head>` 只需要這一行：

```html
<link rel="stylesheet" href="../assets/study.css">
```

根目錄 `index.html` 用 `href="assets/study.css"`。
**改一次，全部檔案同步生效**——不要在個別頁面加內嵌 `<style>`。

## 版面規範（已固定，不要改）

- 品牌：**中性通用**（無 Logo、無品牌色）
- 風格：**極簡灰階** — 頁面底 `#FAFAFA`、卡片 `#FFFFFF`、標題 `#374151`、內文 `#4B5563`
- 強調色：琥珀棕 `#B45309`（僅用於法條符號、口訣 code、連結）
- 功能色：綠 `#047857`（可／優）、紅 `#B91C1C`（不可／劣）
- 圓角 12px、陰影 `0 1px 3px rgba(0,0,0,.04)`
- 支援 `prefers-color-scheme: dark`
- 字體：Inter + Noto Sans TC + JetBrains Mono（法條編號與數字用等寬）

## 可讀性規範（2026-08 修訂）

主要閱讀裝置是**手機（Pixel Fold 外螢幕約 360px 寬）**，樣式為 mobile-first：

- **任何文字不小於 14px**。內文 16px、表格 15px、標題 20~24px。
- 行高：內文 1.8、表格 1.65、標題 1.4~1.5。
- 斷點：`480px`（大手機）→ `700px`（Fold 展開／平板）→ `900px`（桌機）。
  雙欄（`.g2`）、雙欄目錄、`.mn` 左右排版都在 **700px 以上**才啟用，窄螢幕一律單欄堆疊。
- 表格一律包在 `<div class="tw">` 裡：窄螢幕會**滿版出血**取得最大寬度，
  並自動顯示左右捲動陰影提示。`min-width` 窄螢幕 420px、≥700px 才放寬到 520px。
- 可點擊元素（`.btn`）最小觸控高度 44px。
- 已內建列印樣式：測驗答案與法條原文在列印時自動全部展開。

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
| `details.law` + `.quote` + `.src` | 法條原文展開區 |
| `.call` / `.call.key` / `.call.danger` | 一般提示／關鍵推論／風險警告 |
| `.map .step`（`.i` + `.t`） | 步驟式學習地圖 |
| `.mn .row`（`.k` + `.d`） | 記憶口訣（窄螢幕上下堆疊、寬螢幕左右） |
| `.q` + `.qq` + `.aa` + JS toggle | 自我測驗題（點擊翻答案） |
| `.qbar` + `.btn` | 全部展開／收合按鈕 |
| `.g2` + `.box.good` / `.box.bad` | 優缺點雙欄（≥700px 才並排） |
| `.kpis .kpi`（`.v` + `.l`） | 數字重點卡 |
| `.tw > table` | 可橫向捲動的表格（**所有表格都必須包**） |
| `.num` | 等寬數字（表格內數值建議加上） |
| `.yes` / `.no` / `.warn` | 綠／紅／琥珀的判定文字 |

自我測驗需要在頁尾加上這段 JS：

```html
<script>
document.querySelectorAll('.q .qq').forEach(function(el){
  el.addEventListener('click',function(){ el.parentElement.classList.toggle('open'); });
});
</script>
```
