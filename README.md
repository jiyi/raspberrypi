# 我的树莓派安装设置
## 设置键盘
1. 默认设置，使用dvorak布局，caps lock做ctrl键，两个shift键同时按为 caps lock
```bash
# /etc/default/keyboard
XKBMODEL=pc105
XKBLAYOUT=us
XKBVARIANT=dvorak
XKBOPTIONS="ctrl:nocaps,shift:both_capslock"
BACKSPACE=guess
```
2. 蓝牙键盘替换ESC键与`键互换
```bash
# xmodmap 这个文件
keycode 49 = Escape asciitilde
keycode 9 = grave NoSymbol
```

参考：
https://www.zouyesheng.com/xmodmap-usage.html

## 拼音输入法
```bash
$ sudo apt install fcitx fcitx-sunpinyin fcitx-module-cloudpinyin
```
- 安装完成重启
- 用sunpinyin因为有自然码双拼
- cloudpinyin模块就算改成baidu也不能用……
- 增加dovrak布局
- 修改sunpinyin键盘布局