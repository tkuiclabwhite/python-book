# 章節格式速查表

寫新章節時，複製一份現有的 `.md` 檔案（例如 `ch1_variables.md`），保留最上面的 frontmatter，然後照下面的語法寫內文。

## 1. Frontmatter（每個章節檔案開頭必備，照抄就好）

```
---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
```

這段告訴 Jupyter Book「這份檔案裡的程式碼要真的執行」，沒有這段，程式碼區塊只會是靜態文字。

## 2. 標題

```
# 第 X 章：標題        ← 章節主標題，一個檔案只用一次
## 子標題              ← 分節
### 小節               ← 更細的分節
```

## 3. 可執行的程式碼

```` `
```{code-cell} ipython3
name = "Yk"
print(name)
```
```` `

建置時這段會真的被執行，輸出結果自動顯示在程式碼下方（不用自己貼結果）。

## 4. 一般文字排版

```
**粗體**
*斜體*
`行內程式碼`

- 項目一
- 項目二

1. 第一步
2. 第二步

[連結文字](https://example.com)

![圖片說明](圖片網址)
```

## 5. 提示框（note / warning / tip）

這是 MyST 特有的功能，適合放重點提醒或常見錯誤：

```` `
```{note}
這裡放補充說明。
```

```{warning}
這裡放常見錯誤或要特別小心的地方。
```

```{tip}
這裡放小技巧。
```
```` `

## 6. 練習題 + Colab 連結（每章結尾固定格式）

```
## 練習題

題目說明文字...

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tkuiclabwhite/python-book/blob/main/notebooks/chX_exercise.ipynb)
```

`chX_exercise.ipynb` 記得換成這一章對應的練習檔名，並且要真的把這個 notebook 檔案放進 `notebooks/` 資料夾、push 上 GitHub，連結才會生效。

## 7. 寫完之後

1. 在 `_toc.yml` 的 `chapters` 底下加一行 `- file: 新檔名`
2. 本機跑 `jupyter-book build .` 檢查有沒有跑出錯誤（程式碼有 bug 的話，建置會直接失敗並顯示錯誤訊息，等於自動幫你抓 code 有沒有問題）
3. 確認 `_build/html/index.html` 打開來排版正確
4. `python3 -m ghp_import -n -p -f _build/html`（或你已經修好 PATH 就直接 `ghp-import ...`）發布
