---
title: "如何設定 Windows 10 免密碼自動登入, 登入後自動執行挖礦"
date: 2021-04-26T01:26:21+08:00
tags: [挖礦,加密貨幣]
series: 加密貨幣
draft: false
---

大家安裝礦機的時候通常獨立一台，跟自己平常用的電腦分開對吧？

接著分享我的設定流程，設定好之後萬一斷電，當機，只要重開機礦機就會自動開始挖礦！

本篇使用 `Windows10` ，其他OS並不在本篇範圍內


## 設定 Windows 10 自動登入

微軟似乎在某個版本改掉免密碼登入的選項了，因此我們需要開啟 `regedit` 登錄檔編輯器。

![](https://i.imgur.com/mf5aOKL.png)

開啟後，在上方路徑列輸入

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\PasswordLess\Device`

(別傻傻地慢慢找，直接複製貼上啊ＸＤ)

將 `DevicePasswordLessBuildVersion` 的數值改為 `0`，完成後按確定儲存。 **重開機**

![](https://imgur.com/4zx6aAB.png)


**重開機** 後再次找到放大鏡輸入 `netplwiz`

![](https://i.imgur.com/5BL670t.png)


首先取消 `必須使用密碼登入.....`，按下套用之後重新輸入密碼，按下確認，最後再次重開機

![](https://i.imgur.com/VaIf5Jt.png)


如果設定都正確，重開機後就不需要密碼登入了！

## 設定自動啟動路經

接著打開你的挖礦程式，將執行擋建立捷徑

![](https://i.imgur.com/YT2Hpd6.png)

再打開一個資料夾，在路經輸入 `shell:startup`，把剛剛建立的捷徑複製過來就完成啦！

![](https://i.imgur.com/X4LA9TJ.png)

最後再次重開機，如果設定都正確，應該就會看到挖礦程式自動被執行了！


![](https://i.imgur.com/uKvSNMA.png)





### 相關連結
* 幣安交易所 https://www.binance.com/zh-TW/register?ref=TJTGK5HI
* MAX交易所 https://max.maicoin.com/signup?r=ab1234c1
* 顯卡挖以太幣 [{{< ref "/posts/simple-GPU-mining-eth-guide" >}}]({{< ref "/posts/simple-GPU-mining-eth-guide" >}})
---

