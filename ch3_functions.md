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

# 第三章：函式

函式就像是一台自動販賣機：你投入原料（參數），它幫你處理好，吐出結果（回傳值），不用每次都重新寫一次流程。

```{code-cell} ipython3
def greet(name):
    return f"哈囉，{name}！"

print(greet("學弟"))
print(greet("學妹"))
```

## 有預設值的參數

```{code-cell} ipython3
def add(a, b=10):
    return a + b

print(add(5))
print(add(5, 20))
```

## 練習題

寫一個函式，輸入一個數字，回傳它是不是偶數（回傳 `True` 或 `False`）。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tkuiclabwhite/python-book/blob/main/notebooks/ch3_exercise.ipynb)
