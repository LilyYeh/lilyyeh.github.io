---
layout: post
title: Git 如何 Push 到 GitHub Repository
date: 2024-11-11
description: Git 如何 Push 到 GitHub Repository
---
### 步驟 1. 在 github 上 new repository

### 步驟 2. 有兩種方式 push
1. http push 時會要求輸入 github 帳密。
2. ssh 產生一組公私鑰，把公鑰新增至 github。

### 步驟 3. 在 fork (Git 工具) add new remote
輸入 GitHub 的 repository 網址，產生連線。

### SSH Key 的建立與設定

存放 SSH Key 的位置
> ssh-keygen

> Enter file in which to save the key (/Users/username/.ssh/id_rsa):

接下來都按 Enter...

> cd /Users/username/.ssh/

會看到一組公鑰 id_rsa.pub、一組私鑰 id_rsa

> cat id_rsa.pub

複製公鑰到 GitHub 貼上
GitHub 公鑰設定位置：github → setting → SSH and GPG keys

### 專案目錄下，新增 .gitignore
撰寫 git 忽略更改的檔案