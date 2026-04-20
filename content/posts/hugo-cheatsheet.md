---
title: "Hugo 博客管理指令全书 (单行复制版)"
date: 2026-04-21T02:30:54+0800
draft: false
tags: ["Tool", "Guide"]
---

这份手册中的每一条命令都是独立的，方便你点击右上角直接复制执行。

### 🚀 核心：同步与推送
每当完成修改后，按顺序执行：

```bash
cd ~/myblog
```

```bash
git add .
```

```bash
git commit -m "update"
```

```bash
git push origin main
```

---

### 📝 文章管理

**新建文章**
```bash
hugo new posts/new-article.md
```

**删除指定文章**
```bash
rm ~/myblog/content/posts/filename.md
```

**查看文章列表（按时间排序）**
```bash
ls -lt ~/myblog/content/posts/
```

---

### 🔍 内容搜索与状态

**在所有文章中搜索内容**
```bash
grep -r "关键字" ~/myblog/content/posts/
```

**查看当前的草稿文章**
```bash
grep -r "draft: true" ~/myblog/content/posts/
```

---

### 🛠️ 运维与预览

**开启本地预览**
```bash
cd ~/myblog && hugo server -D
```

**将所有草稿一键发布**
```bash
sed -i 's/draft: true/draft: false/g' ~/myblog/content/posts/*.md
```

---

### 📜 Git 状态维护

**查看哪些文件被修改了**
```bash
git status
```

**查看最近 5 次提交记录**
```bash
git log -n 5 --oneline
```

---

### 🖼️ R2 图床引用模板

```markdown
![描述](https://your-cdn-domain.com/image.jpg)
```
