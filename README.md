[English](./README.md) · [简体中文](./README-zh.md)

# defaults-write

Make your mac better.

> You Don’t Have to Know Everything. You Just Have to Know Where to Find It. —— Albert Einstein

## Table of Contents

- [Add Blank Spaces to Left Side of the Dock to Better Organize App(where the Applications Are)](#add-blank-spaces-to-left-side-of-the-dock-to-better-organize-appwhere-the-applications-are)
- [Add Narrow Spaces to Left Side of the Dock to Better Organize Apps(where the Applications Are)](#add-narrow-spaces-to-left-side-of-the-dock-to-better-organize-appswhere-the-applications-are)
- [Add Blank Spaces to Right Side of the Dock to Better Organize App(where the Trash is)](#add-blank-spaces-to-right-side-of-the-dock-to-better-organize-appwhere-the-trash-is)
- [Add Narrow Spaces to Right Side of the Dock to Better Organize Apps(where the Trash is)](#add-narrow-spaces-to-right-side-of-the-dock-to-better-organize-appswhere-the-trash-is)
- [Remove the Auto-Hide Dock Delay](#remove-the-auto-hide-dock-delay)
- [Speed Up Mission Control Animations](#speed-up-mission-control-animations)
- [Return to Default Mission Control Animation Speeds](#return-to-default-mission-control-animation-speeds)
- [Make Hidden App Icons Translucent in the Dock](#make-hidden-app-icons-translucent-in-the-dock)
- [Stop Full Names from Copying with Email Addresses in OS X Mail](#stop-full-names-from-copying-with-email-addresses-in-os-x-mail)
- [Enable Text Selection in Quick Look Windows](#enable-text-selection-in-quick-look-windows)
- [Disable the “Are you sure you want to open this application?” dialog](#disable-the-are-you-sure-you-want-to-open-this-application-dialog)
- [Show indicator lights for open applications in the Dock](#show-indicator-lights-for-open-applications-in-the-dock)
- [Enable the status bar in Finder](#enable-the-status-bar-in-finder)
- [Empty Trash securely by default](#empty-trash-securely-by-default)
- [Always show expanded save dialogs](#always-show-expanded-save-dialogs)
- [Define where to save screenshots](#define-where-to-save-screenshots)
- [Reduce Transparency in Menu and Windows](#reduce-transparency-in-menu-and-windows)
- [Show Debug Menu](#show-debug-menu)
- [Hide Desktop Icon](#hide-desktop-icon)
- [Always Show Hidden Files in the Finder](#always-show-hidden-files-in-the-finder)
- [Change the Rows of Launchpad](#change-the-rows-of-launchpad)
- [Change the Columns of Launchpad](#change-the-columns-of-launchpad)
- [Reset Layout of Launchpad](#reset-layout-of-launchpad)
- [Show Path Bar in Finder](#how-path-bar-in-finder)
- [Set Current Folder as Default Search Scope](#set-current-folder-as-default-search-scope)

### Add Blank Spaces to Left Side of the Dock to Better Organize App(where the Applications Are)

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Add Narrow Spaces to Left Side of the Dock to Better Organize Apps(where the Applications Are)

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="small-spacer-tile";}' && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Add Blank Spaces to Right Side of the Dock to Better Organize App(where the Trash is)

```bash
defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Add Narrow Spaces to Right Side of the Dock to Better Organize Apps(where the Trash is)

```bash
defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="small-spacer-tile";}' && killall Dock
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
defaults write com.apple.dock showhidden -bool YES && killall Dock
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

### Disable the “Are you sure you want to open this application?” dialog

```bash
defaults write com.apple.LaunchServices LSQuarantine -bool false
```

[⬆️ Back to top](#defaults-write)

### Show indicator lights for open applications in the Dock

```bash
defaults write com.apple.dock show-process-indicators -bool true && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Enable the status bar in Finder

```bash
defaults write com.apple.finder ShowStatusBar -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Empty Trash securely by default

```bash
defaults write com.apple.finder EmptyTrashSecurely -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Always show expanded save dialogs

```bash
defaults write -g NSNavPanelExpandedStateForSaveMode -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Define where to save screenshots

```bash
defaults write com.apple.screencapture location -string "$HOME/Desktop"
```

[⬆️ Back to top](#defaults-write)

### Reduce Transparency in Menu and Windows

```bash
defaults write com.apple.universalaccess reduceTransparency -bool true
```

[⬆️ Back to top](#defaults-write)

### Show Debug Menu

```bash
defaults write com.apple.appstore ShowDebugMenu -bool true
```

[⬆️ Back to top](#defaults-write)

### Hide Desktop Icon

```bash
defaults write com.apple.finder CreateDesktop -bool false && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Always Show Hidden Files in the Finder

```
defaults write com.apple.finder AppleShowAllFiles -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Change the Rows of Launchpad

```
defaults write com.apple.dock springboard-rows -int 6 && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Change the Columns of Launchpad

```
defaults write com.apple.dock springboard-columns -int 8 && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Reset Layout of Launchpad

```
defaults write com.apple.dock ResetLaunchPad -bool true && killall Dock
```

[⬆️ Back to top](#defaults-write)

### Show Path Bar in Finder

```bash
defaults write com.apple.finder ShowPathbar -bool true && killall Finder
```

[⬆️ Back to top](#defaults-write)

### Set Current Folder as Default Search Scope

```bash
defaults write com.apple.finder FXDefaultSearchScope -string "SCcf" && killall Finder
```

[⬆️ Back to top](#defaults-write)
