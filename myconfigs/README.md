
### Install

#### Mac
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

brew install git zsh jandedobbeleer/oh-my-posh/oh-my-posh
```

#### Linux
```
apt install curl git
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

curl -s https://ohmyposh.dev/install.sh | bash -s
```


### Add kubectl completion and oh-my-posh to ~/.zshrc:
```
source <(kubectl completion zsh)

eval "$(oh-my-posh init zsh)"
```

Re-init oh-my-zsh: ```source ~/.zshrc```

### On host running terminal emulator

#### Install fonts
```oh-my-posh font install```

#### Add Symbols Nerd Font Mono to VSCode
In Editor: Font Family
Menlo, Monaco, 'Courier New', monospace, 'Symbols Nerd Font Mono'
