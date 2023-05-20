# Configuring user information used across all local repositories

git config --global user.name “[firstname lastname]
git config --global user.email “[valid-email]”


# SETUP & INIT
retrieve an entire repository from a hosted location via URL
git init

initialize an existing directory as a Git repository
git clone [url]

# INSPECT & COMPARE

show the commit history for the currently active branch
git log

show the commits on branchA that are not on branchB
git log branchB..branchA


show the commits that changed file, even across renames
git log --follow [file]

show the diff of what is in branchA that is not in branchB
git diff branchB...branchA


show any object in Git in human-readable format
git show [SHA]


# TRACKING PATH CHANGES

git rm [file]
delete the file from project and stage the removal for commit
git mv [existing-path] [new-path]
change an existing file path and stage the move
git log --stat -M
show all commit logs with indication of any paths that moved

# IGNORING PATTERNS
Preventing unintentional staging or commiting of files
logs/
*.notes
pattern*/

Save a file with desired paterns as .gitignore with either direct string 
matches or wildcard globs
git config --global core.excludesfile [file]
system wide ignore patern for all local repositories


# STAGE & SNAPSHOT
Working with snapshots and the Git staging area
git status
show modified files in working directory, staged for your next commit
git add [file]
add a file as it looks now to your next commit (stage)
git reset [file]
unstage a file while retaining the changes in working directory
git diff
diff of what is changed but not staged
git diff --staged
diff of what is staged but not yet commited
git commit -m “[descriptive message]”
commit your staged content as a new commit snapshot


# REWRITE HISTORY

git rebase [branch]
apply any commits of current branch ahead of specified one
git reset --hard [commit]
clear staging area, rewrite working tree from specified commit


# TEMPORARY COMMITS
git stash
Save modified and staged changes
git stash list
list stack-order of stashed file changes
git stash pop
write working from top of stash stack
git stash drop
discard the changes from top of stash stack