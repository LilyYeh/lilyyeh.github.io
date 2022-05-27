---
layout: post
title: 如何用 Github Page 建立部落格？
date: 2022-05-27 00:00:00 +0300
description: 如何用 Github Page 建立部落格？ # Add post description (optional)
img: github-page.png # Add image post (optional)
---

#### 步驟1. Github Page Repository 建置
- 建置教學 → [Github Page](https://pages.github.com/) 。
- 「User or organization site」是建立個人或公司網頁。
- 「Project site」是建立一個專案的 document。

❤︎小提醒：創建 Repository - username.github.io 名稱時，全部都要小寫英文。

#### 步驟2. Github Page Repository 建置
- 在這裡找一個自己喜歡的網頁主題 → [Jekyll Theme](https://jekyllthemes.io/free) 。
- 從 github fork 出來到一個暫時的 repository，可命名為 tmp。
- 把 tmp clone 到 local。
- 斷開 local 和 github 的 remote 連結。
- local 的 tmp 重新命名為 username.github.io
- 建立 remote 到 Repository - username.github.io。
- push master
- 瀏覽 https://username.github.io 。

#### 步驟3. 在 local 瀏覽我的 Github Page
- 建置教學 → [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
- 濃縮版，打開 terminal
  - 在 macOS 安裝 Homebrew 
  ```
  > /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
  - 安裝 Ruby
  ```
  > ruby-install ruby
  > ruby -v
  ```
  - 安裝 Jekyll
  ```
  > gem install jekyll
  ```
  - 安裝 bundler(:後的版本可自己調整)
  ```
  > gem install bundler:1.17.3
  ```
  - 安裝 Gemfile 裡的東東(like npm install)
  ```
  > cd myproject
  > bundle install
  ```
  - 安裝好之後會產生 Gemfile.lock
  - 啟動 web server
  ```
  > bundle exec jekyll serve
  ```
  ❤︎小提醒：若無法啟動成功，請查看 bundler 版本是否支援你的 jekyll。有些 Gemfile 沒有註明，只好調低 bundler 版本試試看。
  - 瀏覽 http://localhost:4000