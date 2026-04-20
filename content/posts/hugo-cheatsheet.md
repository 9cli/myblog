---
title: "Hugo博客管理指令"
date: 2026-04-21T02:42:25+0800
draft: false
weight: 1
tags: ["Tool", "Guide"]
---

这份手册旨在提供最快的操作体验。所有多行指令已合并，点击右上角即可**一键复制**全套动作。

### 🚀 一键同步部署
执行以下代码块，将自动进入目录、暂存修改、提交并推送到 GitHub：

```bash
cd ~/myblog && git add . && git commit -m "update" && git push origin main
```

---

### 📌 如何置顶文章
在文章开头的 `---` 之间添加 `weight` 参数：
- `weight: 1` (最高置顶)
- `weight: 2` (次之)
*注意：数字越小，位置越靠前。*

---

### 📝 文章管理 (新建与查看)

**新建文章**
```bash
hugo new posts/new-article.md
```

**查看文章列表 (按时间倒序)**
```bash
ls -lt ~/myblog/content/posts/
```

---

### ✏️ 修改标题与文件名

**1. 修改显示标题**
```bash
sed -i 's/^title: .*/title: "你的新标题"/' ~/myblog/content/posts/文件名.md
```

**2. 修改文件名 (URL 地址)**
```bash
mv ~/myblog/content/posts/旧文件名.md ~/myblog/content/posts/新文件名.md
```

---

### 🔍 搜索与状态

**全文内容搜索 (替换关键字)**
```bash
grep -r "关键字" ~/myblog/content/posts/
```

**查看所有草稿文章**
```bash
grep -r "draft: true" ~/myblog/content/posts/
```

---

### 🛠️ 预览与维护

**本地预览 (访问 http://localhost:1313)**
```bash
cd ~/myblog && hugo server -D
```

**一键发布所有草稿**
```bash
sed -i 's/draft: true/draft: false/g' ~/myblog/content/posts/*.md
```

**查看最近 5 次提交记录**
```bash
git log -n 5 --oneline
```

---

### 🖼️ 图片引用模板

```markdown
![描述](https://your-cdn-domain.com/image.jpg)
```
