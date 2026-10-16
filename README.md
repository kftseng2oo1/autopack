# PWA 打包神器（autopack）

把一個單檔 HTML 變成可安裝的 PWA：自動產生 manifest、Service Worker、圖示、離線頁、README，並可一鍵上傳到 GitHub。

**線上使用**：https://kftseng2oo1.github.io/autopack/

## 主要功能
- 上傳 HTML，填入 App 名稱、顏色、scope（例如 `/my-repo/`）
- 自動產生：`index.html`（注入 manifest 與 SW 註冊）、`manifest.json`、`sw.js`、`offline.html`、PNG／SVG 圖示、`README.md`
- **打包驗證**：比對 script 數量、`</body>` 是否完整、檔案大小是否異常、SW 是否重複，避免打包後內容遺失
- 🪟 沙箱預覽，原始檔與打包後對比
- 🐙 用 GitHub Token 直接把所有檔案上傳到指定 repo；也可全部下載
- 針對 iOS 下載限制有專用的部署頁面

## 技術與依賴
- 單檔 HTML PWA（`index.html` 內含全部 HTML/CSS/JS），`manifest.json` + `sw.js` 提供安裝到主畫面與離線快取。
- GitHub REST API（`api.github.com/repos/…/contents`），Token 可選擇記住在本機

## 備註
- 其他 repo 裡的樣板式 README（「一個 Progressive Web App ＋ 檔案清單」）就是這個工具產生的。
