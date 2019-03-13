git init (under a folder to add it to git)<br />
git status<br />
git add <filename><br />
git diff <filename><br />
git commit [-v -a -m<message>] (commit to the local repo)<br />
git push (send the commit to the remote server)<br />
git diff --staged

.gitignore file (see patterns on https://github.com/github/gitignore)

### Configuration
git config --global user.email "someone@somewhere.whatever"<br />
git config --global user.name "someone"<br />
##### To list all global configuration
git config --global -l
##### To list all local configuration
git config --local -l

### Adding all the files in the current directory
git -a . (note: it adds all files and subdirectories recursively)

### History
git log (history)<br />
git log -2 (two most recent commits)<br />
git log --pretty=<oneline|full|fuller><br />
git log --since "2 months"<br />
git log --until "2 months"<br />
git log --graph<br />

### Changing the commit befor pushing to the server
git commit --amend (replaces the previous commit)

### Reverting the commit
git revert <commitID> (use git log to find the commitID)<br />
git reset HEAD~n (n is the number of last commits to be reverted).
  - Example: git reset HEAD~1 (revert only the latest commit).

### Cloning
git clone <url> (make sure it is https)

### Remote
git remote (list the remotes)

#### Also possible:
  - git remote add <remote_repo_name>
  - git remote remove <remote_repo_name>
  - git fetch <remote_repo_name> (download information from the remote repo, but doesn’t merge)
  - git merge <remote_repo_name>/master master (this one merges)

### Perform the change to the target file
Perform a git status - you will see the file had been modified<br />
Perform a git add <target_file> to add this modified file the the staging area<br />
Perform a git status again to see that the changes are now ready to be committed<br />
Perform a git commit - it opens the editor so that you can enter the commit comment<br />
Perform a git push <remote_repo_name> master (finally pushes the change to the server under the master branch)<br />
Perform a git remote show <remote_repo_name><br />

Note: git pull is an alias to git fetch + git merge all together.

### Tags
git tag (list all the tags in the repository)<br />
git tag --list <glob> shows all tags matching the glob pattern<br />
git tag “1.0” (creates a lightweight tag called 1.0)<br />
git show “1.0” (shows the commit of this tag)<br />
git tag -a “1.1” -m “This is my new annotated tag.”<br />
git show “1.1”<br />
git push <remote_repo_name> 1.1 (pushes the 1.1 tag to the remote_repo_name)<br />
git push <remote_repo_name--tags> (pushes all tags to the remote_repo_name

Note: annotated tags contain more information. Created by passing the -a flag to git.

### Staged area
git reset <file_name> (removes a file from the staged area).

### Branching
git branch whatever (create a local branch called whatever, but HEAD stills point to main branch)<br />
git checkout whatever (move HEAD to the whatever branch)<br />
git checkout -b whatever (this is the shorthand for the previous two commands in one shot)<br />
git checkout -b <new_branch_name> <existent_tag> (create a new branch pointing to an existent tag)<br />
git checkout -t <remote>/<remote_branch> (checkout the remote branch localy)<br />
git branch --no-merged (list all branches that contain work you haven’t merged yet)<br />
git branch -v (list the last commit on each branch)<br />
git branch -d <branch_name> (deletes the target branch)<br />

### See also
https://randyfay.com/content/avoiding-git-disasters-gory-story<br />
https://randyfay.com/content/rebase-workflow-git<br />
pull request workflow
