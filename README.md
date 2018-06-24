# defaults-write

Make your mac better.

[English](./) · [简体中文](./README-zh.md)

## Table of Contents

- [Remove the Auto-Hide Dock Delay](#remove-the-auto-hide-dock-delay)
- [Speed Up Mission Control Animations](#speed-up-mission-control-animations)
- [Return to Default Mission Control Animation Speeds](#return-to-default-mission-control-animation-speeds)
- [Make Hidden App Icons Translucent in the Dock](#make-hidden-app-icons-translucent-in-the-dock)

### Remove the Auto-Hide Dock Delay

```bash
defaults write com.apple.Dock autohide-delay -float 0 && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Speed Up Mission Control Animations

```bash
// you can adjust the animation speeds by changing the number after the -float flag。
defaults write com.apple.dock expose-animation-duration -float 0.15 && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Return to Default Mission Control Animation Speeds

```bash
defaults delete com.apple.dock expose-animation-duration && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Make Hidden App Icons Translucent in the Dock

```bash
defaults write com.apple.Dock showhidden -bool YES && killall Dock
```

[⬆️ Back to top](#defaults-write)
