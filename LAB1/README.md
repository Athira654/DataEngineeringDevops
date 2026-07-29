#Requirements

Create a folder de-pipeline, run git init.
Add a pipeline.py and a .gitignore.
Stage and commit with a meaningful message.
Run git log --oneline and confirm your commit.


PS C:\Users\LENOVO THINKPAD> mkdir de-pipeline


    Directory: C:\Users\LENOVO THINKPAD


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        29-07-2026     23:15                de-pipeline


PS C:\Users\LENOVO THINKPAD> cd de-pipeline
PS C:\Users\LENOVO THINKPAD\de-pipeline> git --version
git version 2.55.0.windows.3
PS C:\Users\LENOVO THINKPAD\de-pipeline> git init
Initialized empty Git repository in C:/Users/LENOVO THINKPAD/de-pipeline/.git/
PS C:\Users\LENOVO THINKPAD\de-pipeline> New-Item pipeline.py -ItemType File


    Directory: C:\Users\LENOVO THINKPAD\de-pipeline


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        29-07-2026     23:18              0 pipeline.py


PS C:\Users\LENOVO THINKPAD\de-pipeline> New-Item .gitignore -ItemType File


    Directory: C:\Users\LENOVO THINKPAD\de-pipeline


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        29-07-2026     23:19              0 .gitignore


PS C:\Users\LENOVO THINKPAD\de-pipeline> dir


    Directory: C:\Users\LENOVO THINKPAD\de-pipeline


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        29-07-2026     23:19              0 .gitignore
-a----        29-07-2026     23:18              0 pipeline.py


PS C:\Users\LENOVO THINKPAD\de-pipeline> code .
PS C:\Users\LENOVO THINKPAD\de-pipeline> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        pipeline.py

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\LENOVO THINKPAD\de-pipeline> git add .
PS C:\Users\LENOVO THINKPAD\de-pipeline> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   .gitignore
        new file:   pipeline.py

PS C:\Users\LENOVO THINKPAD\de-pipeline> git commit -m "Initial Project Setup"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'LENOVO THINKPAD@DESKTOP-DM6DETB.(none)')
PS C:\Users\LENOVO THINKPAD\de-pipeline> git config --global user.name "Athira"
>> git config --global user.email "athira.sivanz97@gmail.com"
PS C:\Users\LENOVO THINKPAD\de-pipeline> git commit -m "Initial Project Setup"
[master (root-commit) e252ce2] Initial Project Setup
 2 files changed, 7 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 pipeline.py
PS C:\Users\LENOVO THINKPAD\de-pipeline> git log --oneline
e252ce2 (HEAD -> master) Initial Project Setup
PS C:\Users\LENOVO THINKPAD\de-pipeline>

---
