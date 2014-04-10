git notes
====
---


✍ clone from subversion
---

```git svn clone https://path.to/svn --username=livio.bieri@students.fhnw.ch -s```

where `-s` is equal to `-T trunk -b branches -t tags`.

The -s is only necessary if the svn repository follows the standard layout <br>
(i.e., trunk, branches, and tags directories). If not you can omit the -s.


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
✍ prove that you're not lazy...
---
There is someone claiming that you're a lazy guy doing nothing (yaa, I'm looking at you :older_man:) and you want to prove otherwise? Than it would be handy to have something like the following output:
```
files changed:  26 lines inserted:  256 lines deleted:  120
```
Luckily we can do that with:
```
git log --shortstat --author="livio@livio.li" --since="Last month" -p src/ | grep -E "fil(e|es) changed" | awk '{files+=$1; inserted+=$4; deleted+=$6} END {print "files changed: ", files, "lines inserted: ", inserted, "lines deleted: ", deleted }'
```
