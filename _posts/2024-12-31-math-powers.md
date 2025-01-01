---
title: "[Math] Powers"
last_modified_at: 2024-12-31 15:31:15
categories:
  - Math
tags:
  - 
---

## Powers

수학에서 `Power`(거듭제곱)은 

* 어떤 수나 식을 자신과 반복적으로 곱하는 연산을 의미 
* 이는 **지수** (`exponent`)와 **밑** (`base`)으로 구성되며, 
* 일반적으로 $a^n$ 의 형태로 표현.
    * $a$: `base`, 반복해서 곱해지는 number나 expression을 의미.
    * $n$: `exponent`, `base`가 몇 번 곱해지는지를 나타내는 number.

## Properties

* $a^1=a$: exponent가 1이면 base 그대로 ($0^0= 0$)
* $a^0=1$: 수학적으로는 $a\ne 0$ 인 경우에만 정의되나, 프로그래머 입장에선 $0^0=1$인 경우가 많음(built-in operations에서).
* $0^n=0$
* $a^{-n}=\frac{1}{a}$: $a \ne 0$
* $a^m a^n=a^{m+n}$
* $\frac{a^m}{a^n}=a^{m-n}$
* $(a^m)^n=a^{mn}$
* $(x \times y)^n=x^ny^n$
