git- notes
====
---


✍ clone from subversion
---

```git svn clone https://path.to/svn --username=livio.bieri@students.fhnw.ch -s```

where `-s` is equal to `-T trunk -b branches -t tags` which is the commonly used naming.


✍ rebase from subversion ('update')
---

```
git svn rebase
```

When there is the following message saying `` needs update`` : 

```
git svn rebase
path/to path/to/some/file: needs update
```

We need to add the updated files using:

```
git add -u
```

✍ commits changes to subversion
---

```
git svn dcommit
```

✍ number of commits per user
---
```
git shortlog -s -n --all
```

✍ rename a branch
---
```
git branch -m old_branch new_branch
```

✍ add a remote 'mirror'
---
```
git remote add origin git@github.com:livioso/test.git
```

✍ colorize git output
---
```
git config --global color.ui auto
```
