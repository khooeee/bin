# Setup

Add to ~/.bashrc or ~/.zshrc

```sh
export LSCOLORS=ExFxBxDxCxegedabagacad
export PATH="$HOME/.local/bin:$PATH"
alias l='ls -CGF' # C is list by columns, G is colorized output & F appends / for directories, * for executables & @ for symlinks, etc.
alias lg='lazygit'
alias v='vim'
```

Run:

```bash
echo "export PATH=$(pwd):\$PATH" >> "$HOME/.bashrc"
source ~/.bashrc
```

or

```bash
echo "export PATH=$(pwd):\$PATH" >> "$HOME/.zshrc"
source ~/.zshrc
```

**Conflicts**
These still have the same name as oh-my-zsh git aliases, but different meanings:

| new bin | old bin | oh-my-zsh |
|---|---|---|
| `gacp` | `gap` | add all, commit, push upstream |
| `grhu` | `gru` | fetch + hard reset upstream + clean |

**oh-my-zsh equivalents**
Covered by oh-my-zsh under different names:

| git command | old bin | oh-my-zsh equivalent |
|---|---|---|
| cd $(git rev-parse --show-toplevel) | gr | grt |
| git add | gad | ga |
| git branch | gbr | gb |
| git commit | gcm | gc |
| git diff | gdf | gd |
| hard reset + clean | grh | gwipe |
| git merge | gmg | gm |
| git push | gph | gp |
| git pull | gpl | gl |
| git remote | gre | gr |
| git reset | grs | grh |
| git stash list | gsl | gstl |
| git revert | grv | grev |
| git stash drop | gsd | gstd |
| git stash pop | gspop | gstp |
| git stash push | gspush | gstu |
