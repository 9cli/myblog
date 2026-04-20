---
title: "Hugo 博客管理指令集 (一键复制版)"
date: 2026-04-21T02:20:46+0800
draft: false
tags: ["Tool", "Guide"]
---

这份手册包含了管理本博客的所有常用命令。鼠标悬停在代码块右上角即可**一键复制**。

### 🚀 核心：发布三部曲
每当修改了文章或配置，请依次执行以下命令：

```bash
cd ~/myblog
git add .
git commit -m "update: content change"
git push origin main
```

---

### 📝 文章操作

**创建新文章**
```bash
hugo new posts/new-article.md
```

**删除指定文章**
```bash
rm ~/myblog/content/posts/文件名.md
```

**查看所有文章（按时间排序）**
```bash
ls -lt ~/myblog/content/posts/
```

---

### 🖼️ 图片引用 (R2 图床)
将上传到 Cloudflare R2 的图片粘贴至此处：

```markdown
![图片描述](https://img.183112.xyz/image-name.jpg)
```

---

### 🛠️ 本地调试与预览
如果你想在正式发布前检查排版：

```bash
cd ~/myblog && hugo server -D
```
*执行后访问：http://localhost:1313*

---

### 🔍 状态检查
查看哪些文章目前处于“草稿”状态（不会显示在前端）：

```bash
grep -r "draft: true" ~/myblog/content/posts/
```
