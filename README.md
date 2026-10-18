# 不等式旋鬥場

兩名學生共用一部橫向 iPad，以複合一元一次不等式為陀螺補血、取得護盾及儲存必殺技能量的 Three.js 3D 教育遊戲。

**遊玩網址見本儲存庫右側 About 的網站連結。**

## 玩法

1. 以橫向開啟，兩人各按「準備發射」，同時開始對戰。
2. 每段戰鬥 10 秒。兩人回答同一道題，但選項次序獨立打亂。
3. 選好後按「鎖定答案」；雙方均鎖定或時間到才揭曉。
4. 答對補血、恢復旋轉、取得護盾及能量。累積答對三題，可於戰鬥發動必殺技。
5. 最後一題後仍有一段戰鬥，賽後可逐題重溫及重練。

| 玩家 | 四個選項 | 鎖定答案 | 必殺技 |
| --- | --- | --- | --- |
| P1 左方 | Q W E R | F | G |
| P2 右方 | U I O P | J | K |

教師可在開局前調整難度、4／6／8 題、10／15／20 秒、音量及特效。預設 6 題、7 段戰鬥。遊戲需要 WebGL 2；iPad 建議使用 Safari。

## 原始碼與本機遊玩

- [下載完整 TypeScript 原始碼及驗收紀錄](source.zip)
- `index.html` 已內嵌遊戲、Three.js、公式字體及合成音效；下載後可在桌面瀏覽器直接開啟。
- 解壓 `source.zip` 後，可修改 `src/questions.json` 題庫及 `src/settings.ts` 數值。

```sh
npm ci
npm run build:pages
npm run check
npm test
```

`npm run build:pages` 更新編譯成品及根目錄的單檔 `index.html`。本儲存庫採 main 分支根目錄發佈，更新時請上載重新編譯後的 index.html。

原始碼包另附可選的 GitHub Actions 發佈設定；若改用該設定，須先把原始碼解壓到儲存庫，並把 Settings → Pages 的 Source 改為 GitHub Actions。

已執行的原版 60 項自動測試通過；實際 iPad 多點觸控、畫面及效能仍待驗證。遊戲不需要學生登入，答題紀錄只留在本場記憶體；教師設定保留於裝置。

Third-party licenses 見 THIRD_PARTY_LICENSES.txt。詳細操作、開發說明及逐項驗收紀錄在 source.zip 的 docs 資料夾。
