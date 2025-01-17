---
layout: post
title: js 的 new Date()
date: 2025-01-17
description: js 的 new Date()
---
 
## 前端 js 使用 new Date()
會根據「使用者裝置的時區」返回時間。
```
const now = new Date()
```

<br><br>

## 設定時區

### 台北時區
```
const now = new Date();
const taipeiTime = new Date(
    now.toLocaleString("en-US", { timeZone: "Asia/Taipei" })
);
```

### 日本時區
```
const now = new Date();
const tokyoTime = new Date(
    now.toLocaleString("en-US", { timeZone: "Asia/Tokyo" })
);
```

### UTC 時區
UTC 時間：世界協調時間，簡稱 UTC。 是最主要的世界時間標準，其以原子時的秒長為基礎，在時刻上儘量接近於<u>格林威治標準時間</u>。

```
const now = new Date();
const utcTime = new Date(
    now.toLocaleString("en-US", { timeZone: "UTC" })
);
console.log(utcTime);
```
執行結果：<br>
```
Fri Jan 17 2025 07:28:41 GMT+0800 (台北標準時間)
```

### 轉換為 UTC 時間格式
```
const now = new Date();
const utcDate = now.toUTCString();
console.log(utcDate);
```
執行結果：<br>
```
Fri, 17 Jan 2025 07:28:41 GMT
```

<br><br>

## 取得<u>日期+時間</u>
假設現在，台北時間：2025-01-17 15:28:41
```
const now = new Date();
const taipeiTime = new Date(
    now.toLocaleString("en-US", { timeZone: "Asia/Taipei" })
);
const year = taipeiTime.getFullYear();
const month = taipeiTime.getMonth();
const date = taipeiTime.getDate();
const hours = taipeiTime.getHours();
const minutes = taipeiTime.getMinutes();
const seconds = taipeiTime.getSeconds();
console.log('year => ' + year, 'month => ' + month, 'date => ' + date, 'hours => ' + hours, 'minutes => ' + minutes, 'seconds => ' + seconds);
```

執行結果：<br>
```
year => 2025 month => 0 date => 17 hours => 15 minutes => 28 seconds => 41
```
備註：1月回傳 0、2月回傳 1、3月回傳 2 ...