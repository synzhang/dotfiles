# Linux

## Apps

- [Rime](https://rime.im/): A chinese input method.
  - [ibus-rime](https://github.com/rime/ibus-rime/): Rime Input Method Engine for Linux/IBus.
- [Chrome](https://www.google.com/chrome/): Google web browser.
- [Bitwarden](https://bitwarden.com/): Move fast and securely with the password manager trusted by millions.
- [ufw](https://code.launchpad.net/ufw): A frontend for iptables, designed to be easy to use.
- [Ulauncher](https://github.com/Ulauncher/Ulauncher/): Application launcher for Linux.
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

## Configuration

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

```shell
sudo mv windows_fonts/ /usr/share/fonts/windows_font/
sudo fc-cache -fv
```

https://www.youtube.com/watch?v=CPgMbyFI-88
https://blog.lilydjwg.me/2023/3/5/linux-fonts.216591.html

### Xfce

- [How to Make Xfce Look Better | Ver. 2.0](https://www.youtube.com/watch?v=gxd2BvUFRJA)

--- 

**References:**

https://www.bilibili.com/read/cv6952486/
https://blog.zzsqwq.cn/posts/clash-for-windows-on-linux/
https://distroid.net/set-system-proxy-debian/
https://www.appinn.com/barrier/
https://www.youtube.com/watch?v=KH-VC_wWI1M&t=188s&ab_channel=LinuxScoop