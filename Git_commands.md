# history of cimmits
```
git log
```

# Change last unpushed commit 
```
git commit --amend -m "New commit message."
```

# Add new remote 
```
 git remote add <remote_name> <address_of_repo(with .git at the end of it)>
```

# Remove a remote 
```
 git remote rm <remote_name>
```

# Show all remotes 
```
git remote -v
```

# Show all branches 
show local and remote branches
```
git branch -a
```

# Push a branch to another remote 
push branch develop of our repo to the remote_name
```
git push -u <remote_name> develop:develop
```


# Push all branchs to another remote 
push all branchs of our repo to the remote_name
```
git push <remote_name> -all
```


