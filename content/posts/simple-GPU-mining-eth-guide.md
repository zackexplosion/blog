---
title: "每日出金！簡易又快速的以太幣顯卡挖礦教學"
description: "幣安是我找到最最最最最最好用的礦池了，每日約台北時間下午四點不限金額出金，一張卡挖礦也可以每天看得到你的收益，更是摸的到！"
date: 2021-04-03T23:44:53+08:00
tags: [挖礦,加密貨幣]
series: 加密貨幣
draft: false
---

### 首先，下載挖礦軟體

[連結](/PhoenixMiner_5.5c_Windows.zip) (防毒可能會靠北)： [下載按我按我按我按我按我按我按我](/PhoenixMiner_5.5c_Windows.zip)

解壓縮後，打開資料夾 `PhoenixMiner_5.5c_.....`

點兩下執行裡面的 `0_Ethereum-binance.bat` 即可開始挖礦，看到下面的畫面代表成功啦，詳細的內容後面再談。

![Imgur](https://imgur.com/3NoQSxg.png)

咦？那這樣到底挖給誰？ 不要急！後面就會教你怎麼設定

## 挖到自己的幣安礦池帳號

用預設值挖就會挖給我啦，感謝您的贊助！下面就來教大家如何挖到自己的帳號

### 註冊幣安

首先要註冊[幣安](https://www.binance.com/zh-TW/register?ref=TJTGK5HI)的礦池帳號，這是我找到最最最最最最好用的礦池了，每日約台北時間下午四點不限金額出金，一張卡挖礦也可以每天看得到你的收益，更是摸的到！

主要的兩個步驟

* 點這邊註冊 https://www.binance.com/zh-TW/register?ref=TJTGK5HI
* 註冊完成之後到這頁 https://pool.binance.com/en


接著我們要設定幣安的挖礦帳號

![](https://i.imgur.com/nOq0xYl.png)

按圖操作後會看到下面畫面

![](https://i.imgur.com/8rY75aU.png)

輸入你的帳號名稱之後記得選擇挖礦的帳號類型，這邊我們要挖的是以太幣，所以選擇 `ethash`


### 設定挖礦程式

用任意一款文字編輯器打開 `0_Ethereum-binance.bat` 會看到

```bat
PhoenixMiner.exe -powlim -40 -pool ethash.poolbinance.com:8888 -wal zackexplosion -worker rig1 -epsw x -asm 2 -dbg -1 -allpools 1 -mode 1 -coin eth
pause
```

將其中這段 `-wal zackexplosion` 修改為你剛剛填寫的幣安挖礦帳號


例如

```bat
PhoenixMiner.exe -powlim -40 -pool ethash.poolbinance.com:8888 -wal yolo_zackexplosion -worker rig1 -epsw x -asm 2 -dbg -1 -allpools 1 -mode 1 -coin eth
pause
```

關掉再執行，就可以挖到自己的帳號啦！

接著過大約十分鐘後到 https://pool.binance.com/en/statistics 應該就能看到挖礦效能的圖表出現了！

![](https://i.imgur.com/z9epmLS.png)

最後，礦池會在每日早上八點結算，出金時間不一定，但最晚會在隔天晚上六點前出金（上面都有寫）

![](https://i.imgur.com/Q2tWbYh.png)


### 出金領錢啦

嗯...那接下來要怎麼把以太幣換回新台幣呢？ 有興趣了解的再留言跟我說吧