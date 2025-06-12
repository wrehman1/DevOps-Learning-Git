# DevOps-Learning-Git
---------------------------------------------------------------------------------------------------------

**Version Control**

Version control is a system that tracks changes to your code over time. With version control, you can undo  mistakes, see who made changes and collaborate without stepping on anyones toes. 

-----------------------------------------------------------------------------------------------------------
**Git is not a file tracker**

Git tracks snapshots not diffs. What that means is everytime a commit is pushed , Git takes a snapshot of what the file looks like at that point in time, not what just changed. For example, if one line is changed, it will store a full new version of that file efficiently

Git uses a key-value store (SHA-1 hash) represents the content and stores everything as objects (blobs, trees). If the content of the file chnages, the hash will also change. Each commit will show a full snapshot of the files being pushed. The files are content addressed, not file-name based. 

-----------------------------------------------------------------------------------------------------------
**Git Terminology**

• Repository --> a Git project (tracked folder with a .git directory).

• Commit --> a snapshot of your files and metadata (author, timestamp, message, parent commit, etc).

• Branch --> a movable pointer to a specific commit (e.g. main, dev, feature/login).

• Remote --> a reference to an external Git host (like Github, GitLab) usually named origin.

• Staging Area --> also called the Index; a buffer between your working directory and the repo  what you plan to commit.

• Blobs --> "binary large object" - stores the actual content of files(just the data, no filename/path).

• Trees --> stores filenames, file paths, and pointers to blobs (files) and other trees (directories). Represents a directory snapshot.

• Refs (Reference) --> pointer to a commit: branches (refs/heads), tags (refs,tags), and special ones like HEAD.

• HEAD --> pointer to the current branch or commit you're working on. 

• Index --> the actual file .git/index, a binary file that holds the staging area info.

• Object Store --> .git/objects/ - where Git stores all blobs, trees and commits by SHA hash.

• Tag --> a ref to a specific commit, often used for marking releases. 

-----------------------------------------------------------------------------------------------------------
**Git Commands**

• git init: inilialises a new Git repo with .git directory

• git add: stage changes

• git commit: snapshot changes

• git status: show staged/unstaged work

• git log: show commit history

• git diff: show what changed

• git config: set user/email

• git help <command>: built-in-docs

• git clone: copy a remote repo

• git rm: remove files

• git mv: rename files

• git restore: undo file chnages (modern)

-----------------------------------------------------------------------------------------------------------
**3 areas  of Git**

(1): Working Directory - Files you're editing

(2): Staging Area (Index) - Changes marked for commit

(3): Repository (local.git) - Commit Snapshots

The Flow: [Working Directory] --> git add --> [Staging Area] --> git commit --> [Repository]

-----------------------------------------------------------------------------------------------------------
**Viewing History**

• git log : see commit history

• git log --oneline --graph : visual summary

• git show <commit> : view a specific commit

• git diff : compare unstaged vs last commit

• git diff --staged : compare staged vs last commit

    **BONUS**
    
• git blame <file> : show who last changed each line

• git reflog : view local HEAD history (even deleted branches)

-----------------------------------------------------------------------------------------------------------
**Git vs GitHub**

Git (CLI) is a version control tool. It runs locally on the computer itself. The main purpose of Git is to track and manage code history on the CLI. Git can be used offline and it is Open Source. 

GitHub is a Git repo for hosting and collaboration. It runds on the web (cloud). The main purpose of GitHub is to share code, manage code, open PRs, and collaborate on the GUI. It can't be used offline and is currently owned by Microsoft.  

------------------------------------------------------------------------------------------------------------------------
**README File**

A README file is an essential component of any Git repository. It provides vital information about your project, helps new contributors to get started serves as the first point of reference for users. By including clear and comprehensive sections in the README file, you can ensure that a project is accessible, well documented andf welcoming to new contributors. 

-----------------------------------------------------------------------------------------------------------
**Branching**

• *git branch* : list/create branches

• *git checkout -b <branch>* : create & switch (older syntax)

• *git switch -c <branch>* : modern version

• *git switch <branch>* : switch branches safely

• *git branch -d <branch>* : delete branch

   --Note--

• git switch is newer and more beginner friendly. It works only with newer git versions.

• git branch only creates or lists, it does not switch. 

• checkout still works but is multi-purpose and confusing. 

----------------------------------------------------------------------------------------------------------
**Visualise Branches & Logs**

• "git log --oneline" : compact commit view

• "git log --graph" : visual tree structure

• "git log --oneline --graph --all" : compact. visual and full view. Great for debugging merges and           tracking branches, it shows whats really happening under the hood.

------------------------------------------------------------------------------------------------------
**Rebase vs Merge**

**Merge** is safe and friendly; it brings two branches together and **preserves history** (you can always see where the branch is joint) which makes it great for collaboration. It also creates a new commit called merge commit. It is useful for team workflows.

**Rebase** rewrites history and creates a linear timeline with no merge commits - perfect for when you want to clean up before the pull request. 

------------------------------------------------------------------------------------------------------
**Git Stash & Pop**

• *git stash* : temporarily save uncomitted changes

• *git stash list* : view all stashes

• *git stash apply* : reapply latest stash (keeps stash)

• *git stash pop* : reapply and delete the stash

Use when switching branches mid-task and great for "I'm ready to commit, but I need to move".

------------------------------------------------------------------------------------------------------
**Reset, Revert and Cherry-Pick**

![image](https://github.com/user-attachments/assets/1fa87126-433a-4389-b889-d742860faf03)

------------------------------------------------------------------------------------------------------
**Fork & Pull Requests**










