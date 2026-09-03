# 【品牌名稱】官方網站（GitHub Pages 靜態站）

四頁式品牌官網，可直接上傳到 GitHub repository 並開啟 GitHub Pages 公開。

## 頁面

| 路徑 | 說明 |
|------|------|
| `index.html` | 首頁 |
| `products/` | 產品與成分 |
| `about/` | 博士／研發團隊 |
| `contact/` | 聯絡與詢問 |

## 上傳到 GitHub 並公開

1. 在 GitHub 建立一個 **Public** repository（例如 `nutrition-brand-site`）。
2. 解壓本 zip，把**裡面的所有檔案**上傳到 repo 根目錄（不要多包一層資料夾）。
   - 網頁：Add file → Upload files
   - 或本機 `git push`
3. 進入 repo → **Settings** → **Pages**
4. Source 選 **Deploy from a branch**
5. Branch 選 `main`（或預設分支），Folder 選 `/ (root)` → Save
6. 約 1–10 分鐘後網址為：
   - `https://你的帳號.github.io/nutrition-brand-site/`

> 已含空的 `.nojekyll`，避免 Jekyll 干擾純 HTML 站。

## 上傳前請替換

- 所有 `【品牌名稱】`、`【價格】`、`【〇〇〇 博士】` 等佔位文字
- `contact/index.html` 的信箱、電話、公司資料
- 表單 `action="https://formspree.io/f/YOUR_FORM_ID"`（到 [Formspree](https://formspree.io) 申請後替換）
- 把產品圖、博士照放到 `assets/images/`，並把頁面中的虛線佔位框改成 `<img src="../assets/images/xxx.jpg" alt="...">`

## 專案站路徑注意

若網址含 repo 名稱（`/nutrition-brand-site/`），本站已使用**相對路徑**，一般可直接運作，不必再改連結。

## 本機預覽

用瀏覽器直接開啟 `index.html`，或在資料夾執行：

```bash
python3 -m http.server 8080
```

然後開 `http://localhost:8080`
