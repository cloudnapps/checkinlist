# checkinlist

## Git setup
### install git gui
### install gitk
### install diffmerge

### add below in ~/.gitconfig
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
