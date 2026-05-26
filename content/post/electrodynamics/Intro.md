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

$$
\nabla \times \mathbf{F} = \lim_{S \rightarrow 0}\frac{\oint_C \mathbf{F}\cdot \mathrm{d}\mathbf{l}}{S}
$$

### 曲线坐标系

我们在处理具体问题的时候，通常不会遇到方方正正的电场，大部分场都是球对称或柱对称的，于是我们需要引入曲线坐标系来描述空间的场，接下来我将介绍**柱坐标系**和**球坐标系**。

#### 柱坐标系

柱坐标系使用 $(r, \theta, z)$ 来表述场的空间位置，相当于极坐标的三维扩展版，我们可以得到笛卡尔坐标系和柱坐标系的变换。

我们记 $(X,Y,Z)$ 是笛卡尔坐标系中的位置表述，得到：

$$
\begin{aligned}
  r &= \cos{\theta}X + \sin{\theta}Y\\
  \theta &= \arctan{\frac{Y}{X}}\\
  Z&=z
\end{aligned}
$$

这种变换不是线性变换，我们不能直接找到一个矩阵来表示这种非线性变换，但是我们可以使用雅可比矩阵来表示小区域的变换 $\frac{\partial Q_i}{\partial q_j}$ ，这相当于是一种局部线性化处理。

我们还需要关注柱坐标系中的微分算子：

$$
\begin{aligned}
  \nabla f &= \frac{\partial f}{\partial r}\hat{r} + \frac{\partial f}{r \partial \theta }\hat{\theta} + \frac{\partial f}{\partial z}\hat{z}\\
  \nabla \cdot \mathbf{F} &= \frac{\partial r\mathbf{F}_r}{r\partial r} + \frac{\partial \mathbf{F}_{\theta}}{r\partial r} + \frac{\partial \mathbf{F}_z}{\partial  z} \\
  \nabla \times \mathbf{F} &=
  \begin{bmatrix}
    \hat{r} & r\hat{\theta} & \hat{z} \\
    \frac{\partial }{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial }{\partial z} \\
    \mathbf{F}_r & r \mathbf{F}_\theta & \mathbf{F}_z
  \end{bmatrix}
\end{aligned}
$$

#### 球坐标

