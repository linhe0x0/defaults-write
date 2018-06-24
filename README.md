# defaults-write

Make your mac better.

[English](./) · [简体中文](./README-zh.md)

## Table of Contents

- [Remove the Auto-Hide Dock Delay]()
- [Speed Up Mission Control Animations]()
- [Return to Default Mission Control Animation Speeds]()

### Remove the Auto-Hide Dock Delay

```bash
defaults write com.apple.Dock autohide-delay -float 0 && killall Dock
```

### Speed Up Mission Control Animations

```bash
// you can adjust the animation speeds by changing the number after the -float flag。
defaults write com.apple.dock expose-animation-duration -float 0.15 && killall Dock
```

### Return to Default Mission Control Animation Speeds

```bash
defaults delete com.apple.dock expose-animation-duration && killall Dock
```
