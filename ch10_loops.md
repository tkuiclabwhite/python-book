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

# 第二章：迴圈

迴圈可以想成「重複做同一件事」的機器，你告訴它要做幾次、或做到什麼條件為止，它就會自動重複執行。

## for 迴圈

知道要重複幾次的時候，用 `for` 迴圈最直接。

```{code-cell} ipython3
for i in range(5):
    print(f"第 {i} 次")
```

## while 迴圈

不知道要重複幾次、要看條件決定要不要繼續的時候，用 `while` 迴圈。

```{code-cell} ipython3
count = 0
while count < 3:
    print(f"count = {count}")
    count += 1
```

```{warning}
小心無窮迴圈：如果條件永遠是 True（例如忘記寫 `count += 1`），迴圈會一直跑下去不會停。
```

## 練習題

試著寫一個迴圈，印出 1 到 10 之間所有偶數。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tkuiclabwhite/python-book/blob/main/notebooks/ch2_exercise.ipynb)
