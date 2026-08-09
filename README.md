# 30 天 AI 幼幼班 · 資源總站（GitHub Pages 靜態站）

這個資料夾是「領取頁（網站）」——Meta 自動私訊發的那一條連結就指向這裡。
所有 7 個誘餌（Day 7/14/15/21/26/28/30）的領取頁與 PDF 都集中在同一個網域，
未來可綁自訂網域（如 `ai30.tw`）也不會換址。

## 檔案結構

```
ai30-site/
├─ index.html              ← 資源總站首頁（Meta 自動私訊發這條）
├─ day7.html  … day30.html ← 7 個誘餌領取頁（乾淨網址）
├─ 誘餌_Day7_*.pdf …       ← 7 個誘餌 PDF（領取頁的「下載收藏版」連結對到這裡）
└─ .nojekyll               ← 關掉 Jekyll，避免 _ 開頭檔被當特殊檔
```

> 誘餌頁的 PDF 下載連結用的是原始中文檔名，請**保持 PDF 在站體根目錄、不要改名**。

## 上線步驟（GitHub Pages）

1. **建 repo**：GitHub 開一個 repo，名稱 `ai30`
   → 網址會是 `https://emma394941.github.io/ai30/`
   （若用 `emma394941.github.io` 這個 repo，就把本站放進 `/ai30/` 子資料夾）
2. **上傳**：把本資料夾全部內容 push 到 repo 根（含 `.nojekyll`）
3. **開 Pages**：repo `Settings → Pages → Source` 選 `Deploy from a branch` → `main` / `root` → Save
4. **等 1 分鐘**，開 `https://ai30class.github.io/ai30/` 看結果

## 上線前必填（佔位符）

搜尋並替換以下兩個字串（共 8 個檔：index.html + 7 個 dayXX.html）：

- `你的IG帳號` → 你的 IG username（@ 後那串）
- `https://lin.ee/你的LINE社群連結` → 你的 LINE 官方帳號加好友連結（lin.ee/...）

填了才真的能導流。Meta 自動私訊只用「AI」一個關鍵字，全部導向這個總站。

## 與誘餌來源檔的關係

`dayXX.html` 與 `誘餌_DayXX_*.pdf` 是 `gen_baits.py` 的產出（workspace 根目錄）。
若日後改了誘餌內容：重跑 `python gen_baits.py`，再把新產出的 HTML/PDF 複製進本資料夾即可。
