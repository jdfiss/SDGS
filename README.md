# 可能會用到的教學

---

## 📋 大綱

- [專案結構](#專案結構)
- [方案 A — 新增自己的資料夾](#方案-a--新增自己的資料夾上傳自己的-html)
- [方案 B — 修改某人的檔案](#方案-b--直接修改-nigas-file)
- [方案 C — 更新已上傳的版本](#方案-c--更新已上傳的版本)
- [常見問題](#常見問題-faq)

---

## 專案結構

```
SDGS/
├── niga/
│   ├── index.html      ← niga 的 SDG 11 頁面
│   └── images/         ← 本地圖片資料夾
├── [你的名字]/
│   └── index.html      ← 你自己的頁面（方案 A）
└── README.md
```

---

## 方案 A — 新增自己的資料夾（上傳自己的 HTML）

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
> 確認你的cmd內長這樣 `C:Users\YourName\SDGS`

### 步驟二：建立你的資料夾

```bash
mkdir 你的名字
```

### 步驟三：把你的 HTML 放進去

用檔案總管把你的 `index.html` 拖進 `你的名字/` 資料夾，或用指令：

```bash
copy "你的檔案路徑\index.html" 你的名字\index.html
```

### 步驟四：上傳到 GitHub

```bash
git add 你的名字/
git commit -m "add 你的名字 SDG page"
git push
```

---

## 方案 B — 直接修改 niga's file

### 步驟一：Clone 並進入資料夾

```bash
git clone https://github.com/jdfiss/SDGS.git
cd SDGS
```

### 步驟二：編輯檔案

用你習慣的編輯器打開 `niga/index.html` 修改。

### 步驟三：上傳變更

```bash
git add niga/index.html
git commit -m "update niga index"
git push
```

> **⚠️ 如果 push 失敗（rejected）**
>
> 表示有人比你先 push，先執行：
> ```bash
> git pull
> ```
> 解決衝突後再 push。

---

## 方案 C — 更新已上傳的版本

已經上傳過、想更新內容時使用。

### 步驟一：先同步遠端最新版本

```bash
cd SDGS
git pull
```

> **📌 為什麼要先 pull？**
>
> 如果其他組員在你上次 push 之後也 push 了新內容，
> 你的本地版本就落後了。
> 直接 push 會被 GitHub 拒絕（rejected），
> 所以養成習慣：**每次 push 前先 pull**。

### 步驟二：複製更新後的檔案

```bash
copy "你修改後的檔案路徑\index.html" 你的名字\index.html
```

若有本地圖片需上傳，請新增圖片資料夾(images)：

```bash
xcopy "你的圖片資料夾路徑" 你的名字\images\ /E /I
```

### 步驟三：提交並推上去

```bash
git add 你的名字/
git commit -m "update: 說明你改了什麼"
git push
```

---

## 常見問題 FAQ

**Q：沒裝 Git 怎麼辦？**

下載安裝：https://git-scm.com/downloads

**Q：push 要輸入密碼，輸入後說 authentication failed？**

GitHub 已不支援帳號密碼登入，需要用 Personal Access Token（PAT）：

1. GitHub → 右上角頭像 → Settings
2. Developer settings → Personal access tokens → Tokens (classic)
3. Generate new token → 勾選 `repo` → 產生
4. 複製那串 token，push 時當密碼貼上

**Q：不想裝 Git，可以直接在網頁上傳嗎？**

可以。進入 https://github.com/jdfiss/SDGS → 點進你的資料夾 → `Add file` → `Upload files`，直接拖檔案上去。
