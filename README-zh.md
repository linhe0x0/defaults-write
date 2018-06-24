# defaults-write

这些隐藏的命令会让你的 Mac 更好用。

[English](./) · [简体中文](./README-zh.md)

## 导航

- [取消自动隐藏 Dock 的触发时间](#取消自动隐藏-dock-的触发时间)
- [加快 Mission Control 的动画效果](#加快-mission-control-的动画效果)
- [重置为默认的 Mission Control 的动画速度](#重置为默认的-mission-control-的动画速度)
- [让 Dock 中隐藏的程序图标半透明](#让-dock-中隐藏的程序图标半透明)
- [拷贝 Mail.app 中的邮件地址时不使用全名](#拷贝-mailapp-中的邮件地址时不使用全名)
- [在“快速查看”中开启文本选择功能](#在快速查看中开启文本选择功能)

### 取消自动隐藏 Dock 的触发时间

```bash
defaults write com.apple.Dock autohide-delay -float 0 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 加快 Mission Control 的动画效果

```bash
// you can adjust the animation speeds by changing the number after the -float flag。
defaults write com.apple.dock expose-animation-duration -float 0.15 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 重置为默认的 Mission Control 的动画速度

```bash
defaults delete com.apple.dock expose-animation-duration && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 让 Dock 中隐藏的程序图标半透明

```bash
defaults write com.apple.Dock showhidden -bool YES && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 拷贝 Mail.app 中的邮件地址时不使用全名

```bash
defaults write com.apple.mail AddressesIncludeNameOnPasteboard -bool false
```

[⬆️ 返回顶部](#defaults-write)

### 在“快速查看”中开启文本选择功能

```bash
defaults write com.apple.finder QLEnableTextSelection -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)
