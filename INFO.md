piupiu@AK-PC SKILLFACTORY % git branch
* main
piupiu@AK-PC SKILLFACTORY % git branch homework
piupiu@AK-PC SKILLFACTORY % git branch
  homework
* main
piupiu@AK-PC SKILLFACTORY % git checkout homework
Switched to branch 'homework'
piupiu@AK-PC SKILLFACTORY % vim file-feature-1
piupiu@AK-PC SKILLFACTORY % git add file-feature-1
piupiu@AK-PC SKILLFACTORY % git commit -m "new file feature 1"
[homework 85666b3] new file feature 1
 1 file changed, 1 insertion(+)
 create mode 100644 file-feature-1
piupiu@AK-PC SKILLFACTORY % git branch
* homework
  main
piupiu@AK-PC SKILLFACTORY % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
piupiu@AK-PC SKILLFACTORY % ls -la
total 32
drwxr-xr-x@  7 piupiu  staff   224 Mar 30 22:13 .
drwxr-xr-x@  4 piupiu  staff   128 Mar 30 22:13 ..
drwxr-xr-x@ 13 piupiu  staff   416 Mar 30 22:53 .git
-rw-r--r--   1 piupiu  staff  3254 Mar 30 22:10 INFO.md
-rw-r--r--   1 piupiu  staff    36 Mar 30 22:10 README.md
-rw-r--r--   1 piupiu  staff     9 Mar 30 22:15 file-feature-2.txt
-rw-r--r--   1 piupiu  staff    10 Mar 30 22:17 file-feature.txt
piupiu@AK-PC SKILLFACTORY % git chrckout homework
git: 'chrckout' is not a git command. See 'git --help'.

The most similar command is
	checkout
piupiu@AK-PC SKILLFACTORY % git checkout homework
Switched to branch 'homework'
piupiu@AK-PC SKILLFACTORY % git checkout -       
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
piupiu@AK-PC SKILLFACTORY % git checkout -b homework2
Switched to a new branch 'homework2'
piupiu@AK-PC SKILLFACTORY % vim file-feature-2
piupiu@AK-PC SKILLFACTORY % git status
On branch homework2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	file-feature-2

nothing added to commit but untracked files present (use "git add" to track)
piupiu@AK-PC SKILLFACTORY % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
piupiu@AK-PC SKILLFACTORY % git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	file-feature-2

nothing added to commit but untracked files present (use "git add" to track)
piupiu@AK-PC SKILLFACTORY % git checkout -
Switched to branch 'homework2'
piupiu@AK-PC SKILLFACTORY % git stash -u
Saved working directory and index state WIP on homework2: 9d3efd8 Renamed 3 to 0
piupiu@AK-PC SKILLFACTORY % git branch      
  homework
* homework2
  main
piupiu@AK-PC SKILLFACTORY % git push origin homework
Enumerating objects: 24, done.
Counting objects: 100% (24/24), done.
Delta compression using up to 4 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (24/24), 4.14 KiB | 1.04 MiB/s, done.
Total 24 (delta 5), reused 0 (delta 0)
remote: Resolving deltas: 100% (5/5), done.
remote: 
remote: Create a pull request for 'homework' on GitHub by visiting:
remote:      https://github.com/sashiva12/SKILLFACTORY/pull/new/homework
remote: 
To https://github.com/sashiva12/SKILLFACTORY.git
 * [new branch]      homework -> homework
piupiu@AK-PC SKILLFACTORY % 


Получаем свежие данные репозитория (git clone — 15.1 или git pull origin feature-branch — 15.3).
Пишем код.
огда есть определённый набор изменений, делаем коммит (изменения закрепляются) (git add и git commit).
Снова пишем код.
Снова коммитим код (git commit -am).
Делимся полученным результатом (git push origin feature-branch — 15.3).

git mv - to rename file n keep logs of ammendments
git commit --ammend - change name of commit

cd
ls -la
git --help - installs git ()
git status - shows commits, repository status
git init - creates new repository 
git clone urllink - will cone from github repository localy
cat Readme.md - opens file to read in cmd

(изменения закрепляются) (git add и git commit)
git add
git commit (add description / tittle for changes commit )
git commit -am
git push origin feature-branch Делимся полученным результатом

git diff - shows difference

git log

git stash


Homework 17.2

piupiu@AK-PC SKILLFACTORY % vim file-feature-1.txt
piupiu@AK-PC SKILLFACTORY % ls -la
piupiu@AK-PC SKILLFACTORY % git status
piupiu@AK-PC SKILLFACTORY % git add file-feature-1.txt
piupiu@AK-PC SKILLFACTORY % vim file-feature-2.txt
piupiu@AK-PC SKILLFACTORY % vim file-feature-1.txt

piupiu@AK-PC SKILLFACTORY % git diff
diff --git a/file-feature-1.txt b/file-feature-1.txt
index 3513c0f..2fe5393 100644
--- a/file-feature-1.txt
+++ b/file-feature-1.txt
@@ -1 +1,2 @@
-Создайте файл file-feature-1.txt с произвольным содержимым (например, текст из предыдущей главы) и зафиксируйте его в Git.
+Создайте файл file-feature-1.txt с произвольным содержимым (например, текст из предыдущей главы) и зафиксируйте его в Git changes added                                                                        more changes
+
piupiu@AK-PC SKILLFACTORY % git add
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?

piupiu@AK-PC SKILLFACTORY % git add file-feature-1.txt
piupiu@AK-PC SKILLFACTORY % git add file-feature-2.txt

piupiu@AK-PC SKILLFACTORY % git log
commit 65fbf544650fadd683bceb7b9a4c49869d873978 (HEAD -> main, origin/main, origin/HEAD)
Author: sashiva12 <37350359+sashiva12@users.noreply.github.com>
Date:   Tue Mar 23 13:52:44 2021 +0100

    Update README.md

commit c4fb46f2054e46f52e70d71b47841e69c369c154
Author: sashiva12 <37350359+sashiva12@users.noreply.github.com>
Date:   Tue Mar 23 13:51:35 2021 +0100

    Initial commit
piupiu@AK-PC SKILLFACTORY % vim  file-feature-3.txt     
piupiu@AK-PC SKILLFACTORY % rm file-feature-3.txt
piupiu@AK-PC SKILLFACTORY % ls -la
total 24
drwxr-xr-x@  6 piupiu  staff  192 Mar 29 23:24 .
drwxr-xr-x@  3 piupiu  staff   96 Mar 29 23:24 ..
drwxr-xr-x@ 13 piupiu  staff  416 Mar 30 20:20 .git
-rw-r--r--   1 piupiu  staff   36 Mar 29 20:21 README.md
-rw-r--r--   1 piupiu  staff  241 Mar 29 23:20 file-feature-1.txt
-rw-r--r--   1 piupiu  staff  269 Mar 29 23:19 file-feature-2.txt





