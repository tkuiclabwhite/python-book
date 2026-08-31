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

# 第一章：變數與資料型態

Python 裡的變數就像是貼了標籤的箱子，你把東西放進去，之後就可以用標籤把東西拿出來用。

```{code-cell} ipython3
name = "Yk"
age = 25
is_student = True

print(name)
print(age)
print(is_student)
```

## 常見的資料型態

Python 裡最基本的幾種型態：

- `int`：整數，例如 `10`
- `float`：浮點數，例如 `3.14`
- `str`：字串，例如 `"hello"`
- `bool`：布林值，只有 `True` 或 `False`

```{code-cell} ipython3
a = 10        # int
b = 3.14      # float
c = "hello"   # str
d = True      # bool

print(type(a), type(b), type(c), type(d))
```

## 練習題

試著修改上面的程式碼，把 `name` 換成你自己的名字，`age` 換成你的年齡，看看輸出結果會怎麼變。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tkuiclabwhite/python-book/blob/main/notebooks/ch1_exercise.ipynb)
