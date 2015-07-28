# checkinlist

## Git setup
1.add below in ~/.gitconfig
```
  [alias]
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

Launch console, goto git repositroy folder, run below command:
```
git gui
```
If you see error, do step 3, and run above command again

3.install git with brew

```
brew install git
```

4.install gitk

```
gitk
```
You should see git history

5.install diffmerge

Add diffmerge file to /usr/bin
```
#!/bin/sh
## A little script to make it easier to launch DiffMerge from the command line.
## Install this script into a folder in your path, such as /usr/bin or /usr/local/bin.
##
## Version 4.2.0.697
## Copyright (C) 2003-2013 SourceGear LLC. All Rights Reserved.
##############################################################################

## Change DIFFMERGE_PATH to point to where you installed DiffMerge

DIFFMERGE_PATH=/Applications/DiffMerge.app

## The actual executable is hidden inside the .app bundle.

DIFFMERGE_EXE=${DIFFMERGE_PATH}/Contents/MacOS/DiffMerge

## Launch DiffMerge using the given command line arguments.  Use --help for
## additional information or see the man page distributed along with this
## shell script.

exec ${DIFFMERGE_EXE} --nosplash "$@"
```

And then when you have any uncommitted changes, run
```
git difftool
```
You should see the diffmerge window showing changed files

