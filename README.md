# checkinlist

## Git setup
1.add below in ~/.gitconfig
```  [alias]
          gui = !sh -c /usr/local/git/libexec/git-core/git-gui
  [diff]
          tool = diffmerge
  [difftool "diffmerge"]
          cmd = diffmerge $LOCAL $REMOTE
  [merge]
          tool = diffmerge
  [mergetool "diffmerge"]
          cmd = diffmerge --merge --result=$MERGED $LOCAL $BASE $REMOTE
  [difftool]
          prompt = false
  [mergetool]
          prompt = false
```

2.install git gui

...Launch console, goto git repositroy folder, run below command:
```
git gui
```
...If you see error, do step 3, and run above command again

3.install git with brew

```
brew install git
```

4.install gitk

```
gitk
```
...You should see git history

5.install diffmerge

...When have any uncommitted changes, run
```
git difftool
```
...You should see the diffmerge window showing changed files

