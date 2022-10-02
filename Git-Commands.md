# Git Commands

## Git Repository 

### How to Clone a Repository to your machine
```
git clone [URL]

example:
git clone https://github.com/exampleuser/python.git  - Will Clone the Repository link to your computer
```
### How to show Repository status
```
git status
```
---
## Git Add
### Stage selected files 
```
git add
```
### Stage all files 
```  
git add --all
```
### Stage all files from folder
```
git add .
``` 
---
## Git branch
## How to create and delete branchs
### Create new branch 
```
git branch [NEWBRANCHNAME]
```
### Create new branch and change to new branch 
```
git checkout -b [NEWBRANCHNAME]
```
### Delete branch
```
git branch -d [BRANCHNAME]
```
### Close and delete branch 
```
git push --delete origin [BRANCHNAME]
```
---
## Git commit and push
### Commit changes with a message 
```
git commit -m "COMMIT MESSAGE"  
``` 
 ### Push changes to GitHub 
 ```
git push
```