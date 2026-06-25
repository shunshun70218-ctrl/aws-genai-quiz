# AWS GenAI 考試練習

AWS GenAI 認證題庫（共 97 題）的線上測驗練習網頁，自包含單檔 HTML，開瀏覽器即可作答。

## 🚀 線上作答

開啟 GitHub Pages 網址即可直接練習（部署後可用）：

> https://shunshun70218-ctrl.github.io/aws-genai-quiz/

## 測驗功能

- 每次隨機抽題、打亂順序（開始畫面可設定出題數量，最多 97 題）。
- 自動辨識單選 / 複選；複選題標示「請選 N 個」。
- 作答後即時顯示對錯、正確答案、考點背法。
- 每題上方標示「📄 原文件 Question #N」對應原始題號。
- 結束時統計正確率（圓環）、答對 / 答錯數、完整錯題回顧，並可「只練習錯題」。

## 檔案說明

| 檔案 | 說明 |
|------|------|
| `index.html` | GitHub Pages 入口，自動轉址到測驗網頁 |
| `AWS_GenAI_Quiz.html` | ⭐ 測驗網頁（自包含單檔，含全部題目） |
| `questions_full.json` | ⭐ 唯一權威資料來源：97 題的題目、選項、答案、考點背法 |
| `build_quiz.py` | 用 `questions_full.json` 重新產生測驗網頁 |
| `build_docx.py` | 用 `questions_full.json` 重新產生修正版 Word |
| `AWS_GenAI_Q1-Q97_題目格式_修正版.docx` | 修正版 Word（題目原文 + 答案 + 考點背法） |
| `製作步驟.md` | 完整製作步驟與流程紀錄 |

## 本機重新產生 / 修改題目

編輯 `questions_full.json`（唯一來源），改完後重新產生產出物：

```bash
python3 build_quiz.py   # → 重新產生 AWS_GenAI_Quiz.html
pip install python-docx
python3 build_docx.py   # → 重新產生修正版 Word
```

詳見 [`製作步驟.md`](製作步驟.md)。
