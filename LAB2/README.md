Requirements: 

From main, create feature/add-transform.
Add a transformation function, commit.
Switch to main, edit the same file to force a conflict.
Merge, resolve the conflict, and commit.

---

PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git checkout -b feature/add-transform
Switched to a new branch 'feature/add-transform'
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> netepad pipeline.py
netepad : The term 'netepad' is not recognized as the name of a cmdlet, function, script file, or
operable program. Check the spelling of the name, or if a path was included, verify that the path is
correct and try again.
At line:1 char:1
+ netepad pipeline.py
+ ~~~~~~~
    + CategoryInfo          : ObjectNotFound: (netepad:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> notepad pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git status
On branch feature/add-transform
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pipeline.py

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git add pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git status
On branch feature/add-transform
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   pipeline.py

PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git commit -m "Add Transformation Function"
[feature/add-transform 0c67696] Add Transformation Function
 1 file changed, 2 insertions(+)
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git checkout 'main'
Switched to branch 'main'
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> notepad pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pipeline.py

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git add pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git commit -m "Modify transformation on main"
[main 88f8982] Modify transformation on main
 1 file changed, 2 insertions(+)
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git merge feature/add-transform
Auto-merging pipeline.py
CONFLICT (content): Merge conflict in pipeline.py
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> notepad pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git add pipeline.py
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git commit -m "Resolve merge conflict"
[main e210724] Resolve merge conflict
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git log --oneline --graph --all
*   e210724 (HEAD -> main) Resolve merge conflict
|\
| * 0c67696 (feature/add-transform) Add Transformation Function
* | 88f8982 Modify transformation on main
|/
* 27b3406 Initial project setup
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline>
