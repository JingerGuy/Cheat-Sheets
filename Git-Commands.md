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
Display Local Repository status
```

## Git Add
### How to add files to staging
```
git add
Stage selected files 

git add --all
Stage all files  

git add .
Stage all files from folder
``` 

## Git branch
### How to create and delete branchs
```
git branch [NEWBRANCHNAME]
Create new branch 

git checkout -b [NEWBRANCHNAME]
Create new branch and change to new branch 

git branch -d [BRANCHNAME]
Delete branch 

git push --delete origin [BRANCHNAME]
Close and delete branch 
```
# Git commit and push
```
git commit -m "COMMIT MESSAGE"  
Commit changes with a message entered in the ""
 
git push
Push changes to GitHub 
```