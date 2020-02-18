# Git cheat sheet
## Create a new repository locally, and push to github

Navigate to directory containing the repository to-be.

```
git init
```
```
git add .
```
```
git commit -m "Initial commit"
```

Go to github, create a new repository, and initialise it without a README. Then:

```
git remote add origin git@github.com:georgesavill/[REPO_NAME].git
```
```
git push -u origin master
```
---

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