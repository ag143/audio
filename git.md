## Git Basic commands

### Table of contents ###

* [git config](#git_config)
* [git init](#git_init)
* [git clone](#git_clone)
* [git add](#git_add)
* [git commit](#git_commit)
* [git diff](#git_diff)
* [git reset](#git_reset)
* [git status](#git_status)
* [git rm](#git_rm)
* [git log](#git_log)
* [git show](#git_show)
* [git tag](#git_tag)
* [git branch](#git_branch)
* [git checkout](#git_checkout)
* [git merge](#git_merge)
* [git remote](#git_remote)
* [git push](#git_push)
* [git pull](#git_pull)
* [git stash](#git_stash)







## Git Commands ###
### git_config 
Usage: git config –global user.name “[name]”  

Usage: git config –global user.email “[email address]”  

This command sets the author name and email address respectively to be used with your commits.


<details>
	<summary>  git config Example</summary>
    <pre>  git config user.name  -->get current user.name
      username
    > git config user.email --> get current user.email
      emailid
</pre>
</details>


### git_init
Usage: git init [repository name]

<details>
  <summary>Example</summary>
    >git init
     Initialized empty Git repository in C:/Users/<username>/git/test/.git/
    
</details>

This command is used to start a new repository.

GitInit Command - Git Commands - Edureka

### git_clone
Usage: git clone [url]  

This command is used to obtain a repository from an existing URL.
<details>
  <summary>Example</summary>
    <pre>>git clone https://github.com/<username>/handyguide.git
      Cloning into 'handyguide'...
      remote: Enumerating objects: 14, done.
      remote: Counting objects: 100% (14/14), done.
      remote: Compressing objects: 100% (9/9), done.
      remote: Total 14 (delta 1), reused 0 (delta 0), pack-reused 0
      Receiving objects: 100% (14/14), 4.74 KiB | 1.58 MiB/s, done.
      Resolving deltas: 100% (1/1), done.
    </pre>
</details>


### git_add
Usage: git add [file]  

This command adds a file to the staging area.
<details>
  <summary>Example</summary>
    <pre>>git add read.md
	or 
	git add .     -->to track all the changes in staging to commit
    </pre>
</details>


Usage: git add *  

This command adds one or more to the staging area.



### git_commit
Usage: git commit -m “[ Type in the commit message]”  

This command records or snapshots the file permanently in the version history.

<details>
  <summary>Example</summary>
    <pre>>git commit -m "update"
[main efe0d35] update
 1 file changed, 2 insertions(+), 2 deletions(-)
    </pre>
</details>

Usage: git commit -a  

This command commits any files you’ve added with the git add command and also commits any files you’ve changed since then.

<details>
  <summary>Example</summary>
    <pre>>git commit -a   --> opens vi editor

	checking git commit -a
	# Please enter the commit message for your changes. Lines starting
	# with '#' will be ignored, and an empty message aborts the commit.
	#
	# On branch main
	# Your branch is up to date with 'origin/main'.
	#
	# Changes to be committed:
	#       modified:   git.md
	#
    </pre>
</details>

### git_diff
Usage: git diff  

This command shows the file differences which are not yet staged.



 Usage: git diff –staged 

This command shows the differences between the files in the staging area and the latest version present.

 

Usage: git diff [first branch] [second branch]  

This command shows the differences between the two branches mentioned.

 

### git_reset
Usage: git reset [file]  

This command unstages the file, but it preserves the file contents.

 

Usage: git reset [commit]  

This command undoes all the commits after the specified commit and preserves the changes locally.

 

Usage: git reset –hard [commit]  This command discards all history and goes back to the specified commit.

 

### git_status
Usage: git status  

This command lists all the files that have to be committed.
<details>
  <summary>Example</summary>
    <pre>> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   git.md
 </pre>
</details>

### git_rm
Usage: git rm [file]  

This command deletes the file from your working directory and stages the deletion.

 

### git_log
Usage: git log  

This command is used to list the version history for the current branch.

 

Usage: git log –follow[file]  

This command lists version history for a file, including the renaming of files also.
<details>
  <summary>Example</summary>
    <pre>>git log
commit 018c16c20180a9806506c514a9f82451518cd5fd (HEAD -> main, origin/main, origin/HEAD)
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:55:34 2022 +0530

    update

commit 8fac390f7bd49f05b8c377537470679c4d0b048d
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:14:20 2022 +0530

    update

commit e976f22dd8e4d86103846ce9970c097b4a375f5c
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:10:19 2022 +0530

    checking git commit -a

commit efe0d35a7b66e06c8b0cdd3b6dd4a8da8f98cf23
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:05:46 2022 +0530

    update

commit 7211410484884b4014a6a44e07bdb2079537704b
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:04:47 2022 +0530

    Update git.md
:
 </pre>
</details>
 

### git_show
Usage: git show [commit]  

This command shows the metadata and content changes of the specified commit.

<details>
  <summary>Example</summary>
    <pre>git show 018c16c20180a9806506c514a9f82451518cd5fd
commit 018c16c20180a9806506c514a9f82451518cd5fd (HEAD -> main, origin/main, origin/HEAD)
Author: ag143 <ag14341@gmail.com>
Date:   Thu Feb 3 17:55:34 2022 +0530

    update

diff --git a/git.md b/git.md
index cae3382..c269b35 100644
--- a/git.md
+++ b/git.md
@@ -172,8 +172,17 @@ Usage: git reset –hard [commit]  This command discards all history and goes ba
 Usage: git status

 This command lists all the files that have to be committed.
-
-
+<details>
+  <summary>Example</summary>
+    <pre>> git status
+On branch main
+Your branch is up to date with 'origin/main'.
+
+Changes to be committed:
+  (use "git restore --staged <file>..." to unstage)
+        modified:   git.md
+ </pre>
+</details>

 ### git rm
 </pre>
</details>

### git tag
Usage: git tag [commitID]  

This command is used to give tags to the specified commit.

 

### git_branch
Usage: git branch  

This command lists all the local branches in the current repository.

 
Usage: git branch [branch name]  

This command creates a new branch.

 

Usage: git branch -d [branch name]  

This command deletes the feature branch.

 

### git_checkout
Usage: git checkout [branch name]  

This command is used to switch from one branch to another.

 

Usage: git checkout -b [branch name]  

This command creates a new branch and also switches to it.

 

### git_merge
Usage: git merge [branch name]  

This command merges the specified branch’s history into the current branch.
- In case of issues you can use "git merge --abort"

- in case of issues use "git mergetool" to resolve the issues. Git mergetool opens a gui based on default git tool for me its vimdiff
- https://stackoverflow.com/questions/161813/how-to-resolve-merge-conflicts-in-a-git-repository
 

### git remote
Usage: git remote add [variable name] [Remote Server Link]  

This command is used to connect your local repository to the remote server.

 

### git_push
Usage: git push [variable name] master  

This command sends the committed changes of master branch to your remote repository.

 

Usage: git push [variable name] [branch]  

This command sends the branch commits to your remote repository.

<details>
  <summary>Example</summary>
    <pre>>git push
info: please complete authentication in your browser...
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 311 bytes | 155.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ag143/handyguide.git
   7211410..efe0d35  main -> main
    </pre>
</details>

Usage: git push –all [variable name]  

This command pushes all branches to your remote repository.

 

Usage: git push [variable name] :[branch name]  

This command deletes a branch on your remote repository.

 

### git_pull
Usage: git pull [Repository Link]   

This command fetches and merges changes on the remote server to your working directory.

<details>
  <summary>Example</summary>
    <pre>C:\knowledge\github\handyguide>git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 693 bytes | 26.00 KiB/s, done.
From https://github.com/ag143/handyguide
   715c090..213fc18  main       -> origin/main
Updating 715c090..213fc18
Fast-forward
 git.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
    </pre>
</details>

 

### git_stash
Usage: git stash save  

This command temporarily stores all the modified tracked files. 

<details>
  <summary>Example</summary>
    <pre> c:\knowledge\github\handyguide>git stash
Saved working directory and index state WIP on main: 82921c1 Update git.md 
    </pre>
</details>


Usage:: git stash pop  

This command restores the most recently stashed files.

<details>
  <summary>Example</summary>
    <pre> git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (401dffc034390cb993c9cff522d9233fb6e13871)
</pre>
  
</details>

Usage: git stash list  

This command lists all stashed changesets.


<details>
  <summary>Example</summary>
    <pre> C:\knowledge\github\handyguide>git stash list
stash@{0}: WIP on main: 82921c1 Update git.md
    </pre>
</details>



Usage: git stash drop  

<details>
  <summary>Example</summary>
    <pre>C:\knowledge\github\handyguide>git stash drop
Dropped refs/stash@{0} (06075102772c10324118372540d2a28f58ad865b)
    </pre>
</details>
This command discards the most recently stashed changeset.



 
#### refernce links ###
https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html
https://dzone.com/articles/top-20-git-commands-with-examples
