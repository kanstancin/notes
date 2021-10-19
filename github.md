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