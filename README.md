# Mac Git Hooks
Git global hooks

## Installation
```bash
$ git clone https://github.com/darkjinnee/mac-githooks.git
$ git config --global core.hooksPath ~/mac-githooks
$ chmod -R +x ./mac-githooks
```

### Hide changes
Add lines to file `.gitconfig`
```text
[alias]
    hide   = update-index --skip-worktree
    unhide = update-index --no-skip-worktree
    hidden  = "!git ls-files -v | grep ^[hsS] | cut -c 3-"
```
