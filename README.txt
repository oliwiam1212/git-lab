 jestem Oliwia
studiuje na agh
hahahahahahaha
nie 
tak
ok hej
pa
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\student> ssh -p 2009
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface] [-b bind_address]
           [-c cipher_spec] [-D [bind_address:]port] [-E log_file]
           [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file]
           [-J destination] [-L address] [-l login_name] [-m mac_spec]
           [-O ctl_cmd] [-o option] [-P tag] [-p port] [-Q query_option]
           [-R address] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]]
           destination [command [argument ...]]
PS C:\Users\student> ssh -p 2009 student@149.156.194.192
The authenticity of host '[149.156.194.192]:2009 ([149.156.194.192]:2009)' can't be established.
ED25519 key fingerprint is SHA256:R15TClw3t5KwwR2vv+LcUm3Ca+QIleSYvQVnlg0zvIY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[149.156.194.192]:2009' (ED25519) to the list of known hosts.
(student@149.156.194.192) Password:
(student@149.156.194.192) Password:

 System information as of Tue Mar 10 10:48:15 UTC 2026

  System load:           0.08
  Usage of /:            63.2% of 915.32GB
  Memory usage:          5%
  Swap usage:            0%
  Temperature:           57.8 C
  Processes:             22
  Users logged in:       0
  IPv4 address for eth0: 10.191.221.184
  IPv6 address for eth0: fd42:e0c6:e7ff:c3b0:216:3eff:fe8b:b0f1

=================================================================
           WITAJ W LABORATORIUM GIT & DOCKER (LXD)
=================================================================
 Jesteś zalogowany jako: student
 Twoje środowisko jest odizolowane i gotowe do pracy.

 PRZYDATNE KOMENDY NA START:
  > git status     - sprawdzenie stanu lokalnego repozytorium
  > docker ps      - lista aktualnie uruchomionych kontenerów
  > clear          - wyczyszczenie ekranu terminala
=================================================================


The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

student@student-09:~$ mkdir git-lab
student@student-09:~$ ls
git-lab
student@student-09:~$ ls -l
total 4
drwxrwxr-x 2 student student 4096 Mar 10 11:02 git-lab
student@student-09:~$ ls -lh
total 4.0K
drwxrwxr-x 2 student student 4.0K Mar 10 11:02 git-lab
student@student-09:~$ cd git-lab/
student@student-09:~/git-lab$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/student/git-lab/.git/
student@student-09:~/git-lab$ git statuts
git: 'statuts' is not a git command. See 'git --help'.

The most similar command is
        status
student@student-09:~/git-lab$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
student@student-09:~/git-lab$ touch README.txt
student@student-09:~/git-lab$ ls
README.txt
student@student-09:~/git-lab$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.txt

nothing added to commit but untracked files present (use "git add" to track)
student@student-09:~/git-lab$ git add .
student@student-09:~/git-lab$ git commit -m "Initial commit"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <student@student-09.lxd>) not allowed
student@student-09:~/git-lab$  git config --global user.email olawola11@op.pl
student@student-09:~/git-lab$ git config --global user.name "Oliwia Mosór"
student@student-09:~/git-lab$ git commit -m "Initial commit"
[master (root-commit) 4365d83] Initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.txt
student@student-09:~/git-lab$ git status
On branch master
nothing to commit, working tree clean
student@student-09:~/git-lab$ git log
commit 4365d83e40781aad9d6fd3460ae5fbe4339251e4 (HEAD -> master)
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:16:38 2026 +0000

    Initial commit
student@student-09:~/git-lab$ nano README.txt
student@student-09:~/git-lab$ cat README.txt
HEJ jestem Oliwia
student@student-09:~/git-lab$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.txt

no changes added to commit (use "git add" and/or "git commit -a")
student@student-09:~/git-lab$ git diff README.txt
diff --git a/README.txt b/README.txt
index e69de29..912de94 100644
--- a/README.txt
+++ b/README.txt
@@ -0,0 +1 @@
+HEJ jestem Oliwia
student@student-09:~/git-lab$ git add README.txt
student@student-09:~/git-lab$ git commit -m "Update README"
[master 885a0dc] Update README
 1 file changed, 1 insertion(+)
student@student-09:~/git-lab$ git log
commit 885a0dce47fe933a6ec8dff5024d384b0b5cd370 (HEAD -> master)
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:22:26 2026 +0000

    Update README

commit 4365d83e40781aad9d6fd3460ae5fbe4339251e4
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:16:38 2026 +0000

    Initial commit
student@student-09:~/git-lab$ git branch feature
student@student-09:~/git-lab$ git branch
  feature
* master
student@student-09:~/git-lab$ git checkout feature
Switched to branch 'feature'
student@student-09:~/git-lab$ git status
On branch feature


student@student-09:~/git-lab$ cat README.txt
 jestem Oliwia
studiuje na agh
student@student-09:~/git-lab$ git add .
student@student-09:~/git-lab$ git commit -m "Update 2"
[feature f424299] Update 2
 1 file changed, 2 insertions(+), 1 deletion(-)
student@student-09:~/git-lab$ git log
commit f424299ebeb8d406d024d93fb873ac128acbb6eb (HEAD -> feature)
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:34:43 2026 +0000

    Update 2

commit 885a0dce47fe933a6ec8dff5024d384b0b5cd370 (master)
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:22:26 2026 +0000

    Update README

commit 4365d83e40781aad9d6fd3460ae5fbe4339251e4
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:16:38 2026 +0000

    Initial commit
student@student-09:~/git-lab$ git checkout master
Switched to branch 'master'
student@student-09:~/git-lab$ cat README.txt
HEJ jestem Oliwia
student@student-09:~/git-lab$ git merge feature
Updating 885a0dc..f424299
Fast-forward
 README.txt | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
student@student-09:~/git-lab$ git log
commit f424299ebeb8d406d024d93fb873ac128acbb6eb (HEAD -> master, feature)
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:34:43 2026 +0000

    Update 2

commit 885a0dce47fe933a6ec8dff5024d384b0b5cd370
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:22:26 2026 +0000

    Update README

commit 4365d83e40781aad9d6fd3460ae5fbe4339251e4
Author: Oliwia Mosór <olawola11@op.pl>
Date:   Tue Mar 10 11:16:38 2026 +0000

    Initial commit
student@student-09:~/git-lab$ git branch -d feature
Deleted branch feature (was f424299).
student@student-09:~/git-lab$ git branch
* master
student@student-09:~/git-lab$ git branch -M main
student@student-09:~/git-lab$ git status
On branch main
nothing to commit, working tree clean
student@student-09:~/git-lab$ git remote add origin https://github.com/oliwiam1212/git-lab.git
student@student-09:~/git-lab$ git push -u origin main
Username for 'https://github.com': oliwiam1212
Password for 'https://oliwiam1212@github.com':
remote: Invalid username or token. Password authentication is not supported for Git operations.
fatal: Authentication failed for 'https://github.com/oliwiam1212/git-lab.git/'
student@student-09:~/git-lab$ git push -u origin main
Username for 'https://github.com': oliwiam1212
Password for 'https://oliwiam1212@github.com':
To https://github.com/oliwiam1212/git-lab.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/oliwiam1212/git-lab.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
student@student-09:~/git-lab$ git push -uf origin main
Username for 'https://github.com': oliwiam1212
Password for 'https://oliwiam1212@github.com':
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (9/9), 704 bytes | 704.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/oliwiam1212/git-lab.git
 + 99130b7...f424299 main -> main (forced update)
branch 'main' set up to track 'origin/main'.
student@student-09:~/git-lab$ nano README.txt
student@student-09:~/git-lab$ git commit -m "Update 3"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.txt

no changes added to commit (use "git add" and/or "git commit -a")
student@student-09:~/git-lab$ git push
Username for 'https://github.com': oliwiam1212
Password for 'https://oliwiam1212@github.com':
To https://github.com/oliwiam1212/git-lab.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/oliwiam1212/git-lab.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
student@student-09:~/git-lab$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 939 bytes | 939.00 KiB/s, done.
From https://github.com/oliwiam1212/git-lab
   f424299..4f9f528  main       -> origin/main
Updating f424299..4f9f528
error: Your local changes to the following files would be overwritten by merge:
        README.txt
Please commit your changes or stash them before you merge.
Aborting
student@student-09:~/git-lab$ git config pull.rebase false
student@student-09:~/git-lab$ git pull
Updating f424299..4f9f528
error: Your local changes to the following files would be overwritten by merge:
        README.txt
Please commit your changes or stash them before you merge.
Aborting
student@student-09:~/git-lab$ nano README.txt
student@student-09:~/git-lab$ git pull
Updating f424299..4f9f528
error: Your local changes to the following files would be overwritten by merge:
        README.txt
Please commit your changes or stash them before you merge.
Aborting
student@student-09:~/git-lab$ cat README.txt
lalala
lol
hej
mam 20 lat jestem Oliwia
studiuje na agh
student@student-09:~/git-lab$ git push
Username for 'https://github.com': oliwiam1212
Password for 'https://oliwiam1212@github.com':
To https://github.com/oliwiam1212/git-lab.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/oliwiam1212/git-lab.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
student@student-09:~/git-lab$ nano README.txt
student@student-09:~/git-lab$ git add .
student@student-09:~/git-lab$ git commit -m "Update 4"
[main 41b059d] Update 4
 1 file changed, 4 insertions(+), 1 deletion(-)
student@student-09:~/git-lab$ git push
Username for 'https://github.com': git pull
Password for 'https://git%20pull@github.com':
remote: Invalid username or token. Password authentication is not supported for Git operations.
fatal: Authentication failed for 'https://github.com/oliwiam1212/git-lab.git/'
student@student-09:~/git-lab$ git push
Username for 'https://github.com': oliwia1212
Password for 'https://oliwia1212@github.com':
To https://github.com/oliwiam1212/git-lab.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/oliwiam1212/git-lab.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
student@student-09:~/git-lab$ git pull
Auto-merging README.txt
Merge made by the 'ort' strategy.
 README.txt | 5 +++++
 1 file changed, 5 insertions(+)
student@student-09:~/git-lab$ git config pull.rebase marge
student@student-09:~/git-lab$
