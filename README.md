# 北十勝揚・新人培訓紀錄表

互動式新人培訓追蹤網頁。透過 GitHub Pages 發布後，夥伴們只要打開同一個網址，
就能各自建立自己名下新人的培訓紀錄、逐項打卡課程/操作/證照，並匯出 JSON 報表回傳。

---

## 一、如何用 GitHub 發布成公開網頁（免寫程式）

1. 到 [github.com](https://github.com) 登入你的帳號（沒有帳號的話先免費註冊）。
2. 右上角點 **+** → **New repository**。
   - Repository name 填一個名稱，例如 `training-tracker`
   - 選擇 **Public**（公開，這樣夥伴才能用網址打開）
   - 不用勾選任何初始化選項，直接點 **Create repository**
3. 進入剛建好的空 repository，點 **uploading an existing file**（或 "Add file" → "Upload files"）。
4. 把這個資料夾裡的 `index.html` 拖進去上傳，下方填寫 commit message（例如「發布新人培訓紀錄表」），點 **Commit changes**。
5. 上傳完成後，點上方 **Settings** 分頁 → 左側選單找到 **Pages**。
6. 在 **Build and deployment** → **Source** 選 **Deploy from a branch**；
   **Branch** 選 `main`，資料夾選 `/ (root)`，點 **Save**。
7. 等 1～2 分鐘，重新整理這個 Pages 設定頁，畫面上方會出現你的網址，格式像：
   `https://你的帳號.github.io/training-tracker/`
8. 把這個網址分享給夥伴們，大家打開瀏覽器輸入網址就能使用，不需要安裝任何東西。

之後如果我幫你調整了內容（例如修改課程大綱、新增功能），你只要回到 repository，
用同樣的「Upload files」把新的 `index.html` 上傳覆蓋，Pages 會自動更新（約 1 分鐘生效）。

### 如果你比較熟悉 git 指令

```bash
git init
git add index.html
git commit -m "發布新人培訓紀錄表"
git branch -M main
git remote add origin https://github.com/你的帳號/training-tracker.git
git push -u origin main
```
再到 GitHub 網站上的 Settings → Pages 設定成 Deploy from branch（同上第 5～6 步）。

---

## 二、夥伴們怎麼使用、資料存在哪裡

這個網頁是「純前端」網頁，**沒有後台資料庫**，所以：

- 每個人打開網址後，看到的是自己瀏覽器裡的資料，不會跟別人共用或互相看到。
- 資料**不會自動儲存**（瀏覽器重新整理或關閉分頁就會清空），所以每次填寫完，
  一定要點畫面右上角 **💾 匯出備份**，下載一個 JSON 檔保存起來。
- 下次要繼續填寫時，先點 **📥 匯入備份**，把上次下載的 JSON 讀回來即可接續使用。

### 讓夥伴把紀錄回傳給你彙整

1. 夥伴在自己電腦上打開網址，建立他負責的新人、填寫進度。
2. 填完後點 **💾 匯出備份**，把 JSON 檔傳給你（Line、Email、雲端硬碟都可以）。
3. 你打開同一個網址，點 **📥 匯入備份**，選擇夥伴傳來的 JSON。
   - 如果你畫面上已經有其他新人資料，會跳出選單問你要「**合併加入**」還是「**取代目前資料**」。
   - 選「**合併加入**」，就能把不同夥伴傳來的名單，逐步彙整成一份完整的團隊總覽。
4. 建議固定一個頻率（例如每週）請大家回傳一次 JSON，你這邊持續合併，
   就能在總覽頁看到全團隊的新人培訓進度統計。

> 因為資料只存在各自瀏覽器裡，公開網址本身不會外洩任何人的培訓紀錄——
> 除非有人自己把 JSON 檔案傳出去。

---

## 三、檔案內容

- `index.html`：整個網頁（含樣式與程式碼），單一檔案，上傳這個就好。
