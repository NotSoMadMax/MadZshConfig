# MadZshConfig
My zsh configurations

## Install [oh-my-zsh](https://ohmyz.sh)
```
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install [powerlevel10k](https://github.com/romkatv/powerlevel10k)
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```
Set ``ZSH_THEME="powerlevel10k/powerlevel10k"`` in ``~/.zshrc``.

## Git
* Git Ignore

```
# Compiled Files
*.class
*.o

# Packages
*.7z
*.jar
*.rar
*.zip
*.gz
*.bzip
*.bz2
*.xz
*.lzma
*.cab
*.iso
*.tar
*.dmg

# IDE
.idea/*

# Mac
.DS_Store
.DS_Store?
```

## zsh
* ``~/.profile``

```
# Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$HOME/.rvm/bin:$PATH"

# Set Python2.7 path
export PATH="/Library/Frameworks/Python.framework/Versions/2.7/bin:${PATH}"

# Set sqlite
export PATH="/usr/local/opt/sqlite/bin:$PATH"

# Load RVM into a shell session *as a function*
[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"

# Alias
alias gs="git status "
alias gb="git branch "
alias gch="git checkout "
alias ga="git add "
alias gcm="git commit "
```
* ``~/.zshrc``

```
source ~/.profile

export PATH=$HOME/bin:/usr/local/bin:$PATH
```
