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
**README File**

A README file is an essential component of any Git repository. It provides vital information about your project, helps new contributors to get started serves as the first point of reference for users. By including clear and comprehensive sections in the README file, you can ensure that a project is accessible, well documented andf welcoming to new contributors. 

-----------------------------------------------------------------------------------------------------------
