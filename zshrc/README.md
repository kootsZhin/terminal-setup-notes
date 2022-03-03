# .zshrc

Setting up highlighting, prompt format and extensions.

## Extensions

[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions):

```zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/plugins/zsh-autosuggestions
```

[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting):

```zsh
git clone https://github.com/zsh-users/zsh-syntax-highlighting ~/.zsh/plugins/zsh-syntax-highlighting
```

## Code Snippet

```zsh
export CLICOLOR=1
export LSCOLORS=gxBxhxDxfxhxhxhxhxcxcx

source ~/.zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
source ~/.zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
source ~/.bash_profile
autoload -U colors && colors
setopt prompt_subst

PROMPT='[%{$fg[yellow]%}%D{%F} %D{%H:%M:%S}%{$reset_color%}] %n | %1~$(git branch --show-current 2&> /dev/null | xargs -I branch echo " (branch)") %% '
```

## Resources

- For more extensions/resources: [zsh-users](https://github.com/zsh-users)
- For zsh documentation: [ZSH Documentation](https://zsh.sourceforge.io/Doc/)
