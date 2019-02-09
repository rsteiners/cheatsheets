- git init (under a folder to add it to git)
- git status
- git add <filename>
- git diff <filename>
- git commit [-v -a -m<message>] (commit to the local repo)
- git push (send the commit to the remote server)
- git diff --staged

.gitignore file (see patterns on https://github.com/github/gitignore)

### History
- git log (history)
- git log -2 (two most recent commits)
- git log --pretty=<oneline|full|fuller>
- git log --since "2 months"
- git log --until "2 months"
- git log --graph

### Changing the commit befor pushing to the server
- git commit --amend (replaces the previous commit)

### Reverting the commit
- git revert <commitID> (use git log to find the commitID)

### Cloning
- git clone <url> (make sure it is https)

### Remote
- git remote (list the remotes)

#### Also possible:
  - git remote add <remote_repo_name>
  - git remote remove <remote_repo_name>
  - git fetch <remote_repo_name> (download information from the remote repo, but doesn’t merge)
  - git merge <remote_repo_name>/master master (this one merges)

### Perform the change to the target file
- Perform a git status - you will see the file had been modified
- Perform a git add <target_file> to add this modified file the the staging area
- Perform a git status again to see that the changes are now ready to be committed
- Perform a git commit - it opens the editor so that you can enter the commit comment
- Perform a git push <remote_repo_name> master (finally pushes the change to the server under the master branch)
- Perform a git remote show <remote_repo_name>

Note: git pull is an alias to git fetch + git merge all together.

### Tags
- git tag (list all the tags in the repository)
- git tag --list <glob> shows all tags matching the glob pattern
- git tag “1.0” (creates a lightweight tag called 1.0)
- git show “1.0” (shows the commit of this tag)
- git tag -a “1.1” -m “This is my new annotated tag.”
- git show “1.1”
- git push <remote_repo_name> 1.1 (pushes the 1.1 tag to the remote_repo_name)
- git push <remote_repo_name--tags> (pushes all tags to the remote_repo_name

Note: annotated tags contain more information. Created by passing the -a flag to git.

### Staged area
- git reset <file_name> (removes a file from the staged area).

### Branching
- git branch whatever (create a local branch called whatever, but HEAD stills point to main branch)
- git checkout whatever (move HEAD to the whatever branch)
- git checkout -b whatever (this is the shorthand for the previous two commands in one shot)
- git branch --no-merged (list all branches that contain work you haven’t merged yet)
- git branch -v (list the last commit on each branch)
- git branch -d <branch_name> (deletes the target branch)

### See also
- https://randyfay.com/content/avoiding-git-disasters-gory-story
- https://randyfay.com/content/rebase-workflow-git
- pull request workflow
