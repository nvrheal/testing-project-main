# Git Concepts 

**Master** / **Main** is the default main branch name in older Git repositories, representing the primary line of development. It is often used to hold the production-ready or stable version of a project.

**Origin** is the default name Git gives to the remote repository (like on GitHub or GitLab) that your local repo is connected to. The main branch in the remote repository is called **origin/main**

**HEAD** in Git is a pointer that shows your current location — it usually points to the latest commit in the branch you’re working on.

**Commit Hash** is a unique 40-character identifier (SHA-1) that Git generates for each commit to track and reference it precisely.

**Merge** takes the updates made in one branch and applies them to another, bringing both branches’ work together into a unified history.

# Git Commands

**Initializing a new Git repository** in the current directory, allowing you to start tracking your project's files with Git.

```bash
    git init
```

**Set the username and email** used for commits in the current repository only.

```bash
    git config user.name "Your Name"
    git config user.email "you@example.com"
```

**Display all Git configuration** settings currently in effect.

```bash
    git config --list
```

**Stage changes** (new, modified, or deleted files) to be included in the next commit.

```bash
    git add filename                    # stages a specific file.
    git add .                           # stages all changes in the current directory.
    git add -A                          # stages all changes across the repository.
```

**Commit the staged changes** as a new snapshot in the repository’s history.

```bash
    git commit -m "message"
```

**Shows the current state** of your working directory and staging area — it tells you which files are modified, staged, or untracked.

```bash
    git status
```

**Display the commit history** of the repository.

```bash
    git log -v                              # verbose
```

**Move your project head** to the exact state of that specific commit (**detached HEAD state**) or branch.

```bash
    git checkout <commit-hash>              # head -> <commit-hash>
    git checkout master                     # head -> master
```

**Create a new branch** and immediately switches to it.

```bash
    git checkout -b branch-name
```

**list all branches and highlights** the one you’re currently on with an asterisk (`*`).

```bash
    git branch
```

**Merge the changes** from the branch-name branch into your master branch.

```bash
    git checkout master
    git merge branch-name
```

**connects your local repository to a remote one** on GitHub.

```bash
    git remote add origin https://github.com/johnabdulshahied/project-name.git              # Connect local repo Origin to github project URL origin
    git branch -M main                                                                      # rename your master branch to main
    git push -u origin main                                                                 # push main to origin/main
```

**Show the URLs of the remote repositories linked** to your project for fetching and pushing changes.

```bash
    git remote -v
```

**Upload the main branch in the local repository to the remote repository** and sets it as the default branch for future pushes and pulls.

```bash
    git push -u origin main
```

**Fetche and Merge any new changes** on remote branch from the remote repository.

```bash
    git pull                            # Pull from remote repo the branch you are currently on
    git pull origin main                # Pull explicitly the origin branch in the remote repository to the main branch in local repository
```