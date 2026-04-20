---
title: "Linux 命令大全（手册版）"
date: 2026-04-21T04:06:44+0800
draft: false
tags: ["Linux", "Manual", "Runoob"]
---

本篇文章参考菜鸟教程及官方手册整理，涵盖了 Linux 运维与开发中最常用的命令。

### 📂 文件与目录管理

**列出目录内容**
```bash
ls -ah
```

**切换工作目录**
```bash
cd /home/user
```

**显示当前路径**
```bash
pwd
```

**创建新目录**
```bash
mkdir new_folder
```

**删除空目录**
```bash
rmdir folder_name
```

**删除文件或目录（强制递归）**
```bash
rm -rf file_or_dir
```

**复制文件**
```bash
cp source_file dest_file
```

**移动或重命名文件**
```bash
mv old_name new_name
```

**创建符号链接（软连接）**
```bash
ln -s target link_name
```

---

### 📄 文件查看与编辑

**查看文件全文内容**
```bash
cat filename
```

**分屏查看大文件**
```bash
more filename
```

**逐页前后翻看文件**
```bash
less filename
```

**查看文件前 10 行**
```bash
head -n 10 filename
```

**查看文件最后 10 行（常用于日志）**
```bash
tail -n 10 filename
```

**在文件中查找字符串**
```bash
grep "keyword" filename
```

**统计文件行数、字数**
```bash
wc -l filename
```

---

### 🛡️ 权限与所有权

**修改文件权限（读写执行）**
```bash
chmod 755 filename
```

**修改文件所有者**
```bash
chown user:group filename
```

**以管理员权限执行命令**
```bash
sudo command
```

---

### ⚙️ 系统管理与监控

**显示系统实时进程**
```bash
top
```

**列出所有进程快照**
```bash
ps -aux
```

**终止进程**
```bash
kill -9 pid
```

**查看磁盘空间占用**
```bash
df -h
```

**查看目录占用大小**
```bash
du -sh
```

**查看内存使用情况**
```bash
free -h
```

**查看系统内核信息**
```bash
uname -a
```

---

### 🌐 网络管理

**显示网络接口信息**
```bash
ifconfig
```

**测试网络连接**
```bash
ping google.com
```

**显示网络状态与端口占用**
```bash
netstat -tpln
```

**下载网络文件**
```bash
wget https://url.com/file
```

**向 URL 发送请求**
```bash
curl -I https://blog.183112.xyz
```

---

### 📦 备份与压缩

**打包并压缩为 .tar.gz**
```bash
tar -czvf archive.tar.gz folder
```

**解压 .tar.gz 文件**
```bash
tar -xzvf archive.tar.gz
```

**压缩为 .zip**
```bash
zip -r archive.zip folder
```

**解压 .zip 文件**
```bash
unzip archive.zip
```

---

### 🔍 搜索与查找

**查找文件名**
```bash
find / -name "filename"
```

**快速定位文件路径**
```bash
locate filename
```

**查找命令的可执行位置**
```bash
which command_name
```

---

### 🛠️ 软件包管理 (Debian/Ubuntu)

**更新软件列表**
```bash
sudo apt update
```

**升级已安装软件**
```bash
sudo apt upgrade
```

**安装新软件**
```bash
sudo apt install package_name
```
