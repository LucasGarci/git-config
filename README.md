# My .gitconfig

* Large File Support
* Use `git pr` to create a Pull Request directly on github
* Autotrack branches so `git push` and `git pull` work with the matching remote branch out-of-the-box
* Colors
* Works well with zsh
* Aliases:
  * ci = commit
  * co = checkout
  * st = status
  * br = branch
  * lg = log # with colors
  * pl = pull --rebase
  * undo = reset --soft HEAD^ 
  * `undo --hard will stash dirty directory after a soft undo
  * sm = submodule
  r = pull-request --target-branch master
* No fast forward on merges by default (always create a merge commit, normally I decide wether or not get rid of it manually)


```
[user]
  name = jsdario
  email = jesus@netbeast.co
[core]
  editor = nano
  excludesfile = /Users/jdario/.gitignore_global
[filter "lfs"]
  process = git-lfs filter-process
  required = true
  clean = git-lfs clean -- %f
  smudge = git-lfs smudge -- %f
[push]
  default = current
[alias]
    ci = commit
    co = checkout
    st = status
    br = branch
    lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)%Creset' --abbrev-commit
    graph = log --graph --all '--pretty=format:%Cred%h%Creset %ad | [%C(bold blue)%an%Creset] %Cgreen%d%Creset %s' --date=iso
  rem = remote 
  pl = pull --rebase
  next = add -A && git rebase --continue
  sm = submodule
  pr = pull-request --target-branch master
  undo = reset --soft HEAD^
[merge]
        ff = false
[pull]
  default = current
```