---
title: "Intro"
slug: "Intro"
description: ""
date: 2026-05-25T21:13:10+08:00
lastmod: 2026-05-25T21:13:10+08:00
draft: false
categories:
  - "电动力学"
tags:
  - "数学"
  - "矢量分析"
series: [格里菲斯电动力学]
math: true
toc: true
comments: false
license: "CC BY-NC-SA 4.0"
---

## 电动力学中常用的数学基础

### 梯度、散度、旋度

此处在笛卡尔坐标系中描述上述的微分算子：

**梯度**：描述标量函数在空间中的变化速率，沿着梯度是函数上升最快的，其几何意义是**函数等值线/面的法向量**

$$
\begin{aligned}
\nabla f &= \frac{\partial f}{\partial x}\hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z}\\
&= \frac{\partial f}{\partial x_i}\hat{x_i}
\end{aligned}
$$

**散度**：描述矢量函数在空间中的发散程度，数学定义是：

$$
\begin{aligned}
\nabla \cdot \mathbf{F} &= \frac{\partial \textbf{F}_x}{\partial x} + \frac{\partial \textbf{F}_y }{\partial y} + \frac{\partial \textbf{F}_z}{\partial z}\\
& = \frac{\partial \mathbf{F}_i}{\partial x_i}
\end{aligned}
$$

我们可以使用使用一种朴素的方式求出散度：

$$
\nabla \cdot \mathbf{F} = \lim_{V \rightarrow 0}\frac{\oint_S \mathbf{F}\cdot\mathrm{d}\mathbf{a}}{V}
$$

**旋度**：描述矢量函数在空间中的旋转程度，数学定义是：

$$
\nabla \times \mathbf{F} = 
\begin{bmatrix}
  \hat{x} & \hat{y} & \hat{z} \\
  \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z}\\
  \mathbf{F}_x & \mathbf{F}_y & \mathbf{F}_z 
\end{bmatrix}
$$

我们也可以写成这样