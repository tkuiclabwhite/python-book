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

# 第二章：型別、變數與運算子

## 2-1 型別

Python 將資料分成數種 **型別 （type）** ，例如3.14是浮點數、"Hello, World！"是字串等，而型別決定了資料的表示方式，以及程式該如何處理資料。

Python 屬於 **動態型別 （dynamically typed）** 程式語言，資料在使用之前無須宣告型別，同時 Python 亦屬於 **強型別（strongly typed）** 程式語言，只能接受有明確定義的操作。

舉例來說，`print（"1+23"）`會印出1+23，因為 Python將“1+23"視為字串，而 `print（1+23）` 會印出24，因為 Python將1和23視為數值，1和23相加會得到24，但 `print（1+"23"）`則會發生錯誤，因為 Python將1和"23"視為數值和字串，而Python 並沒有明確定義數值和字串相加的方式。

Python 內建許多型別，包括：

- 數值型別 （numeric type）：int、float、complex、bool。

- 文字序列型別 （text sequence type）：str。

- 二元序列型別 （binary sequence type）：bytes、bytearray、memoryview。

- 序列型別（sequence type）：list、tuple、range。

- 集合型別 （set type）： set、frozenset。

- 對映型別 （mapping type）：dict。

在本章中，我們會簡單介紹 int（整數）、float（浮點數）、complex（複數）、bool（布林）、str（字串）等基本型別，以及 list（串列）、tuple（序對）、set（集合）、dict （字典）等容器型別，然後在第3章和第6章詳細說明這些型別的、處理與應用。至於其它比較少用的型別，有興趣的讀者可以參考 Python 說明文件。


### 2-1-1 數值型別(int、float、complex、bool)

### 2-1-2 字串型別(str)

### 2-1-3 list(串列)、tuple(序對)、set(集合)與dict(字典)

## 2-2 變數

### 2-2-1 變數命名規則

### 2-2-2 設定變數的值

## 2-3 常數

## 2-4 運算子

### 2-4-1 算術運算子

### 2-4-2 移位運算子

### 2-4-3 位元運算子

### 2-4-4 比較運算子

### 2-4-5 指派運算子

### 2-4-6 邏輯運算子

### 2-4-7 其它特殊符號

### 2-4-8 運算子的優先順序

## 2-5 輸出

## 2-6 輸入

## 學習評量

## 實例演練