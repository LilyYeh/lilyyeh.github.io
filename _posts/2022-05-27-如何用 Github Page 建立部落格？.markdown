---
layout: post
title: 如何用 Github Page 建立部落格？
date: 2022-05-27 00:00:00 +0300
description: 如何用 Github Page 建立部落格？ # Add post description (optional)
img: github-page.png # Add image post (optional)
---

#### 步驟1. Github Page Repository 建置
- 建置教學 → <a target="_blank" href="https://pages.github.com/">Github Page</a> 。
- 「User or organization site」是建立個人或公司網頁。
- 「Project site」是建立一個專案的 document。

❤︎小提醒：創建 Repository - username.github.io 名稱時，全部都要小寫英文。

#### 步驟2. Github Page Repository 建置
- 在這裡找一個自己喜歡的網頁主題 → <a target="_blank" href="https://jekyllthemes.io/free">Jekyll Theme</a> 。
- 從 github fork 出來到一個暫時的 repository，可命名為 tmp。
- 把 tmp clone 到 local。
- 斷開 local 和 github 的 remote 連結。
- local 的 tmp 重新命名為 username.github.io
- 建立 remote 到 Repository - username.github.io。
- push master
- 瀏覽 https://username.github.io 。

#### 步驟3. 在 local 瀏覽我的 Github Page
- 建置教學 → <a target="_blank" href="https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll">Testing your GitHub Pages site locally with Jekyll</a>
- 濃縮版，打開 terminal
  - 在 macOS 安裝 Homebrew 
  ```
  > /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
  - 安裝 Ruby
  ```
  > brew install chruby ruby-install
  > ruby-install ruby 3.3.5
  > ruby -v
  > echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zprofile
  > echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zprofile
  > echo "chruby ruby-3.3.5" >> ~/.zprofile
  ```
  - 安裝 Jekyll
  ```
  > gem install jekyll
  > jekyll -v
  ```
  - 安裝 bundler
  ```
  > gem install bundler
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
  ❤︎小提醒：若無法啟動成功，可能是 ruby 和 jekyll 版本相容性問題，請見[建置教學](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)。
  - 瀏覽 http://localhost:4000