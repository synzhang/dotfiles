# Linux

## Initialization

```sh
# Switch to root
su

# Add user account to sudo group
/sbin/addgroup my_username sudo
```

Then logout and re-login.

## Drivers

- [Linux for T2](https://t2linux.org): Patches to Linux and associated distros for Apple T2-based devices.


## Package Manager

### Flatpak

```sh
sudo apt install flatpak

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

## Apps

Then restart system.

- [dotbot](https://github.com/anishathalye/dotbot): A tool that bootstraps your dotfiles.
- [Rime](https://rime.im/): A chinese input method.
  - [ibus-rime](https://github.com/rime/ibus-rime/): Rime Input Method Engine for Linux/IBus.
- [Chrome](https://www.google.com/chrome/): Google web browser.
- [Bitwarden](https://bitwarden.com/): Move fast and securely with the password manager trusted by millions.
- [asdf](https://github.com/asdf-vm/asdf): Extendable version manager with support for Ruby, Node.js, Elixir, Erlang & more.
- [yadm](https://github.com/TheLocehiliosan/yadm): Yet Another Dotfiles Manager.
- [ufw](https://code.launchpad.net/ufw): A frontend for iptables, designed to be easy to use.
- [Hyprland](https://github.com/hyprwm/Hyprland): Hyprland is a highly customizable dynamic tiling Wayland compositor that doesn't sacrifice on its looks.
- [Ulauncher](https://github.com/Ulauncher/Ulauncher/): Application launcher for Linux.
- [Nvim](https://github.com/neovim/neovim/): hyperextensible Vim-based text editor.
  - [NvChad](https://github.com/NvChad/NvChad): Blazing fast Neovim config providing solid defaults and a beautiful UI, enhancing your neovim experience.
- [Visual Studio Code](https://code.visualstudio.com/): Code editing. Redefined. Free. Built on open source. Runs everywhere.
- [Telegram](https://telegram.org/): Telegram is a cloud-based mobile and desktop messaging app with a focus on security and speed.
- [RustDesk](https://rustdesk.com/): Open source virtual / remote desktop infrastructure for everyone!
- [Motrix](https://motrix.app): A full-featured download manager.
- [Syncthing](https://syncthing.net/): A continuous file synchronization program. It synchronizes files between two or more computers in real time, safely protected from prying eyes.
- [Rclone](https://github.com/rclone/rclone): A command-line program to sync files and directories to and from different cloud storage providers.
- [Barrier](https://github.com/debauchee/barrier/): Barrier is software that mimics the functionality of a KVM switch, which historically would allow you to use a single keyboard and mouse to control multiple computers by physically turning a dial on the box to switch the machine you're controlling.
- [Pandoc](https://github.com/jgm/pandoc): A universal document converter.
- [ImageMagick](https://github.com/imagemagick/imagemagick): Used to create, edit, compose, or convert bitmap images, and supports a wide range of file formats.
- [FFmpeg](https://github.com/FFmpeg/FFmpeg): A collection of libraries and tools to process multimedia content such as audio, video, subtitles and related metadata.
- [HandBrake](https://github.com/HandBrake/HandBrake): A tool for converting video from nearly any format to a selection of modern, widely supported codecs.
- [Upscayl](https://github.com/upscayl/upscayl): Free and Open Source AI Image Upscaler.
- [Buzz](https://github.com/chidiwilliams/buzz): Buzz transcribes and translates audio offline on your personal computer. Powered by OpenAI's Whisper.
- [LocalSend](https://github.com/localsend/localsend): LocalSend is a free, open-source app that allows you to securely share files and messages with nearby devices over your local network, without needing an internet connection.
- [Timeshift](https://github.com/linuxmint/timeshift): System restore tool for Linux.
- [Waybar](https://github.com/Alexays/Waybar): Highly customizable Wayland bar for Sway and Wlroots based compositors.
- [PolyBar](https://github.com/polybar/polybar): A fast and easy-to-use status bar.
- [Rofi](https://github.com/davatorium/rofi): A window switcher, application launcher and dmenu replacement.
- [btop](https://github.com/aristocratos/btop): A monitor of resources.
- [fd](https://github.com/sharkdp/fd): A simple, fast and user-friendly alternative to 'find'.
- [fzy](https://github.com/jhawthorn/fzy): A fast, simple fuzzy text selector for the terminal with an advanced scoring algorithm.
- [fzf](https://github.com/junegunn/fzf): A general-purpose command-line fuzzy finder.
- [yazi](https://github.com/sxyazi/yazi): Blazing fast terminal file manager written in Rust, based on async I/O.
- [wget](https://www.gnu.org/software/wget): A free software package for retrieving files using HTTP, HTTPS, FTP and FTPS, the most widely used Internet protocols. 
- [p7zip](https://p7zip.sourceforge.net/): A command line port of 7-Zip for POSIX systems.
  - p7zip-full: provides utilities to pack and unpack 7z archives within a shell or using a GUI.
- [ranger](https://github.com/ranger/ranger): A VIM-inspired filemanager for the console.
- [Shutter](https://github.com/shutter-project/shutter): Screenshot tool for Linux.
- [Flameshot](https://github.com/flameshot-org/flameshot): Powerful yet simple to use screenshot software.
- [Xournal++](https://github.com/xournalpp/xournalpp/): A handwriting notetaking software with PDF annotation support.
- [bandwhich](https://github.com/imsnif/bandwhich): Terminal bandwidth utilization tool.


## Configurations

### System Proxy

```sh
sudo vim /etc/environment
```

```conf
export HTTP_PROXY="http://127.0.0.1:7890/"
export HTTPS_PROXY="http://127.0.0.1:7890/"
export FTP_PROXY="http://127.0.0.1:7890/"
export NO_PROXY="127.0.0.1,localhost"
```

### Input Method

IBus

```sh
ln -s ./ibus/rime/default.custom.yaml ~/.config/ibus/rime
ln -s ./ibus/rime/ibus_rime.yaml ~/.config/ibus/rime

# Optional
ibus-setup
```

### Fonts

```sh
sudo apt install font-manager
```

- [Source Han Sans | 思源黑体](https://github.com/adobe-fonts/source-han-sans)
- [Source Han Serif | 思源宋体](https://github.com/adobe-fonts/source-han-serif)

```sh
sudo mv windows_fonts/ /usr/share/fonts/windows_font/
sudo fc-cache -fv
```

https://www.youtube.com/watch?v=CPgMbyFI-88
https://blog.lilydjwg.me/2023/3/5/linux-fonts.216591.html

### Hyprland

#### Keybindings

| Keys | Action |
| :--  | :-- |
| <kbd>Super</kbd> + <kbd>Q</kbd> | quit active/focused window
| <kbd>Alt</kbd> + <kbd>F4</kbd> | quit active/focused window
| <kbd>Super</kbd> + <kbd>Del</kbd> | quit hyprland session
| <kbd>Super</kbd> + <kbd>W</kbd> | toggle window on focus to float
| <kbd>Alt</kbd> + <kbd>Enter</kbd> | toggle window on focus to fullscreen
| <kbd>Super</kbd> + <kbd>J</kbd> | toggle layout
| <kbd>Super</kbd> + <kbd>G</kbd> | toggle window group
| <kbd>Super</kbd> + <kbd>T</kbd> | launch kitty terminal
| <kbd>Super</kbd> + <kbd>E</kbd> | launch dolphin file explorer
| <kbd>Super</kbd> + <kbd>C</kbd> | launch vscode
| <kbd>Super</kbd> + <kbd>F</kbd> | launch firefox
| <kbd>Super</kbd> + <kbd>A</kbd> | launch desktop applications (rofi)
| <kbd>Super</kbd> + <kbd>Tab</kbd> | switch open applications (rofi)
| <kbd>Super</kbd> + <kbd>R</kbd> | browse system files (rofi)
| <kbd>F10</kbd> | mute audio output (toggle)
| <kbd>F11</kbd> | decrease volume (hold)
| <kbd>F12</kbd> | increase volume (hold)
| <kbd>Super</kbd> + <kbd>V</kbd> | clipboard history paste
| <kbd>Super</kbd> + <kbd>L</kbd> | lock screen
| <kbd>Super</kbd> + <kbd>Backspace</kbd> | logout menu
| <kbd>Super</kbd> + <kbd>K</kbd> | switch keyboard layout
| <kbd>Super</kbd> + <kbd>P</kbd> | drag to select area or click on a window to print
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>P</kbd> | print current screen
| <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>P</kbd> | print current screen (frozen)
| <kbd>Super</kbd> + <kbd>RightClick</kbd> | resize the window
| <kbd>Super</kbd> + <kbd>LeftClick</kbd> | change the window position
| <kbd>Super</kbd> + <kbd>MouseScroll</kbd> | cycle through workspaces
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>| resize windows (hold)
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>| move active window within the current workspace
| <kbd>Super</kbd> + <kbd>[0-9]</kbd> | switch to workspace [0-9]
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>[0-9]</kbd> | move active window to workspace [0-9]
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>[0-9]</kbd> | move active window to workspace [0-9] (silently)
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>S</kbd> | move window to special workspace
| <kbd>Super</kbd> + <kbd>S</kbd> | toogle to special workspace
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd> | disable hypr effects for gamemode
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>→</kbd> | next wallpaper
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>←</kbd> | previous wallpaper
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>↑</kbd> | next waybar mode
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>↓</kbd> | previous waybar mode
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>D</kbd> | toggle (theme <//> wall) based colors
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>T</kbd> | theme select menu
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>W</kbd> | wallpaper select menu
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>A</kbd> | rofi style select menu

### Sway

### Xfce

- [How to Make Xfce Look Better | Ver. 2.0](https://www.youtube.com/watch?v=gxd2BvUFRJA)

--- 

**References:**

https://www.bilibili.com/read/cv6952486/
https://blog.zzsqwq.cn/posts/clash-for-windows-on-linux/
https://distroid.net/set-system-proxy-debian/
https://www.appinn.com/barrier/
https://www.youtube.com/watch?v=KH-VC_wWI1M&t=188s&ab_channel=LinuxScoop
https://linux.cn/article-15955-1.html
https://www.trickster.dev/post/back-to-the-terminal-the-new-era-of-cli-and-tui-software
https://github.com/megabitsenmzq/Tutorials/blob/master/Debian/index.md
https://github.com/iDvel/rime-ice
