# ZSH setup

## Repo

On `~` (home) path clone this repo

```bash
git init 
git remote add origin https://github.com/deinacademy/zsh-setup.git
git pull origin main
```

On `.zshrc` file add.

```bash
# Helpers
export OPEN="explorer.exe"
export PATH="$HOME/.helpers/b64/:$PATH"
export PATH="$HOME/.helpers/git/:$PATH"
export PATH="$HOME/.helpers/md/:$PATH"
export PATH="$HOME/.helpers/open/:$PATH"
chmod +x ~/.helpers/**/*

# Custom
local WINHOME=$(wslpath "$(wslvar USERPROFILE)")

local GIT_USER_NAME="user"
local GIT_USER_EMAIL="user@mail.com"
local GITHUB_USER_NAME="user"
local GITHUB_USER_EMAIL="user@users.noreply.github.com"
[ -f ~/.aliases ] && . ~/.aliases
[ -f ~/.colors ] && . ~/.colors
[ -f ~/.hooks ] && . ~/.hooks
```

Add execution permission:

```bash
chmod +x ~/.helpers/**/*
```

Once finish, reopen all terminals or update his source running `source ~/.zshrc` command and now you can use it.

## Folder Structure

```bash
~
├── .cheatsheet
│   └── git.md
│   └── open.md
├── .helpers
│   ├── b64
│   ├── git
│   ├── md
│   ├── open
│   └── react
├── .aliases
├── .colors
├── .hooks
└── .zshrc
```

## Article Series

- [Reveal the command behind an alias with ZSH](https://dev.to/equiman/reveal-the-command-behind-an-alias-with-zsh-4d96)
- [Useful Alias for ZSH](https://dev.to/equiman/useful-alias-for-zsh-1j8b)
- [Automatic change directory after git clone](https://dev.to/equiman/automatic-change-directory-after-git-clone-8ei)
- [Command validations with ZSH](https://dev.to/equiman/command-validations-with-zsh-2boa)
- [Open File Explorer and Browser from ZSH](https://dev.to/equiman/open-file-explorer-and-browser-mbb)
- [ZSH cheatsheet for git plugin](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a)
- [base64 encode/decode multiple files](https://dev.to/equiman/base64-encode-decode-multiple-files-2ol1)
