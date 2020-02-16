# Change commit messages

Run:

```
git rebase -i HEAD~n
```
Where n is number of commits into the past to return. Then:

 - Change "pick" to "reword"

 - Save and exit

 - Change commit messages

 - Save and exit

 - Repeat until all commits have been reworded

 ```
 git push --force
 ```