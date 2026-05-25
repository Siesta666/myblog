---
title: "一维无限深势阱的定态解"
slug: "infinite-well"
description: "用边界条件理解量子化，而不是把能级公式硬背下来。"
date: 2026-05-25T16:40:00+08:00
lastmod: 2026-05-25T16:40:00+08:00
draft: false
categories:
  - "量子力学"
tags:
  - "薛定谔方程"
  - "边界条件"
  - "能级量子化"
series:
  - "量子力学基础"
math: true
toc: true
comments: false
license: "CC BY-NC-SA 4.0"
---

考虑粒子被限制在 $0<x<L$ 内，势能为

$$
V(x)=
\begin{cases}
0, & 0<x<L, \\
\infty, & \text{otherwise}.
\end{cases}
$$

阱外波函数为零，边界条件要求

$$
\psi(0)=\psi(L)=0.
$$

## 定态方程

阱内的定态薛定谔方程为

$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}=E\psi.
$$

令 $k^2=2mE/\hbar^2$，通解为

$$
\psi(x)=A\sin kx+B\cos kx.
$$

由 $\psi(0)=0$ 得 $B=0$，由 $\psi(L)=0$ 得

$$
\sin kL = 0 \Rightarrow kL=n\pi,\quad n=1,2,3,\dots
$$

于是能量本征值为

$$
E_n=\frac{n^2\pi^2\hbar^2}{2mL^2}.
$$

归一化后，波函数为

$$
\psi_n(x)=\sqrt{\frac{2}{L}}\sin\frac{n\pi x}{L}.
$$

## 物理图像

能级离散来自边界条件。只有半波长能够整数次“塞进”盒子里的驻波，才是允许态。基态 $n=1$ 不是静止态，它仍然有非零能量，这就是零点能。

## 小结

无限深势阱是量子化最清楚的模型之一：微分方程给出波形，边界条件筛掉大多数解，归一化让概率解释成立。
