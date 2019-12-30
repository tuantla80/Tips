### 1. Git  
> git config --list  
#### 1.1 Creating a repository  
> $ mkdir test  
> $ cd test  
> $ git init  
  (Initialized empty Git repository in /tmp/test/.git/ )  
> $ ls -a  
> $ git status  
#### 1.2. Clone a repo  
> $git clone git@github.com:user/test  
#### 1.3 Changing a file  
> $ echo "print('make a simple file')" >> test1.py  
> $ git status  
> $ git add test1.py  
  (adding a file)  
> $ git commit -m "adding a test1.py"  
> $ git log  
#### 1.4 Viewing changes  
> $ git diff   
  (Changes between working directory and what was last staged)  
> $ git diff --staged  
  (Changes between staging area and last commit)  
- Note: HEAD (the current version (most recent commit))  
- HEAD~1 (version before current)  
- HEAD~2 (Version before that)  
> $ git diff HEAD~1
  (Changes made in the last commit)  
> $ git diff HEAD~2
  (Changes made in the last 2 commits)  
> $ git diff 0c0d57e  
  (Changes made since commit hash)  
#### 1.5 Recover the last version  
> $ echo "print('make a new simple file with same name')" > test1.py  
> $ cat test1.py  
> $ git checkout HEAD test1.py  
> $ cat test1.py  
#### 1.6 Resetting  
> $ git reset --hard HEAD~1  
#### 1.7 Branches  
> $ git checkout -b "new_branch"  
  (switched to a new branch 'new_branch' and may do some changes, such as add, commit,...)  
> $ git checkout -b master  
  (switched to branch 'master')  
#### 1.8 Merge  
#### 1.9. Tips  
- Use .gitignore  

### 2. Guthub  
> Refer: https://guides.github.com/  

  




