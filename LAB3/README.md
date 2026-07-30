PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git remote -v
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git remote add origin https://github.com/Athira654/de-pipeline.git
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git remote -v
origin  https://github.com/Athira654/de-pipeline.git (fetch)
origin  https://github.com/Athira654/de-pipeline.git (push)
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 8 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (13/13), 1.19 KiB | 203.00 KiB/s, done.
Total 13 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Athira654/de-pipeline.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git checkout feature/add-transform
Switched to branch 'feature/add-transform'
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git push -u origin feature/add-transform
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'feature/add-transform' on GitHub by visiting:
remote:      https://github.com/Athira654/de-pipeline/pull/new/feature/add-transform
remote:
To https://github.com/Athira654/de-pipeline.git
 * [new branch]      feature/add-transform -> feature/add-transform
branch 'feature/add-transform' set up to track 'origin/feature/add-transform'.
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git log --oneline
e210724 (HEAD -> main, origin/main) Resolve merge conflict
88f8982 Modify transformation on main
0c67696 (origin/feature/add-transform, feature/add-transform) Add Transformation Function
27b3406 Initial project setup
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git revert e210724
error: commit e21072487a8ed03905c63fbfc3d284f10e9354ed is a merge but no -m option was given.
fatal: revert failed
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git tag v0.1.0
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git tag
v0.1.0
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git push origin v0.1.0
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Athira654/de-pipeline.git
 * [new tag]         v0.1.0 -> v0.1.0
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git revert 88f8982
Auto-merging pipeline.py
CONFLICT (content): Merge conflict in pipeline.py
error: could not revert 88f8982... Modify transformation on main
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git revert --abort
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline> git revert 0c67696
Auto-merging pipeline.py
CONFLICT (content): Merge conflict in pipeline.py
error: could not revert 0c67696... Add Transformation Function
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\LENOVO THINKPAD\Desktop\de-pipeline>
