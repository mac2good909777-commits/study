# Study — 單一主題學習檔案庫

> 一個檔案一個主題。每篇都附**法條原文擷取**、決策對照表、記憶口訣與自我測驗。
> 設計目的是**讀一次能記住、需要時能查到**，而不是讀完就忘的長文。

🔗 **線上閱讀：https://mac2good909777-commits.github.io/study/**

---

## 檔案索引

| 主題 | 分類 | 建立 | 連結 |
|---|---|---|---|
| 高齡租住服務：日本對標與台灣切入評估<br><sub>金融環不巨大、資產環才巨大 · 六環節獲利拆解 · 四段切入排序</sub> | 產業機會 | 2026-08-14 | [📖 互動版](https://mac2good909777-commits.github.io/study/senior-rental-market/) ／ [📄 Markdown](senior-rental-market/README.md) |
| 案例：一間北屯自宅的持有／出售決策全紀錄<br><sub>只還息 13 年 · 93% 集中度 · 三方案 20 年對照 · 感性帳定價</sub> | 案例研究 | 2026-08-14 | [📖 互動版](https://mac2good909777-commits.github.io/study/beitun-case/) ／ [📄 Markdown](beitun-case/README.md) |
| 租屋 vs 買房：台灣參數下的總持有成本與機會成本<br><sub>TCO × 機會成本正確算法 × 只還息陷阱 × 公設比坪效 × 日本 20 年實績</sub> | 個人財務／不動產 | 2026-08-14 | [📖 互動版](https://mac2good909777-commits.github.io/study/rent-vs-buy/) ／ [📄 Markdown](rent-vs-buy/README.md) |
| 一人有限公司稅務實務：發票、擴大書審、資金合法動用<br><sub>速查表在最前面 · 進項扣抵 vs 列費用 · 1,000 萬門檻</sub> | 公司稅務 | 2026-08-12 | [📖 互動版](https://mac2good909777-commits.github.io/study/corporate-tax-basics/) ／ [📄 Markdown](corporate-tax-basics/README.md) |
| 都市土地農業區，作為長期資產的優勢與陷阱<br><sub>自然人 vs 法人 × 短期 vs 長期</sub> | 不動產稅務 | 2026-08-11 | [📖 互動版](https://mac2good909777-commits.github.io/study/urban-agricultural-zone/) ／ [📄 Markdown](urban-agricultural-zone/README.md) |

---

## 每篇檔案的固定結構

為了讓吸收有節奏，所有主題都照同一套骨架寫：

1. **30 秒總結** — 五句話帶走全部
2. **學習地圖** — 核心觀念之間的因果鏈
3. **核心觀念 N 節** — 每節：一句話結論 → 為什麼 → **法條原文（可展開）**
4. **對照表／四宮格** — 把文字壓成可掃描的表
5. **優缺點分欄** — 正反並列，不藏缺點
6. **地雷清單** — 實務上會出事的地方
7. **記憶口訣** — 四句話對應四條法條
8. **自我測驗** — 點擊翻答案，先想再看
9. **法條原文總表** — 全部引用條文＋官方連結

---

## 新增一個主題

```bash
cd C:\Claude\projects\study
cp -r _template your-topic-slug
# 編輯 your-topic-slug/index.html 與 README.md
# 在本檔與 index.html 各加一列索引
git add . && git commit -m "study: your topic" && git push
```

命名規則：`英文短名`（純 ASCII、不加編號，避免中文資料夾名在 GitHub Pages 上的編碼問題）。
**不加編號的原因**：每一頁都要能單獨分享，網址若帶 `004-` 會讓收到連結的人覺得還有別的檔案。

---

## 原則

- **法條一律附原文**，不只給結論。條文會修，結論會過期，原文＋連結才查得回去。
- **不藏缺點**。優缺點分欄並列，任何「這個很棒」旁邊必須有「但是」。
- **可驗證優先於好看**。每個數字、稅率、門檻都要指得出來源。
- **不是法律意見**。個案執行前請由會計師／地政士／律師出具書面意見。

---

<sub>Mac Chang（張現傑）· 工業地產 · 瑞禾開發／睦聚開發</sub>
