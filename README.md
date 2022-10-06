# My Computer Setup

## System

- [Homebrew](https://brew.sh/): The Missing Package Manager for macOS.

### Shell

- [Zsh](https://www.zsh.org/): Zsh is a shell designed for interactive use.
  - [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh): Oh My Zsh is an open source, community-driven framework for managing your zsh configuration.
  - [Powerlevel10k](https://github.com/romkatv/powerlevel10k): Powerlevel10k is a theme for Zsh. It emphasizes speed, flexibility and out-of-the-box experience.
- [Bash-it](https://github.com/Bash-it/bash-it): A community Bash framework.
- [fzf](https://github.com/junegunn/fzf): A command-line fuzzy finder.
- [z](https://github.com/rupa/z): Jump around.
- [tldr pages](https://tldr.sh/): Simplified and community-driven man pages.
- [exa](https://the.exa.website/): A modern replacement for ls.
- [bat](https://github.com/sharkdp/bat): A cat(1) clone with wings.
- [tree](https://formulae.brew.sh/formula/tree): Display directories as trees.

### SSH

1. Generating a new SSH key

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

2. Adding your SSH key to the ssh-agent

```
eval "$(ssh-agent -s)"

open ~/.ssh/config
# If the file doesn't exist, create the file.
# touch ~/.ssh/config
```

```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

If your SSH key file has a different name or path than the example code(`id_ed25519`), modify the filename or path to match your current setup.

3. Add your SSH private key to the ssh-agent and store your passphrase in the keychain

```
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
```

## Development

- [Visual Studio Code](https://code.visualstudio.com/): Code editing. Redefined. Free. Built on open source. Runs everywhere.
- [Git](https://git-scm.com/): Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
  - [Tig](http://jonas.github.io/tig/): Text-mode interface for Git.
  - [GitUI](https://github.com/extrawurst/gitui): Blazing fast terminal-ui for git written in Rust.
- [Node.js](https://nodejs.org/en/): Node.js is an open-source, cross-platform JavaScript runtime environment.
  - [n](https://github.com/tj/n): Node version management
  - [npm-check](https://github.com/dylang/npm-check): Check for outdated, incorrect, and unused dependencies.
- [Docker](https://www.docker.com/products/docker-desktop/): The fastest way to containerize applications.
- [Postman](https://www.postman.com/): Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration so you can create better APIs—faster.
- [Nerd Fonts](https://www.nerdfonts.com/): Nerd Fonts patches developer targeted fonts with a high number of glyphs (icons). Specifically to add a high number of extra glyphs from popular ‘iconic fonts’ such as Font Awesome, Devicons, Octicons, and others.

## App

- [1Password](https://1password.com/): The world’s most-loved password manager.
- [Chrome](https://www.google.com/chrome/): Google web browser.
- [Firefox](https://www.mozilla.org/en-US/firefox/new/): Get Firefox, a free web browser backed by Mozilla, a non-profit dedicated to internet health and privacy. Available now on Windows, Mac, Linux, Android and iOS.
- [Dropbox](https://www.dropbox.com/): Easy to use, reliable, private, and secure. It’s no wonder Dropbox is the choice for storing and sharing your most important files.
- [Google Drive](https://www.google.com/drive/): Store, share, and collaborate on files and folders from your mobile device, tablet, or computer.
- [Obsidian](https://obsidian.md/): Obsidian is a powerful knowledge base on top of a local folder of plain text Markdown files.
- [MarginNote](https://www.marginnote.com/): A brand new e-reader to better study and digest your books.
- [Mindnode](https://www.mindnode.com/): Mind Mapping & Outlining.
- [PDF Expert](https://pdfexpert.com/): The go-to PDF editor for iPhone, iPad and Mac We make it easy to edit, annotate, sign and organize PDFs.
- [Bitwarden](https://bitwarden.com/): Move fast and securely with the password manager trusted by millions.
- [Raycast](https://www.raycast.com/): Raycast is a blazingly fast, totally extendable launcher. It lets you complete tasks, calculate, share common links, and much more.
- [Figma](https://www.figma.com/): Build better products as a team. Design, prototype, and gather feedback all in one place with Figma.
- [Keka](https://www.keka.io/): The macOS file archiver Store more, share with privacy.
- [Calibre](https://calibre-ebook.com/): E-book management.
- [Sigil](https://sigil-ebook.com/): Sigil was designed to make it easy to create great ebooks using the EPUB format.
- [Telegram](https://telegram.org/): Telegram is a cloud-based mobile and desktop messaging app with a focus on security and speed.
- [WeChat](https://apps.apple.com/us/app/wechat/id414478124): A messaging and social media app made by Tencent.
- [iStat Menus](https://bjango.com/mac/istatmenus/): An advanced Mac system monitor for your menu bar.
- [CleanMyMac X](https://cleanmymac.com/): The most user-friendly problem fixer for Mac. Delete system junk, unwanted apps and malware, and tune your Mac for maximum speed. For a slow computer, use immediately.
- [Keyboard Maestro](https://www.keyboardmaestro.com/main/): The Premier Mac Automation Software.
- [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466): Use Microsoft Remote Desktop for Mac to connect to Azure Virtual Desktop, Windows 365, admin-provided virtual apps and desktops, or remote PCs.
- [IINA](https://iina.io/): The modern media player for macOS.
- [Aliyun Drive](https://www.aliyundrive.com/): A fast, non-intrusive and easy to share online drive made by Alibaba.
- [OBS Studio](https://obsproject.com/): Free and open source software for video recording and live streaming.
- [Kap](https://getkap.co/): Capture your screen.
- [Shottr](https://shottr.cc/): Shottr is a free macOS screenshot app with scrolling screenshots, OCR, annotation and measurement instruments.
- [Grammarly](https://www.grammarly.com/): Great Writing, Simplified. Compose bold, clear, mistake-free writing with Grammarly’s new AI-powered desktop app.
- [Karabiner-Elements](https://karabiner-elements.pqrs.org/): A powerful and stable keyboard customizer for macOS.
- [Sip](https://sipapp.io/): A better Color Picker for your Mac.
- [Motrix](https://motrix.app): A full-featured download manager.

---

**References:**

- [dotfiles](https://dotfiles.github.io/)
- [My Setup](https://mysetup.co/)
- [My 2021 New Mac Setup
](https://www.swyx.io/new-mac-setup-2021)
- [Mac Setup for Web Development [2022]
](https://www.robinwieruch.de/mac-setup-web-development/)
