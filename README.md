# defaults-write

Make your mac better.

[English](./) · [简体中文](./README-zh.md)

## Table of Contents

- [Add Blank Spaces to Dock to Better Organize Apps](#add-blank-spaces-to-dock-to-better-organize-apps)
- [Remove the Auto-Hide Dock Delay](#remove-the-auto-hide-dock-delay)
- [Speed Up Mission Control Animations](#speed-up-mission-control-animations)
- [Return to Default Mission Control Animation Speeds](#return-to-default-mission-control-animation-speeds)
- [Make Hidden App Icons Translucent in the Dock](#make-hidden-app-icons-translucent-in-the-dock)
- [Stop Full Names from Copying with Email Addresses in OS X Mail](#stop-full-names-from-copying-with-email-addresses-in-os-x-mail)
- [Enable Text Selection in Quick Look Windows](#enable-text-selection-in-quick-look-windows)

### Add Blank Spaces to Dock to Better Organize Apps

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

[⬆️ Back to top](#defaults-write)

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

### Stop Full Names from Copying with Email Addresses in OS X Mail

```bash
defaults write com.apple.mail AddressesIncludeNameOnPasteboard -bool false
```

[⬆️ Back to top](#defaults-write)

### Enable Text Selection in Quick Look Windows

```bash
defaults write com.apple.finder QLEnableTextSelection -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)
