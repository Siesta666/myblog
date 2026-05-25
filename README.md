# 物理学习笔记

这是一个使用 Hugo 和 Stack 主题搭建的物理学习笔记发布网站，目标部署到 GitHub Pages。

## 本地预览

```powershell
hugo server --buildDrafts
```

## 新建笔记

```powershell
hugo new content post/topic/my-note.md
```

把 front matter 里的 `draft` 改成 `false` 后，文章会出现在首页和对应分类中。

## GitHub Pages 部署

仓库推送到 `main` 分支后，`.github/workflows/hugo.yaml` 会构建并发布 `public` 目录内容。第一次使用时，请在 GitHub 仓库页面进入 `Settings -> Pages`，把 `Source` 设置为 `GitHub Actions`。

当前项目仓库按 `Siesta666/myblog` 配置，默认访问地址为：

```text
https://siesta666.github.io/myblog/
```
