---
title: "AJAX載入測試檔案 Load Video With Axios"
date: 2020-09-17T12:15:03+08:00
draft: false
---

昨天想說把檔案快取在 localstorage 可以減少上傳的步驟，結果被卡小問題卡著，後來想到直接用 ajax 載入本地檔案不是更輕鬆嗎？

於是昨天的全部廢掉，改成這樣..........

````js
if (DEV) {
  const testvideo = await request({
    url: "/test.mov",
    method: "GET",
    responseType: "blob" // important
  });
  this.$refs.video.src = URL.createObjectURL(testvideo.data);
  this.video = this.$refs.video;
  const buffer = await testvideo.data.arrayBuffer();
  handleAudio.call(this, buffer);
}
````


這樣可以省掉很多點來點去的時間....