---
title: "Capistrano-db-task sync disable confirm 關閉確認視窗"
date: 2020-09-01T09:49:26+08:00
draft: false
---

工作上很常用到 `cap production db:pull` 來同步 production 環境上使用者產生的資料，雖然多問無礙，但每次都問實在很煩，特別是這種要跑一陣子 task 常常執行下去後就去幹別的事。

總之，我從原始碼找到這個 `SKIP_DATA_SYNC_CONFIRM` 參數，搭配 `direnv` 設定後以後就不需要再被問惹。





https://codepen.io/zackexplosion/pen/MWyPLrx

拜託，問問題前先學會問問題的工具，把問題整理好別人才好幫助你，你這樣全部亂塞到github誰看的懂啦ww

不過你的問題很簡單，只是```value```打成```Value```而已........