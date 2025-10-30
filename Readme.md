# Adaptions to Git Extras 

Forked from: https://github.com/tj/git-extras/

Instead of contributing my way of thinking i will 

1. adapt the code to fix problems that i have
2. see how it works for me.

# installation

```bash
re-install.sh
```

# Updating to a new version

```bash
git fetch origin
git  tag  --sort=v:refname | tail

NEW_TAG=7.4.0  # <-- update this to the latest tag 

git co tomsit-master
git branch origin-$NEW_TAG $NEW_TAG 
git rebase $NEW_TAG
# resolve conflicts

#update the PR https://github.com/elonderin/git-extras/pull/3 base to the new origin-$NEW_TAG 
 
re-install.sh
```
