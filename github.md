### Work routine:

* only read https://github.com/notifications/participating that someone mentions you.
* when you have more time or get bore: https://github.com/notifications 
* if you even have time, check new issues https://github.com/issues that are interesting to follow

### Shortcuts

* https://github.com/issues/assigned.
* https://github.com/issues/pulls

### More tips 

* Refine Github experience https://github.com/sindresorhus/refined-github
* If you want to know what your colleagues are doing on GH: https://devspace.io/

### Commands

* Reset changes
``` 
git reset --hard
```

* New branch locally
```
git branch xx
git checkout typexx
```

* Fetch new branch from remote
```
git fetch origin xx
git checkout xx
```

* List branch locally
```
git branch --list
```

* List branch remote
```
git branch -r
```
* List branch both local and remote
```
git branch -a
```
* Delete xx on local
```
git branch xx -D
```
* Delete xx on remote. Here origin is my remote
```
git push origin :xx
```
* Pull xx from remote
```
git pull origin xx
```
* Merge xx from remote
```
git merge origin xx
git merge origin xx --no-ff
```
* Squash all commit from a feature branch, which diverges from this branch
```
git merge origin xx --squash
```
* Rename old branche
```
#Rename branch locally 
git branch -m old_branch new_branch         
#Delete the old branch 
git push origin :old_branch                     
#Push the new branch, set local branch to track the new remote
git push --set-upstream origin new_branch   
```
* showing parents of a merge commit
```
git show --pretty=raw <commit hash>
```
