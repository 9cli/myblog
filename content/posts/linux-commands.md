---
title: "Linux 常用管理指令手册"
date: 2026-04-21T03:54:02+0800
draft: false
tags: ["Linux", "Guide"]
---

本手册收录了日常维护中最常用的 Linux 指令，旨在实现“极速查阅，一键执行”。

### 📂 文件与目录管理

**查看当前目录完整路径**
```bash
pwd
```

**列出文件（包含隐藏文件与详细信息）**
```bash
ls -la
```

**快速创建多层级目录**
```bash
mkdir -p path/to/directory
```

**删除文件或文件夹（慎用）**
```bash
rm -rf filename_or_dir
```

---

### 🔍 系统状态监控

**查看系统实时资源占用 (CPU/内存)**
```bash
top
```

**查看磁盘剩余空间（易读格式）**
```bash
df -h
```

**查看当前目录占用空间大小**
```bash
du -sh .
```

**查看内存使用情况**
```bash
free -m
```

---

### 🌐 网络与端口

**查看所有运行中的端口**
```bash
netstat -tunlp
```

**测试网络连通性**
```bash
ping -c 4 google.com
```

**查看本机 IP 地址**
```bash
ip addr
```

---

### 📦 软件包管理 (Ubuntu/Debian)

**更新软件源并升级所有已安装软件**
```bash
sudo apt update && sudo apt upgrade -y
```

**安装指定软件包**
```bash
sudo apt install -y package_name
```

**卸载并清理配置文件**
```bash
sudo apt purge package_name && sudo apt autoremove
```

---

### 🛠️ 系统操作

**查看最近 10 条执行过的命令**
```bash
history | tail -n 10
```

**立即重启系统**
```bash
sudo reboot
```

**立即关机**
```bash
sudo shutdown -h now
```

---

### 📝 快捷搜索

**在当前目录下递归搜索包含关键字的文件**
```bash
grep -r "keyword" .
```

**查找文件名中包含特定字符的文件**
```bash
find . -name "*keyword*"
```
