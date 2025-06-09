# DevOps-Learning-Git

**Version Control**

Version control is a system that tracks changes to your code over time. With version control, you can undo  mistakes, see who made changes and collaborate without stepping on anyones toes. 


**Git is not a file tracker**

Git tracks snapshots not diffs. What that means is everytime a commit is pushed , Git takes a snapshot of what the file looks like at that point in time, not what just changed. For example, if one line is changed, it will store a full new version of that file efficiently

Git uses a key-value store (SHA-1 hash) represents the content and stores everything as objects (blobs, trees). If the content of the file chnages, the hash will also change. Each commit will show a full snapshot of the files being pushed. The files are content addressed, not file-name based. 


**README File**

A README file is an essential component of any Git repository. It provides vital information about your project, helps new contributors to get started serves as the first point of reference for users. By including clear and comprehensive sections in the README file, you can ensure that a project is accessible, well documented andf welcoming to new contributors. 

--------------------------------------------------------------------------------------------------------------------------
