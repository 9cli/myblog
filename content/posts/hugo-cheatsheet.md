---
title: "Hugo 博客管理指令全书 (极速复制版)"
date: 2026-04-21T02:36:32+0800
draft: false
tags: ["Tool", "Guide"]
---

这份手册旨在提供最快的操作体验。所有多行指令已合并，点击右上角即可**一键复制**全套动作。

### 🚀 一键同步部署
执行以下代码块，将自动进入目录、暂存修改、提交并推送到 GitHub：

```bash
cd ~/myblog && git add . && git commit -m "update" && git push origin main
```

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

**1. 修改显示标题 (修改文件内部的 title 字段)**
建议直接用文本编辑器打开文件修改，或者用这条指令（替换“新标题”和“文件名”）：
```bash
sed -i 's/^title: .*/title: "你的新标题"/' ~/myblog/content/posts/文件名.md
```

**2. 修改文件名 (即修改文章的 URL 链接地址)**
```bash
mv ~/myblog/content/posts/旧文件名.md ~/myblog/content/posts/新文件名.md
```

---

### 📂 删除与清理

**删除指定文章**
```bash
rm ~/myblog/content/posts/filename.md
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
