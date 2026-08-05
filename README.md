# 伊忍 YI-REN COLD BREW TEA — 品牌官網（純淨單欄版）

第四個版本，回應您的三個明確要求重新設計：**圖片不併排、不壓縮、不編號**。純靜態網站（HTML + CSS + JS，無需建置工具），可直接部署到 GitHub Pages。

## 這版做了什麼調整

1. **圖片不併排**：整站沒有任何雙欄／多欄圖片排版。從 Hero、風味介紹、品牌故事到門市，每一張圖都獨佔一整行，上下堆疊，一次只看一張。
2. **圖片不壓縮**：每張圖的 `width`／`height` 屬性都逐一比對過實際檔案尺寸，完全一致；且沒有使用任何會裁切變形的 `object-fit: cover`，圖片一律以原始比例完整顯示。
3. **不編號**：拿掉了上一版「TEA·01」這種產品編號系統，菜單回到最單純的「品名＋價格」呈現。

版面因此變成一條由上到下的單一敘事軸線：文字段落 → 一張圖 → 文字段落 → 一張圖，像一篇長文章，而不是排版緊湊的型錄。

## 檔案結構

```
/
├── index.html
├── css/style.css
├── js/main.js
├── images/          19 張已優化的產品／品牌圖片（WebP，共約 1.9MB）
└── README.md
```

## 部署到 GitHub Pages

1. GitHub 建立新 repository（例如 `yi-ren-tea`）。
2. 把整個資料夾內容 push 上去：
   ```bash
   git init
   git add .
   git commit -m "伊忍 YI-REN 純淨單欄版官網"
   git branch -M main
   git remote add origin https://github.com/你的帳號/yi-ren-tea.git
   git push -u origin main
   ```
3. repo 的 **Settings → Pages** → Source 選 **Deploy from a branch** → Branch 選 `main` / `root` → Save。
4. 約 1–2 分鐘後即可透過 `https://你的帳號.github.io/yi-ren-tea/` 造訪。

## 其他待調整項目

- 企業訂購表單、電子報表單目前皆為 `mailto:` 靜態寫法，建議接 Formspree／Google 表單。
- 門市地址、社群連結目前為佔位內容，請於資訊確定後更新。
- 頁面較長（單頁約可捲動數千像素），這是刻意的敘事節奏；若日後覺得太長，可以考慮把「工藝與包裝」或「風味介紹」拆成獨立子頁面。

## 本機預覽

```bash
python3 -m http.server 8000
# 瀏覽器開啟 http://localhost:8000
```
