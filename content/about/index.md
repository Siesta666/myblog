---
title: "关于"
description: "这个站点的写作方式和维护说明。"
date: 2026-05-25T16:45:00+08:00
lastmod: 2026-05-25T16:45:00+08:00
draft: false
math: true
toc: true
comments: false
license: false
---

这里是一个用 Hugo 和 Stack 主题搭建的物理学习笔记站点。

写作目标是把每个知识点拆成三个层次：

1. 物理图像：先说明问题在描述什么。
2. 数学推导：保留关键方程和边界条件。
3. 解题检查：用量纲、极限情况和符号方向检查结果。

新增笔记时可以运行：

```powershell
hugo new content post/topic/my-note.md
```

本地预览：

```powershell
hugo server --buildDrafts
```

发布时把 `draft` 改为 `false`，推送到 GitHub 的 `main` 分支后，GitHub Pages 会自动构建。
