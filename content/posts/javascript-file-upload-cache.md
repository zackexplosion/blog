---
title: "加速 Javascript File Upload 開發流程/檔案預先選取/檔案儲存localstorage"
date: 2020-09-16T13:32:42+08:00
draft: false
---

每次寫上傳檔案的功能都很靠北的要一直自己重新點，累死，研究了一下怎麼存在localstorage，這樣只要選一次，之後reload就可以省略掉這步驟了。

```js
class DevCacheFile {
  key = "temp_file_cache";
  constructor() {}

  save(file, result) {
    // save dev file to cache
    const dataToSave = JSON.stringify({
      type: file.type,
      blob: Array.from(new Uint8Array(result))
    });
    localStorage.setItem(this.key, dataToSave);
  }

  restore() {
    var data = localStorage.getItem(this.key);
    if (!data) return null;
    data = JSON.parse(data);
    var blob = new Uint8Array(data.blob).buffer;
    blob = new Blob([blob]);
    var file = new File([blob], { type: data.type });
    return file;
  }
}
```

用法大概這樣

```js

    // whatever.js
    var file
    var devCacheFile = new DevCacheFile()
    var reader = new FileReader()
    reader.onload = () => {
      const result = reader.result;
      if (result.length <= 0) {
        console.error("error, videoFileAsBuffer is empty");
        return;
      }

      if (DEV) {
        // save dev file to cache
        devCacheFile.save(file, result);
      }

    };

    file = devCacheFile.restore();

    // 自己找地方放這個function，下面範例是 input[type=file] 的change事件
    handleSelectedFile(event) {
      file = event.target.files[0];
      reader.readAsArrayBuffer(file);
    }
```