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
.
> $ git diff HEAD1  
  (Changes made in the last commit)  
> git diff HEAD~2  
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
#### 1.9 Archive  
> $ git archive master -o test.zip
#### 1.10. Tips  
- Use .gitignore  

### 2. Guthub  
> Refer: https://guides.github.com/
### 3. Git command examples
I. Clone a project from Github or Bitbucket to work with

  - Step 1: Go to a directory and make git clone
    C:\Python>git clone https://tuantla80@bitbucket.org/tuantla80/test_db.git
        Cloning into 'test_db'...
        remote: Counting objects: 4, done.
        remote: Compressing objects: 100% (4/4), done.
        remote: Total 4 (delta 0), reused 0 (delta 0)
        Unpacking objects: 100% (4/4), 970 bytes | 74.00 KiB/s, done.
    
  - Step 2: go to the test_db directory (getting from Step 1)
    C:\Python>cd test_db

    C:\Python\test_db>git status
        On branch master
        Your branch is up to date with 'origin/master'.
        nothing to commit, working tree clean
    
   - Step 3: Adding folder, files to test_db and then git status
   - Step 4: git add, git status, git commit, git push origin master as usual
      C:\Python\test_db>git add . 
      C:\Python\test_db>git commit -m "ml model: Done"
      C:\Python\test_db>git push origin master

#---------------------------------------------------------------------------------------------
II. Git commands
user1@user MINGW64 ~
$ git config --global user.name "Tuan"

user1@user MINGW64 ~
$ git config user.name
Tuan

user1@user MINGW64 ~
$ git config --global user.email "tuantla80@gmail.com"

user1@user MINGW64 ~
$ git config user.email
tuantla80@gmail.com

user1@user MINGW64 ~
$ pwd
/c/Users/user1

user1@user MINGW64 ~
$ mkdir Test

user1@user MINGW64 ~
$ cd Test

user1@user MINGW64 ~/Test
$ touch index.html

user1@user MINGW64 ~/Test
$ ls
index.html

user1@user MINGW64 ~/Test
$ notepad index.html

user1@user MINGW64 ~/Test
$ notepad++ index.html
bash: notepad++: command not found

user1@user MINGW64 ~/Test
$ Notepad++ index.html
bash: Notepad++: command not found

user1@user MINGW64 ~/Test
$ notepad index.html

user1@user MINGW64 ~/Test
$ notepad index.html

user1@user MINGW64 ~/Test
$ rm index.html

user1@user MINGW64 ~/Test
$ ls

user1@user MINGW64 ~/Test
$ cd ..

user1@user MINGW64 ~
$ pwd
/c/Users/user1

user1@user MINGW64 ~
$ rmdir Test

user1@user MINGW64 ~
$ cd Test
bash: cd: Test: No such file or directory

user1@user MINGW64 ~
$ mkdir repos

user1@user MINGW64 ~
$ cd repos

user1@user MINGW64 ~/repos
$ pwd
/c/Users/user1/repos

user1@user MINGW64 ~/repos
$ mkdir MyGitRepo

user1@user MINGW64 ~/repos
$ cd MyGitRepo/

user1@user MINGW64 ~/repos/MyGitRepo
$ pwd
/c/Users/user1/repos/MyGitRepo

user1@user MINGW64 ~/repos/MyGitRepo
$ git init
Initialized empty Git repository in C:/Users/user1/repos/MyGitRepo/.git/

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ ls

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ ls -a
./  ../  .git/

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ touch index.html

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ touch styles.css

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ ls
index.html  styles.css

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        styles.css

nothing added to commit but untracked files present (use "git add" to track)

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git add index.html

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        styles.css


user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git rm --cached index.html
rm 'index.html'

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        styles.css

nothing added to commit but untracked files present (use "git add" to track)

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git add .

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html
        new file:   styles.css


user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git commit -m "Add skeleton files for webpage."
[master (root-commit) 1eb61de] Add skeleton files for webpage.
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
 create mode 100644 styles.css

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git log
commit 1eb61dea320ee265a6c5c740414a39ff057b9fba (HEAD -> master)
Author: Tuan <tuantla80@gmail.com>
Date:   Sun Dec 20 16:45:56 2020 +1100

    Add skeleton files for webpage.

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git branch
* master

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git branch user-authentication

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git branch
* master
  user-authentication

user1@user MINGW64 ~/repos/MyGitRepo (master)
$  git che
checkout      cherry        cherry-pick

user1@user MINGW64 ~/repos/MyGitRepo (master)
$  git checkout user-authentication
Switched to branch 'user-authentication'

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git branch
  master
* user-authentication

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ touch auth.js

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ ls
auth.js  index.html  styles.css

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ notepad index.html


user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git diff index.html
diff --git a/index.html b/index.html
index e69de29..75446e8 100644
--- a/index.html
+++ b/index.html
@@ -0,0 +1 @@
@@ -0,0 +1 @@
+<!-- This is a comment -->
\ No newline at end of file

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ touch MyApp.log

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        MyApp.log
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ touch Device.log

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Device.log
        MyApp.log
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ touch .gitignore

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        Device.log
        MyApp.log
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ notepad .gitignore

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git add .gitignore

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        auth.js


user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git commit -m "Add .gitignore"
[user-authentication cfb4945] Add .gitignore
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        auth.js

no changes added to commit (use "git add" and/or "git commit -a")

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git add .

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   auth.js
        modified:   index.html


user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git commit -m "Complete user authentication"
[user-authentication fa23ea3] Complete user authentication
 2 files changed, 1 insertion(+)
 create mode 100644 auth.js

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git status
On branch user-authentication
nothing to commit, working tree clean

user1@user MINGW64 ~/repos/MyGitRepo (user-authentication)
$ git checkout master
Switched to branch 'master'

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Device.log
        MyApp.log

nothing added to commit but untracked files present (use "git add" to track)

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git merge user-authentication
Updating 1eb61de..fa23ea3
Fast-forward
 .gitignore | 2 ++
 auth.js    | 0
 index.html | 1 +
 3 files changed, 3 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 auth.js

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git status
On branch master
nothing to commit, working tree clean

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git log
commit fa23ea3ecef9710d67683c57575465daf31a75be (HEAD -> master, user-authentication)
Author: Tuan <tuantla80@gmail.com>
Date:   Sun Dec 20 17:42:26 2020 +1100

    Complete user authentication

commit cfb49454ff6bb6657b36ab9fcac6ca12921a8dfa
Author: Tuan <tuantla80@gmail.com>
Date:   Sun Dec 20 17:39:44 2020 +1100

    Add .gitignore

commit 1eb61dea320ee265a6c5c740414a39ff057b9fba
Author: Tuan <tuantla80@gmail.com>
Date:   Sun Dec 20 16:45:56 2020 +1100

    Add skeleton files for webpage.

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git tag -a v1.0.0 -m "Version 1.0.0 release"

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ get tag
bash: get: command not found

user1@user MINGW64 ~/repos/MyGitRepo (master)
$ git tag
v1.0.0

user1@user MINGW64 ~
$ pwd
/c/Users/user1

user1@user MINGW64 ~
$ cd repos

user1@user MINGW64 ~/repos
$ ls
MyGitRepo/

user1@user MINGW64 ~/repos
$ pwd
/c/Users/user1/repos

user1@user MINGW64 ~/repos
$ epos/
bash: epos/: No such file or directory

user1@user MINGW64 ~/repos
$ git clone https://tuantla@bitbucket.org/tuantla/hellobitbucket.git
Cloning into 'hellobitbucket'...
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), 585 bytes | 5.00 KiB/s, done.

user1@user MINGW64 ~/repos
$ ls
MyGitRepo/  hellobitbucket/

user1@user MINGW64 ~/repos
$ cd hellobitbucket/

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ ls -a
./  ../  .git/  .gitignore

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ touch HelloWorld.txt

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ notepad HelloBitbucket.txt

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        HelloBitbucket.txt
        HelloWorld.txt

nothing added to commit but untracked files present (use "git add" to track)

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git add .

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   HelloBitbucket.txt
        new file:   HelloWorld.txt


user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git commit -m "Create hello text files"
[master fc31dfd] Create hello text files
 2 files changed, 1 insertion(+)
 create mode 100644 HelloBitbucket.txt
 create mode 100644 HelloWorld.txt

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git branch
* master

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git push origin master


user1@user MINGW64 ~/repos/hellobitbucket (master)
$
fatal: helper error (-1073741510): Unknown

user1@user MINGW64 ~/repos/hellobitbucket (master)
$

user1@user MINGW64 ~/repos/hellobitbucket (master)
$

user1@user MINGW64 ~/repos/hellobitbucket (master)
$

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git commit -m "Create hello text files"
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

user1@user MINGW64 ~/repos/hellobitbucket (master)
$


user1@user MINGW64 ~/repos/hellobitbucket (master)
$


user1@user MINGW64 ~/repos/hellobitbucket (master)
$

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git push origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 348 bytes | 58.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://bitbucket.org/tuantla/hellobitbucket.git
   642d409..fc31dfd  master -> master

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git pull
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0)
Unpacking objects: 100% (3/3), 276 bytes | 1024 bytes/s, done.
From https://bitbucket.org/tuantla/hellobitbucket
   fc31dfd..4a5cc51  master     -> origin/master
Updating fc31dfd..4a5cc51
Fast-forward
 README.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git fetch

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ git merge
Already up to date.

user1@user MINGW64 ~/repos/hellobitbucket (master)
$ cd ..

user1@user MINGW64 ~/repos
$ ls
MyGitRepo/  hellobitbucket/

user1@user MINGW64 ~/repos
$ cd ..

user1@user MINGW64 ~
$ pwd
/c/Users/user1

user1@user MINGW64 ~
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/user1/.ssh/id_rsa):
Created directory '/c/Users/user1/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/user1/.ssh/id_rsa
Your public key has been saved in /c/Users/user1/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:LEhaODY25UrfohY6W1Ez8fmQ8l1iqSqOH70zK4+0YJk user1@user
The key's randomart image is:
+---[RSA 3072]----+
|    o            |
|   + o o .       |
|  O O = + .      |
| + @ B B o       |
|  = + = S        |
| .o= o .         |
|+EB o            |
|.X.=o.           |
|o.=o++           |
+----[SHA256]-----+

user1@user MINGW64 ~
$ ls ~/.ssh
id_rsa  id_rsa.pub

user1@user MINGW64 ~
$ pwd
/c/Users/user1

user1@user MINGW64 ~
$ clip < ~/.ssh/id_rsa.pub

user1@user MINGW64 ~
$ ssh -T git@bitbucket.org
The authenticity of host 'bitbucket.org (104.192.141.1)' can't be established.
RSA key fingerprint is SHA256:zzXQOXSRBEiUtuE8AikJYKwbHaxvSc0ojez9YXaGp1A.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'bitbucket.org,104.192.141.1' (RSA) to the list of known hosts.
logged in as tuantla

You can use git or hg to connect to Bitbucket. Shell access is disabled

user1@user MINGW64 ~


  




