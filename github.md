# GitHub notes
### Basics

```bash
git init ### initializes repo 
git add .
git commit -m "first commit"
git remote add origin https://github.com/kanstancin/notes.git
git push 
```

### undo commit

```bash
git commit -m "Something terribly misguided" # (0: Your Accident)
git reset HEAD~                              # (1)
git add .                                    # (2)
git commit -c ORIG_HEAD                      # (3)
```

### remove folder after .gitignore
```bash
git rm -r --cached myFolder
```

### large files
```bash
git lfs install ### inside repo
git lfs track "*.weights"
git add .gitattributes
```

### add all plus commit
```bash
git commit -a "commit"
```

### delete branch
```bash
git branch -d iss53 
```

### branches, merging

```bash
# https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
git branch iss53 # create new branch
git checkout iss53 # switch to a branch, or in other words,
# switch HEAD pointer to a branch

# to merge:
#   1. switch to lagging branch
#   2. 
git merge iss53
# (optional)
git branch -d br_name

# there are two types of merging:
# Fast-forward:  if branches point to commits along one 
# history line. This only makes branch pointer to point 
# to the commit of iss53
# Recursive strategy: if branches point to commits in parallel
# history lines, with one ancestor. This merges the code if there are no 
# conflicts, i.e same piece of code changed in both commits. 
# In addition, it creates a new commit with two merged commits
```

### add credentials
```bash
# after pushing or pulling for the first time, it will
# ask for credentials and store it
git config --global credential.helper store
```