---
title: git switch git restore について
date: "2022-05-26T23:42:03.284Z"
description: "git"
---

いつの間にか git switch , git restore がリリースされておりました。  
隣の席の人が使用しており、気になったので改めて調べました！


まずは、3点のオプションから

## git checkout
```
git checkout [-q] [-f] [-m] [<branch>]
git checkout [-q] [-f] [-m] --detach [<branch>]
git checkout [-q] [-f] [-m] [--detach] <commit>
git checkout [-q] [-f] [-m] [[-b|-B|--orphan] <new_branch>] [<start_point>]
git checkout [-f|--ours|--theirs|-m|--conflict=<style>] [<tree-ish>] [--] <paths>…​
git checkout [<tree-ish>] [--] <pathspec>…​
git checkout (-p|--patch) [<tree-ish>] [--] [<paths>…​]
```

## git switch
```
git switch [<options>] [--no-guess] <branch>
git switch [<options>] --detach [<start-point>]
git switch [<options>] (-c|-C) <new-branch> [<start-point>]
git switch [<options>] --orphan <new-branch>
```
## git restore
```
git restore [<options>] [--source=<tree>] [--staged] [--worktree] <pathspec>…​
git restore (-p|--patch) [<options>] [--source=<tree>] [--staged] [--worktree] [<pathspec>…​]
```



## git checkoutとの比較

### ブランチ作成
```
git checkout -b <new-branch>
git switch -c <new-branch>
```

 ## ブランチ切り替え
```
git checkout <branch>
git switch <branch>
```

### ファイル変更取り消し
```
git checkout --  <pathspec>…​
git restore  <pathspec>…​
```

ざっくり調べてみました！  
ブランチ作成は今まで通り、checkoutで使ってしまいそうです。