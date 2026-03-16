# SDGS 網頁程式設計 期末專題

## 專案結構預覽

```
SDGS/
├── index.html       ← jdfiss 的檔案
├── niga/
│   └── index.html   ← niga 的 SDG 11 頁面
└── 你的名字/
    └── index.html   ← 你的頁面
```

---

## 方法 A：新增自己的頁面（推薦）

### 步驟一：Clone 專案到電腦
```bash
git clone https://github.com/jdfiss/SDGS.git
cd SDGS
```
> **📌 git clone 做了什麼？**
>
> 1. 連線到 GitHub 上那個 repo
> 2. 在你目前所在的資料夾裡，自動建立一個叫 `SDGS` 的新資料夾
> 3. 把 repo 裡所有檔案下載進去
> 4. 同時記住這個 repo 的來源網址（之後 push 才知道要推去哪）
>
> `cd SDGS` 則是把終端機的位置切換進去那個資料夾，
> 之後的 git 指令才會針對這個 repo 生效。
> 
> 確認你的cmd畫面像這樣 `C:Users\YourName\SDGS>`


### 步驟二：建立自己的資料夾並放入檔案
用你的名字當資料夾名稱，把做好的 `.html` 複製進去並命名為 `index.html`。

Windows：
```cmd
mkdir 你的名字
copy "你的檔案路徑\xxx.html" 你的名字\index.html
```

或直接用**檔案總管**拖進去也可以。

### 步驟三：上傳到 GitHub
```bash
git add 你的名字/
git commit -m "Add 你的名字 project"
git push
```

---

## 方法 B：直接修改別人的頁面

> ⚠️ 修改前請先確認沒有其他人同時在改，以免產生衝突。

### 步驟一：Clone 並進入專案
```bash
git clone https://github.com/jdfiss/SDGS.git
cd SDGS
```

### 步驟二：用編輯器開啟修改
```
niga/index.html
```

### 步驟三：儲存並上傳
```bash
git add niga/index.html
git commit -m "更新 SDG11 頁面：說明你改了什麼"
git push
```

如果 push 失敗（代表有人比你先推）：
```bash
git pull
git push
```

---

## 常見問題

**Q：我沒有 Git？**  
下載安裝：https://git-scm.com/download/win

**Q：push 時要輸入密碼？**  
GitHub 需要用 Personal Access Token 代替密碼。  
到 GitHub → Settings → Developer settings → Personal access tokens → 產生一組，貼在密碼欄位。

**Q：只改一點點，可以在網頁上直接改嗎？**  
可以。進到 repo → 點開檔案 → 右上角鉛筆圖示 → 改完後按 Commit changes。
