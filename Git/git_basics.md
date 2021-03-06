# Git Basics


### Adding Remote

```
git init

git remote add origin LINK

git pull origin master ()

git add -A

git commit -m "MESSAGE"

git push -u origin master


```


# Renaming Branches

```
# rename current branch
git branch -m NEWNAME
# rename specific branch
git branch -m OLD_NAME NEW_NAME 

```

# Removing Remote
```
git remote rm origin
```

### Show last commit detailed
```
git show
```

### Git Terminal
```
git mv ...
git remove
```

### Adding Files

* **All files**
```
git add -A
```

* **Just updated files**  (tracked: renamed, moved, deleted)
```
git add -u
```

### Delete Branch
* **Delete just label locally**
```
git -d branchname 

```
* **Delete branch in the local repo and remote**
```
git branch -d name (just deletes on the locacl repository)
git push origin :name
```
or
```
git branch -d name (just deletes on the locacl repository)
git push <remote_name> --delete <branch_name>
```

## Show Tracked Files
```
git ls-files
```

## Set the current branch's pointer
(consequently create a new history from a this point)
```
git checkout filename
```


### Marks:
```
git tag tagname
git tag --list (show list with tags)
git tag -d tagname (-d for delete)
git tag -a tagname -m "Message" (obs: v. 1.0)
```


### Notes
* **origin** = default name for remote repository
* **pull** = fetch + merge (remote)
* **HEAD** = last commit on the current branch 

### By conflict
* cat file_conflicted (see diferences)
* git mergetool

