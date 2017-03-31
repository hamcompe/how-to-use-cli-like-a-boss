# How to use CLI like a boss

**CLI Program**: 

- [iTerm2](https://www.iterm2.com/)
- [hyper.js](https://hyper.is/)

**Tools**: 
    
- [homebrew](https://brew.sh/) (Package manager on MacOS)
- [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) (CLI framework)    
- [z.sh](https://github.com/rupa/z) (Go to any directories that you've been to extremely fast)

## CLI
###  Example of my aliases

```
# Open sublime text
alias sub='open -a "Sublime Text"'

# Show/Hide Hidden Files
alias showHidden='defaults write com.apple.finder AppleShowAllFiles YES; killall Finder /System/Library/CoreServices/Finder.app'
alias hideHidden='defaults write com.apple.finder AppleShowAllFiles NO; killall Finder /System/Library/CoreServices/Finder.app'
```

This is how I open my project in sublime

```
$ cd <my-project-path>
$ sub .
```

## Homebrew

### Example of package I uses
- [gitignore](https://github.com/imwithye/gitignore)
- tree

### installation
```
$ brew install <package-name>
```

***Notes**: [My article that talks about, how to use gitignore package.](https://blog.vannizer.com/a-better-way-to-create-gitignore-3b157245c133)*

## Oh-my-zsh

### Advantage for using oh-my-zsh
- [Plugins](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins)
- [Themes](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes)
- Display all aliases list - `$ alias`
- Build in alias - e.g., *git*
- autocomplete
- etc.

### Example command I uses

```
$ alias | grep 'git'
```

### List of plugins I uses

- git
- common-aliases
- vi-mode

### List of git commands I uses

- `gst` : status
- `gaa` : add all to staging
- `gc` : commit
- `glo` : log one line, only current branch
- `gloga` : log one line, all branch, and more decoration
- `gb` : show all branches
- `gco <branch name>` : move between branch
- `gcb <branch name` : create new branch, and move to that branch
- `ggpull` : pull code from current branch
- `ggpush` : push code from current branch
- `grhh` : revert all changed code, back to latest pulled code
- `gbda` : delete all the branches that already has been merged, except **master**, **develop** and **dev**
- `gfa` : update all branches status from remote
- `gwip` : like stash, but save it in the commit
- `gunwip` : like stash pop, but need to pop from `gwip`
- `grbi @~<number of commit which you wanna iteract with>` : rebase commits. I usually for make **two or multiple commits** become **one commit**. (use fixup)
- `git merge --no-ff <branch name>` : merge branch, and create message that say which branch has been merged
- `git push -f` : force to push the commit, use when I squash (rebase) commits

***Notes**: I prefer to use `gwip` and `gunwip` over `git stash`, because you could see your stashed code from the **log***

## git tag
```
$ git tag -a v1.3.2 -m "Tag message"
$ git push --tags
```
