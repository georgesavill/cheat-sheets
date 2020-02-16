# Git cheat sheet
## Rename previous commit messages

```
git rebase -i HEAD~n
```
Where n is number of commits into the past to return. Then:

 - Change "pick" to "reword" for each commit message to be changed

 - Save and exit

 - Change commit messages in file that opens

 - Save and exit

 - Repeat until all commits have been reworded

 ```
 git push --force
 ```