<img width="772" height="678" alt="Screenshot 2026-08-26 181747" src="https://github.com/user-attachments/assets/447243a9-bdfd-4943-8774-92c365aa089f" />
<img width="565" height="621" alt="Screenshot 2026-08-26 181821" src="https://github.com/user-attachments/assets/51e3c7be-40c5-4464-9056-ffd1e3aea2bf" />
<img width="519" height="649" alt="Screenshot 2026-08-26 181842" src="https://github.com/user-attachments/assets/e794c685-5da1-4ba1-8ea4-be126c594e66" />
<img width="1032" height="558" alt="Screenshot 2026-08-26 181911" src="https://github.com/user-attachments/assets/fae18a9a-12af-4fc2-91a0-61a9cf88420d" />



PS D:\merge> mkdir git-merge-demo


    Directory: D:\merge


Mode                 LastWriteTime         Length Name                   
----                 -------------         ------ ----                   
d-----        26-08-2026  05:58 PM                git-merge-demo         


PS D:\merge> cd git-merge-demo
PS D:\merge\git-merge-demo> git init
Initialized empty Git repository in D:/merge/git-merge-demo/.git/git add .
PS D:\merge\git-merge-demo> 
PS D:\merge\git-merge-demo> git commit -m "Initial commit"
On branch master

Initial commit

nothing to commit (create/copy files and use "git add" to track)
PS D:\merge\git-merge-demo> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS D:\merge\git-merge-demo> git add .
PS D:\merge\git-merge-demo> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS D:\merge\git-merge-demo> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
PS D:\merge\git-merge-demo> git add .
>> git commit -m "Initial commit"
[master (root-commit) 3efc640] Initial commit
 1 file changed, 10 insertions(+)
 create mode 100644 index.html
PS D:\merge\git-merge-demo> git branch -M main
PS D:\merge\git-merge-demo> git branch
* main
PS D:\merge\git-merge-demo> git switch -c feature-contributor
Switched to a new branch 'feature-contributor'
PS D:\merge\git-merge-demo> git branch
* feature-contributor
  main
PS D:\merge\git-merge-demo> git add .
PS D:\merge\git-merge-demo> git commit -m "Add contributor feature"
[feature-contributor c35ac9c] Add contributor feature
 1 file changed, 1 deletion(-)
PS D:\merge\git-merge-demo> git switch main
Switched to branch 'main'
PS D:\merge\git-merge-demo> git branch
  feature-contributor
* main
PS D:\merge\git-merge-demo> git add .
PS D:\merge\git-merge-demo> git commit -m "Add owner update"
[main b2fac30] Add owner update
 1 file changed, 1 insertion(+), 1 deletion(-)
PS D:\merge\git-merge-demo> git log --oneline --graph --all
* b2fac30 (HEAD -> main) Add owner update
| * c35ac9c (feature-contributor) Add contributor feature
|/  
* 3efc640 Initial commit
PS D:\merge\git-merge-demo> git switch main
Already on 'main'
PS D:\merge\git-merge-demo> git merge feature-contributor --no-edit
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
PS D:\merge\git-merge-demo> git log --oneline --graph --all
* b2fac30 (HEAD -> main) Add owner update
| * c35ac9c (feature-contributor) Add contributor feature
|/  
* 3efc640 Initial commit
PS D:\merge\git-merge-demo> git status
On branch main
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   index.html

PS D:\merge\git-merge-demo> git commit -m "Resolve merge conflict"
[main 416b88f] Resolve merge conflict
PS D:\merge\git-merge-demo> git status
On branch main
nothing to commit, working tree clean
PS D:\merge\git-merge-demo> git log --oneline --graph --all
*   416b88f (HEAD -> main) Resolve merge conflict
|\  
| * c35ac9c (feature-contributor) Add contributor feature
* | b2fac30 Add owner update
|/  
* 3efc640 Initial commit    git remote add origin https://github.com/pavithraB-wec/merge.gitge\git-merge-demo> 
PS D:\merge\git-merge-demo> git branch -M main
PS D:\merge\git-merge-demo> git push -u origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 842 bytes | 421.00 KiB/s, done.
Total 10 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/pavithraB-wec/merge.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS D:\merge\git-merge-demo> 
