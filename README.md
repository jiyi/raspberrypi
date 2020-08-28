## 设置键盘
默认设置，使用dvorak布局，caps lock做ctrl键，两个shift键同时按做 caps lock
```bash
# /etc/default/keyboard
XKBMODEL=pc105
XKBLAYOUT=us
XKBVARIANT=dvorak
XKBOPTIONS="ctrl:nocaps,shift:both_capslock"
BACKSPACE=guess
```

蓝牙键盘替换ESC键
```bash
# xmodmap 这个文件
keycode 49 = Escape asciitilde
keycode 9 = grave NoSymbol
```

参考：
https://www.zouyesheng.com/xmodmap-usage.html