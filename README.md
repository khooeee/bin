# bin

Personal helper scripts. Put this directory on your `PATH`.

## Install

```bash
git clone git@github.com:khooeee/bin.git ~/bin
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc   # or ~/.zshrc
source ~/.bashrc
```

Requires: `git`. Optional: `gh` (`cpr`); a clipboard tool such as `pbcopy` / `xclip` / `wl-copy` (`last-commit`, `last-sha`).

## Commands

| command | what it does |
|---|---|
| `cpr` | branch from message → add all → commit → force-push → create PR (`gh`) → open diff |
| `gac` | add all + commit |
| `gacp` | add all + commit + push `-u` |
| `gcom` | checkout default branch (`origin/HEAD`) |
| `gdco` | checkout given branch, then delete previous branch |
| `gdcom` | stash if needed → checkout default → delete previous → pull → stash pop |
| `gmv` | `git mv` |
| `gplom` | stash if needed → pull default branch → stash pop |
| `gpoh` | force-push current branch to `origin` (`-fu`) |
| `gq` | add all + amend keeping last message |
| `gqp` | `gq` + force-push |
| `grhh` | hard reset + clean untracked from repo root |
| `grhu` | fetch + hard reset to upstream + clean |
| `last-commit` | copy last commit subject + URL to clipboard |
| `last-sha` | copy last commit SHA to clipboard |

## Notes

Destructive / force: `grhh`, `grhu`, `gqp`, `gpoh`, `cpr` (force-push).

If you use oh-my-zsh git aliases, these names can clash or mean something different:

| bin | note |
|---|---|
| `gacp` | not the same as common zsh `gap` / related add-patch flow |
| `grhu` | fetch + hard reset upstream + clean (destructive) |
