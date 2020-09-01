---
title: "Capistrano-db-task sync disable confirm 關閉確認視窗"
date: 2020-09-01T09:49:26+08:00
draft: false
---

工作上很常用到 `cap production db:pull` 來同步 production 環境上使用者產生的資料，雖然多問無礙，但每次都問實在很煩，特別是這種要跑一陣子 task 常常執行下去後就去幹別的事。

總之，我從原始碼找到這個 `SKIP_DATA_SYNC_CONFIRM` 參數，搭配 `direnv` 設定後以後就不需要再被問惹。





