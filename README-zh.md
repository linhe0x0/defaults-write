# defaults-write

这些隐藏的命令会让你的 Mac 更好用。

[English](./) · [简体中文](./README-zh.md)

## 导航

- [取消自动隐藏 Dock 的触发时间]()
- [加快 Mission Control 的动画效果]()
- [重置为默认的 Mission Control 的动画速度]()

### 取消自动隐藏 Dock 的触发时间

```bash
defaults write com.apple.Dock autohide-delay -float 0 && killall Dock
```

### 加快 Mission Control 的动画效果

```bash
// you can adjust the animation speeds by changing the number after the -float flag。
defaults write com.apple.dock expose-animation-duration -float 0.15 && killall Dock
```

### 重置为默认的 Mission Control 的动画速度

```bash
defaults delete com.apple.dock expose-animation-duration && killall Dock
```
