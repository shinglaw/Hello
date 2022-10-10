# Hello
Testing


slaw@BRC-BC05M53 MINGW64 ~
$ ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk
SSH protocol v.1 is no longer supported

slaw@BRC-BC05M53 MINGW64 ~
$ ssh -l slaw cbrglogin1.molbiol.ox.ac.uk
slaw@cbrglogin1.molbiol.ox.ac.uk's password:
Last login: Mon Oct 10 10:06:21 2022 from client-8-78.eduroam.oxuni.org.uk
[slaw@cbrglogin1 ~]$ ssh-keygen -t rsa -b 4096
Generating public/private rsa key pair.
Enter file in which to save the key (/home/s/slaw/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/s/slaw/.ssh/id_rsa.
Your public key has been saved in /home/s/slaw/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:Jv5rV+u2szMu9odyjb79rm37Lo/crpBhaCJQdj4w0Eg slaw@cbrglogin1
The key's randomart image is:
+---[RSA 4096]----+
|   .E+= .        |
|    .o.=         |
|    .   o        |
|     .   . .     |
|      o S o o    |
|     . + o ..o   |
|      .    .o=   |
|       .. = X+++.|
|       .o+ XOO*%%|
+----[SHA256]-----+
[slaw@cbrglogin1 ~]$ ssh-keygen -t ecdsa -b 521
Generating public/private ecdsa key pair.
Enter file in which to save the key (/home/s/slaw/.ssh/id_ecdsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/s/slaw/.ssh/id_ecdsa.
Your public key has been saved in /home/s/slaw/.ssh/id_ecdsa.pub.
The key fingerprint is:
SHA256:8IYsD9G88E+LQ8Uc6ulBYeK6t5HL3A9qfgP+L/DqWKg slaw@cbrglogin1
The key's randomart image is:
+---[ECDSA 521]---+
|    . o .        |
|   . = = .       |
|    + * +        |
|   . B B         |
|  . o X S        |
|   ooB * .       |
|  o.=+* o        |
| . *o*=o         |
|E .+X+o=o        |
+----[SHA256]-----+
[slaw@cbrglogin1 ~]$ ^C
[slaw@cbrglogin1 ~]$ cat /home/s/slaw/.ssh/id_ecdsa.pub
ecdsa-sha2-nistp521 AAAAE2VjZHNhLXNoYTItbmlzdHA1MjEAAAAIbmlzdHA1MjEAAACFBADmOEJxrf8JtD63K+doZM+knQc5N9QhjdDTNTAGK4vgFM3UyowZOreJ2VsAx5XQppAH4zvAwpErR4A595dA2+1dAAHBmGAUlsA/fM72NWqneoBjCytsoQslimTgdd37BzGwnDi+fYVnwY4AJ6nXdlYODuwYZD7M7FrFxpbIrZe15hd9ZA== slaw@cbrglogin1
[slaw@cbrglogin1 ~]$ git
usage: git [--version] [--help] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

The most commonly used git commands are:
   add        Add file contents to the index
   bisect     Find by binary search the change that introduced a bug
   branch     List, create, or delete branches
   checkout   Checkout a branch or paths to the working tree
   clone      Clone a repository into a new directory
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   fetch      Download objects and refs from another repository
   grep       Print lines matching a pattern
   init       Create an empty Git repository or reinitialize an existing one
   log        Show commit logs
   merge      Join two or more development histories together
   mv         Move or rename a file, a directory, or a symlink
   pull       Fetch from and merge with another repository or a local branch
   push       Update remote refs along with associated objects
   rebase     Forward-port local commits to the updated upstream head
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index
   show       Show various types of objects
   status     Show the working tree status
   tag        Create, list, delete or verify a tag object signed with GPG

'git help -a' and 'git help -g' lists available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
[slaw@cbrglogin1 ~]$ git --version
git version 1.8.3.1
[slaw@cbrglogin1 ~]$ module avail git
----------------------------------------------------------------- /package/environment-modules/modulefiles -----------------------------------------------------------------
git/2.31.1
[slaw@cbrglogin1 ~]$ nano .bashrc
[slaw@cbrglogin1 ~]$ source .bashrc
[slaw@cbrglogin1 ~]$ git --version
git version 2.31.1
[slaw@cbrglogin1 ~]$ cat .bashrc
# .bashrc

# Source global definitions
if [ -f /etc/bashrc ]; then
        . /etc/bashrc
fi

# Uncomment the following line if you don't like systemctl's auto-paging feature:
# export SYSTEMD_PAGER=

# User specific aliases and functions
module load git/2.31.1

[slaw@cbrglogin1 ~]$ git config --global user.name
[slaw@cbrglogin1 ~]$ git config --global user.email
[slaw@cbrglogin1 ~]$ git config --global user.name "Shing Law"
[slaw@cbrglogin1 ~]$ global user.email "shing.law@ndorms.ox.ac.uk"
-bash: global: command not found
[slaw@cbrglogin1 ~]$ git config --global user.email "shing.law@ndorms.ox.ac.uk"
[slaw@cbrglogin1 ~]$ git config --global user.name
Shing Law
[slaw@cbrglogin1 ~]$ git config --global user.email
shing.law@ndorms.ox.ac.uk
[slaw@cbrglogin1 ~]$ cd /project/obds/$USER/git
-bash: cd: /project/obds/slaw/git: No such file or directory
[slaw@cbrglogin1 ~]$ mkdir /project/obds/$USER/git
[slaw@cbrglogin1 ~]$ cd /project/obds/$USER/git
[slaw@cbrglogin1 git]$ git clone git@github.com:shinglaw
OBDS_Oct_2022
Cloning into 'shinglaw'...
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ECDSA key fingerprint is SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM.
ECDSA key fingerprint is MD5:7b:99:81:1e:4c:91:a5:0d:5a:2e:2e:80:13:3f:24:ca.
Are you sure you want to continue connecting (yes/no)? n
Please type 'yes' or 'no': no
Host key verification failed.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
[slaw@cbrglogin1 git]$ git clone git@github.com:shinglaw/OBDS_Oct_2022.git
Cloning into 'OBDS_Oct_2022'...
The authenticity of host 'github.com (140.82.121.3)' can't be established.
ECDSA key fingerprint is SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM.
ECDSA key fingerprint is MD5:7b:99:81:1e:4c:91:a5:0d:5a:2e:2e:80:13:3f:24:ca.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,140.82.121.3' (ECDSA) to the list of known hosts.
Enter passphrase for key '/home/s/slaw/.ssh/id_ecdsa':
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
[slaw@cbrglogin1 git]$ pmd
-bash: pmd: command not found
[slaw@cbrglogin1 git]$ pwd
/project/obds/slaw/git
[slaw@cbrglogin1 git]$ ls
OBDS_Oct_2022
[slaw@cbrglogin1 git]$ cd OBDS_May_2022
-bash: cd: OBDS_May_2022: No such file or directory
[slaw@cbrglogin1 git]$ cd OBDS_Oct_2022/
[slaw@cbrglogin1 OBDS_Oct_2022]$ ls
README.md
[slaw@cbrglogin1 OBDS_Oct_2022]$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
[slaw@cbrglogin1 OBDS_Oct_2022]$ nano .gitignore
[slaw@cbrglogin1 OBDS_Oct_2022]$ ls -a
.  ..  .git  .gitignore  README.md
[slaw@cbrglogin1 OBDS_Oct_2022]$ status
-bash: status: command not found
[slaw@cbrglogin1 OBDS_Oct_2022]$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
[slaw@cbrglogin1 OBDS_Oct_2022]$ git add .gitignore
[slaw@cbrglogin1 OBDS_Oct_2022]$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore

[slaw@cbrglogin1 OBDS_Oct_2022]$ git commit -m "add file .ignore"
[main d317cec] add file .ignore
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore
[slaw@cbrglogin1 OBDS_Oct_2022]$ status
-bash: status: command not found
[slaw@cbrglogin1 OBDS_Oct_2022]$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
[slaw@cbrglogin1 OBDS_Oct_2022]$ git push
Warning: Permanently added the ECDSA host key for IP address '140.82.121.4' to the list of known hosts.
Enter passphrase for key '/home/s/slaw/.ssh/id_ecdsa':
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 48 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 300 bytes | 50.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:shinglaw/OBDS_Oct_2022.git
   ae86f04..d317cec  main -> main
[slaw@cbrglogin1 OBDS_Oct_2022]$ client_loop: send disconnect: Connection reset by peer

slaw@BRC-BC05M53 MINGW64 ~
$ cat
ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk
ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk


$ ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk
$ ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk
dir
dir


slaw@BRC-BC05M53 MINGW64 ~
$ ssh -1 slaw cbrglogin1.molbiol.ox.ac.uk
SSH protocol v.1 is no longer supported

slaw@BRC-BC05M53 MINGW64 ~
$ ssh -l slaw cbrglogin1.molbiol.ox.ac.uk
slaw@cbrglogin1.molbiol.ox.ac.uk's password:
Last login: Mon Oct 10 10:14:32 2022 from client-8-78.eduroam.oxuni.org.uk
[slaw@cbrglogin1 ~]$ git pull
fatal: not a git repository (or any parent up to mount point /Filers)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
[slaw@cbrglogin1 ~]$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  R  Templates  Videos
[slaw@cbrglogin1 ~]$ cd /project/obds
[slaw@cbrglogin1 obds]$ ls
aejaz     ccohen   dagarwal  ecarroll  gcaratti  heggingt  jsayers   kgupta    mbull  nelliott  ntatzwie  rling   slaw     yzhao
albrecht  cgeorge  dsims     fclanchy  gsangha   ipark     jsouthco  macmahon  mczeh  nicki     nyang     shared  srahmig
[slaw@cbrglogin1 obds]$ cd slaw
[slaw@cbrglogin1 slaw]$ ls
git
[slaw@cbrglogin1 slaw]$ cd git
[slaw@cbrglogin1 git]$ ls
OBDS_Oct_2022
[slaw@cbrglogin1 git]$ cd OBDS_Oct_2022/
[slaw@cbrglogin1 OBDS_Oct_2022]$ git pull
Enter passphrase for key '/home/s/slaw/.ssh/id_ecdsa':
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 674 bytes | 11.00 KiB/s, done.
From github.com:shinglaw/OBDS_Oct_2022
   d317cec..c5a6c4a  main       -> origin/main
Updating d317cec..c5a6c4a
Fast-forward
 README.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
[slaw@cbrglogin1 OBDS_Oct_2022]$ cat readme
cat: readme: No such file or directory
[slaw@cbrglogin1 OBDS_Oct_2022]$ ls
README.md
[slaw@cbrglogin1 OBDS_Oct_2022]$ cat README.md
# OBDS_Oct_2022
Hello
[slaw@cbrglogin1 OBDS_Oct_2022]$ git
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone             Clone a repository into a new directory
   init              Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add               Add file contents to the index
   mv                Move or rename a file, a directory, or a symlink
   restore           Restore working tree files
   rm                Remove files from the working tree and from the index
   sparse-checkout   Initialize and modify the sparse-checkout

examine the history and state (see also: git help revisions)
   bisect            Use binary search to find the commit that introduced a bug
   diff              Show changes between commits, commit and working tree, etc
   grep              Print lines matching a pattern
   log               Show commit logs
   show              Show various types of objects
   status            Show the working tree status

grow, mark and tweak your common history
   branch            List, create, or delete branches
   commit            Record changes to the repository
   merge             Join two or more development histories together
   rebase            Reapply commits on top of another base tip
   reset             Reset current HEAD to the specified state
   switch            Switch branches
   tag               Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch             Download objects and refs from another repository
   pull              Fetch from and integrate with another repository or a local branch
   push              Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
[slaw@cbrglogin1 OBDS_Oct_2022]$
