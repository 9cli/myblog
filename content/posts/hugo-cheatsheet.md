---
title: "Hugo 博客管理指令全书 (通用版)"
date: 2026-04-21T02:26:47+0800
draft: false
tags: ["Tool", "Guide"]
---

这份手册包含了管理本博客的所有常用命令。

### 🚀 基础：同步三部曲
每当修改了文章或配置，请依次执行以下命令：

```bash
cd ~/myblog && git add . && git commit -m "update" && git push origin main
```

---

### 📝 内容管理
**新建/删除/查看**
```bash
hugo new posts/filename.md           # 新建文章
rm ~/myblog/content/posts/file.md    # 删除文章
ls -lt ~/myblog/content/posts/       # 按时间列出所有文章
```

**搜索与状态检查**
```bash
grep -r "关键字" ~/myblog/content/posts/    # 在所有文章中搜索内容
grep -r "draft: true" ~/myblog/content/posts/ # 查看哪些是草稿
```

---

### 🛠️ 运维与预览
**本地预览模式**
```bash
cd ~/myblog && hugo server -D
```
*执行后访问：http://localhost:1313*

**一键发布所有草稿**
```bash
sed -i 's/draft: true/draft: false/g' ~/myblog/content/posts/*.md
```

---

### 🖼️ R2 图床引用模板
在 Markdown 中插入已上传至 R2 的图片：

```markdown
![描述](https://your-cdn-domain.com/image-name.jpg)
```

---

### 📜 Git 状态维护
```bash
git status                  # 查看当前有哪些文件被修改但未提交
git log -n 5 --oneline      # 查看最近 5 次提交记录
```
