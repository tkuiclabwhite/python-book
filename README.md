# Python 入門教材（Jupyter Book 版）

這是用 Jupyter Book 搭的最小可行架構，示範「翻書」的閱讀體驗＋可執行程式碼。

## 本機預覽

```bash
pip install "jupyter-book<2"
jupyter-book build .
```

打包完成後，打開 `_build/html/index.html` 就能在瀏覽器裡看到成品，左側有章節目錄，每頁底下有上一章／下一章的翻頁按鈕。

## 放到 GitHub Pages（免費 host 給學弟妹看）

```bash
jupyter-book build .
git add .
git commit -m "新增章節內容"
git push
ghp-import -n -p -f _build/html
```

執行後會把 `_build/html` 推到 `gh-pages` branch，去 repo 的 Settings → Pages 設定 `gh-pages` 當作來源，之後給學弟妹一個網址就能讀。

## 檔案結構

```
_config.yml       # 書名、作者、執行設定
_toc.yml          # 章節順序（目錄）
intro.md          # 首頁
```

## 怎麼加新章節

1. 新增一個 `.md` 檔，複製任一章的 frontmatter（開頭 `---` 之間那段）
2. 用 ```` ```{code-cell} ipython3 ```` 包住可執行的程式碼區塊
3. 在 `_toc.yml` 的 `chapters` 底下加一行 `- file: 新檔名`（不用副檔名）
4. 在 `notebooks/` 底下新增對應的練習 `.ipynb`
5. 在章節結尾貼上 Colab 徽章（記得把網址換成你自己的 repo）：
   ```
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/你的帳號/你的repo/blob/main/notebooks/檔名.ipynb)
   ```
6. 重新 `jupyter-book build .`

## Colab 徽章網址規則

`colab.research.google.com/github/{帳號}/{repo}/blob/{branch}/{路徑}.ipynb`

只要 `.ipynb` 檔案存在於你的 GitHub repo 裡（不用先手動開過 Colab），這個網址點下去 Colab 就會自動抓檔案內容開啟。所以流程是：notebook 檔案跟著整個 repo 一起 push 上 GitHub → 網址就會生效。

## 後續可以做的事

- 把 Colab 練習連結換成你自己開的 notebook
- 加入圖片、GIF 動圖解釋概念（Jupyter Book 支援 `![]()` 語法）
- 用 git 版控整個資料夾，之後每屆學弟妹接手教材時直接 `git clone`
