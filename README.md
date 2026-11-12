# 泰文子音圖卡 · บัตรภาพพยัญชนะไทย

看圖和名稱詞（ก ไก่、ข ไข่……）練習泰文 44 個子音的網頁。

網站：https://calvinctchenmay.github.io/thai-consonants/

## 訪客可以做的事

- **練習**：看圖寫子音，有手寫板、看答案、自動播放和泰文發音。
- **全部圖卡**：44 張一起看，點一下翻開答案。
- **考試**：從 4 個長得像的字母裡選答案，考完會打分數，也可以只重考答錯的題。
- **介面語言**：可以切換中文或泰文，也能用網址指定，例如 `?lang=th`。

## 修改內容（需要登入）

打開 `admin.html`（網站右下角的「內容管理」），用 GitHub 金鑰登入後，可以修改每個字母的圖片、表情符號和中文意思。按「發布到網站」後，大約 1 到 2 分鐘網站就會更新。

第一次使用要先產生金鑰：

1. 打開 https://github.com/settings/personal-access-tokens/new
2. Repository access 選「Only select repositories」，再選 `thai-consonants`。
3. Permissions 裡把 Contents 改成「Read and write」。
4. 按 Generate token，把金鑰貼到管理頁登入。

金鑰只存在你自己的瀏覽器裡。沒有金鑰的人看得到管理頁，但改不了任何內容。

## 檔案

| 檔案 | 用途 |
|---|---|
| `index.html` | 訪客的練習和考試頁 |
| `admin.html` | 內容管理頁 |
| `content.json` | 44 個字母的名稱詞、中文、表情符號和圖片路徑 |
| `images/` | 管理頁上傳的圖片 |
| `style.css` | 兩頁共用的樣式 |

## 瀏覽統計（Google Analytics）

1. 到 https://analytics.google.com 建立「資源」，再新增「網站」資料串流，網址填 `https://calvinctchenmay.github.io/thai-consonants/`。
2. 複製「評估 ID」（格式像 `G-ABC123XYZ`）。
3. 在 GitHub 打開 `config.js`，按鉛筆圖示編輯，把 ID 填進 `gaId: ""` 的引號裡，按 Commit changes。

填好後約 1 到 2 分鐘生效。除了瀏覽次數，也會記錄這些事件：`mode_change`（切換模式）、`exam_finish`（考完試，含分數）、`print_sheet`（列印）、`language_change`（切換語言）、`autoplay_start`（開始自動播放）。管理頁不會載入統計程式。
