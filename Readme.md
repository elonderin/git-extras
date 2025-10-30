# Adaptions to Git Extras 

Forked from: https://github.com/tj/git-extras/

Instead of contributing my way of thinking i will first adapt some the code to fix problems as i want to see how it works for me.

# installation

```bash
re-install.sh
```

# Updating to a new version


```bash
PREV_TAG=6.4.0
NEW_TAG=7.4.0

git fetch origin
git branch origin-$NEW_TAG $NEW_TAG 
git co -b tomsit-$NEW_TAG $NEW_TAG
git cp $PREV_TAG..tomsit-$PREV_TAG

# OR with rebase
git co tomsit-master
git rebase $NEW_TAG
# resolve conflicts

#update the PR 
re-install.sh
```
