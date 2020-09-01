---
title: "Macos Keyrepeat 速度調整"
date: 2020-09-01T11:09:55+08:00
draft: false
---

MacOS 預設的 keyrepeat 實在靠北慢，用下面的指令可以設定超過GUI能設定的上限

```
defaults write -g InitialKeyRepeat -int 12 # normal minimum is 15 (225 ms)
defaults write -g KeyRepeat -int 2 # normal minimum is 2 (30 ms)
```

這是我自己習慣的設定，詳細請參考下方來源連結
<https://apple.stackexchange.com/questions/10467/how-to-increase-keyboard-key-repeat-rate-on-os-x>