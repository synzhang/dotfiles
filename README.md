# My Computer Setup

## System

- [Homebrew](https://brew.sh/): The Missing Package Manager for macOS.

### Shell

- [Zsh](https://www.zsh.org/): Zsh is a shell designed for interactive use.
  - [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh): Oh My Zsh is an open source, community-driven framework for managing your zsh configuration.
  - [Powerlevel10k](https://github.com/romkatv/powerlevel10k): Powerlevel10k is a theme for Zsh. It emphasizes speed, flexibility and out-of-the-box experience.
  - [zsh-z](https://github.com/agkozak/zsh-z): Jump quickly to directories that you have visited "frecently." A native Zsh port of z.sh with added features.
- [Pandoc](https://github.com/jgm/pandoc): A universal document converter.
- [ImageMagick](https://github.com/imagemagick/imagemagick): Used to create, edit, compose, or convert bitmap images, and supports a wide range of file formats.
- [FFmpeg](https://github.com/FFmpeg/FFmpeg): A collection of libraries and tools to process multimedia content such as audio, video, subtitles and related metadata.
- [exa](https://the.exa.website/): A modern replacement for ls.
- [bat](https://github.com/sharkdp/bat): A cat(1) clone with wings.
- [tree](https://formulae.brew.sh/formula/tree): Display directories as trees.
- [fzf](https://github.com/junegunn/fzf): A command-line fuzzy finder.
- [fd](https://github.com/sharkdp/fd): A simple, fast and user-friendly alternative to 'find'.
- [ripgrep](https://github.com/BurntSushi/ripgrep): ripgrep recursively searches directories for a regex pattern while respecting your gitignore.
- [tldr](https://tldr.sh/): Simplified and community-driven man pages.
- [tokei](https://github.com/XAMPPRocky/tokei): Count your code, quickly.

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
  Enable key-repeating:
  ```shell
  $ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false              # For VS Code
  $ defaults write com.microsoft.VSCodeInsiders ApplePressAndHoldEnabled -bool false      # For VS Code Insider
  $ defaults write com.visualstudio.code.oss ApplePressAndHoldEnabled -bool false         # For VS Codium
  $ defaults write com.microsoft.VSCodeExploration ApplePressAndHoldEnabled -bool false   # For VS Codium Exploration users
  # And then re-login
  ```
- [Neovim](https://github.com/neovim/neovim): Vim-fork focused on extensibility and usability.
  - [SpaceVim](https://github.com/SpaceVim/SpaceVim): A community-driven modular vim/neovim distribution - The ultimate vimrc.
- [Git](https://git-scm.com/): Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
  ```shell
  $ git config --global user.email "you@example.com"
  $ git config --global user.name "Your Name"
  $ git config --global core.editor vim
  $ git config --global pull.rebase true
  ```
  - [Tig](http://jonas.github.io/tig/): Text-mode interface for Git.
  - [GitUI](https://github.com/extrawurst/gitui): Blazing fast terminal-ui for git written in Rust.
- [Node.js](https://nodejs.org/en/): Node.js is an open-source, cross-platform JavaScript runtime environment.
  - [n](https://github.com/tj/n): Node version management
  - [npm-check](https://github.com/dylang/npm-check): Check for outdated, incorrect, and unused dependencies.
- [Docker](https://www.docker.com/products/docker-desktop/): The fastest way to containerize applications.
- [Postman](https://www.postman.com/): Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration so you can create better APIs—faster.
- [Sequel Ace](https://apps.apple.com/us/app/sequel-ace/id1518036000): SQL Tool for Experts & Novices.
- [Nerd Fonts](https://www.nerdfonts.com/): Nerd Fonts patches developer targeted fonts with a high number of glyphs (icons). Specifically to add a high number of extra glyphs from popular ‘iconic fonts’ such as Font Awesome, Devicons, Octicons, and others.

## App

- [1Password](https://1password.com/): The world’s most-loved password manager.
- [Chrome](https://www.google.com/chrome/): Google web browser.
- [Firefox](https://www.mozilla.org/en-US/firefox/new/): Get Firefox, a free web browser backed by Mozilla, a non-profit dedicated to internet health and privacy. Available now on Windows, Mac, Linux, Android and iOS.
- [Dropbox](https://www.dropbox.com/): Easy to use, reliable, private, and secure. It’s no wonder Dropbox is the choice for storing and sharing your most important files.
- [Google Drive](https://www.google.com/drive/): Store, share, and collaborate on files and folders from your mobile device, tablet, or computer.
- [Obsidian](https://obsidian.md/): Obsidian is a powerful knowledge base on top of a local folder of plain text Markdown files.
- [Zotero](https://www.zotero.org/): Your personal research assistant. Easy-to-use tool to help you collect, organize, annotate, cite, and share research.
  * [zotfile](https://github.com/jlegewie/zotfile): Advanced PDF management for Zotero.
  * [Mdnotes](https://github.com/argenos/zotero-mdnotes): A Zotero plugin to export item metadata and notes as markdown files.
  * [Better BibTeX for Zotero](https://github.com/retorquere/zotero-better-bibtex): Make Zotero effective for us LaTeX holdouts.
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
- [Actions](https://apps.apple.com/us/app/actions/id1586435171): Useful actions for Shortcuts.
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
- [Scratch](https://apps.apple.com/us/app/scratch/id1446785996): With Scratch, you can program your own interactive stories, games, and animations.
- [Reeder](https://apps.apple.com/cn/app/reeder-4/id1449412482): A RSS Reader.
- [Affinity Photo](https://apps.apple.com/us/app/affinity-photo/id824183456): Professional photo editing.
- [Yoink](https://apps.apple.com/us/app/yoink-improved-drag-and-drop/id457622435): Your Files and Snippet Shelf.
- [Unsplash](https://apps.apple.com/us/app/unsplash-wallpapers/id1284863847): A breathtaking photo for your desktop wallpaper, every day.
- [HandBrake](https://github.com/HandBrake/HandBrake): A tool for converting video from nearly any format to a selection of modern, widely supported codecs.
- [Upscayl](https://github.com/upscayl/upscayl): Free and Open Source AI Image Upscaler.
- [Buzz](https://github.com/chidiwilliams/buzz): Buzz transcribes and translates audio offline on your personal computer. Powered by OpenAI's Whisper.
- [LocalSend](https://github.com/localsend/localsend): LocalSend is a free, open-source app that allows you to securely share files and messages with nearby devices over your local network, without needing an internet connection.

---

**References:**

- [dotfiles](https://dotfiles.github.io/)
- [Takuya's dotfiles](https://github.com/craftzdog/dotfiles-public)
- [My Setup](https://mysetup.co/)
- [My 2021 New Mac Setup](https://www.swyx.io/new-mac-setup-2021)
- [Mac Setup for Web Development [2022]](https://www.robinwieruch.de/mac-setup-web-development/)
- [The Ultimate Guide to Your Terminal Makeover](https://towardsdatascience.com/the-ultimate-guide-to-your-terminal-makeover-e11f9b87ac99)
