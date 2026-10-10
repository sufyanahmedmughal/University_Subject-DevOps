# Proof of Work

## Git Log Output

7515d31 (HEAD -> main, origin/main) Merge pull request #1 from sufyanahmedmughal/development
043c89f (origin/development, development) fix: resolved merge conflict
4112619 (origin/staging, staging) fix: staging label
708e892 feat: updated script with staging env
8fa2e9a feat: initial commit with deploy script

## Reflection Questions

### Q1: What is the difference between Git (local tracking) and GitHub (cloud platform)?

Git is a distributed version control system that runs on a developer's local machine and tracks changes made to files over time. It allows us to create commits, branches, and merges without needing an internet connection. GitHub is a cloud-based platform that hosts Git repositories online. It adds collaboration features such as pull requests, issue tracking, and code reviews. In short, Git is the tool that tracks the work, while GitHub is the place where that work is stored and shared with others.

### Q2: Explain the 3 architecture stages: Working Directory, Staging Area, Local Repository.

The Working Directory is the folder on our computer where we create and edit files, and changes here are not yet tracked by Git. The Staging Area (index) is an intermediate space where we place selected changes using `git add`, preparing them for the next commit. The Local Repository is the hidden `.git` database where Git permanently stores committed snapshots after we run `git commit`. Files move from the Working Directory to the Staging Area and finally to the Local Repository. This flow lets us choose exactly which changes become part of each commit.

### Q3: What is the difference between git stash pop and git stash apply?

Both commands restore changes that were previously saved using `git stash`. The difference is what happens to the stash entry afterwards. `git stash pop` applies the stashed changes and then removes that entry from the stash list. `git stash apply` applies the changes but keeps the entry in the stash list, so it can be reused on another branch later. We use `pop` when we are done with the stash and `apply` when we want to keep a backup copy.

### Q4: What is the difference between git fetch and git pull?

`git fetch` downloads the latest commits and branch information from the remote repository but does not change our working files or current branch. It lets us review what has changed before deciding to merge. `git pull` is a combination of `git fetch` followed by `git merge`, so it downloads the changes and immediately integrates them into our current branch. Because of this, `git pull` is faster but can cause unexpected merge conflicts. `git fetch` is the safer option when we want to inspect remote changes first.