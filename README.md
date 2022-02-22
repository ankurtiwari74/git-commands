# git-commands
Git Commands

Check Config: 
				git config -l
				
Add Username: 
				git config --global user.name "Ankur Tiwari"
				
Add Email: 
				git config --global user.email "ankurtiwari74@yahoo.com"
				
Initialize Project: 
				git init
				
Staging Files: 
				1. Add Files to Staging
					git add FileName
					git add --all
					git add -A
					git add .
					
				2. Add Commit Message to Staging
					git commit -m "Commit Message"
					
Check Logs: 
				git log
				git log --oneline
				
Check Status of Tracked and Untracked Files: 
				git status
				
Restoring Files: 
				git restore FileName
				git restore .
				git checkout .
				
Restoring the Staged Files:
				git restore --staged FileName
				git restore --staged .
				
Ignore Files:
				Create a .gitignore file at the root level of the project and edit it to ignore specific files.
				Eg. 
				DS_Store
				.vs_code/
				authentication.js
				node_modules
				notes/
				**/*-todo.md
				
Global Ignore File:
				git config --global core.excludesfile [file]
				
Clearing the Cache:
				git rm -r --cached .
				
Deleting a File:
				1. Delete from file system and stage the file to git.
				2. git rm FileName
				
Rename a File:
				1. Rename file from file system, and git will treat it as two operations (1. Delete of OlderFileName, 2. Untracked NewFileName)
				2. git mv OlderFileName NewFileName
				
Differences:
				git diff
				git diff FileName
				
Amending:
				git commit -amend
				git commit -am "New Commit Message"
				git commit -amend --no-edit
				
Reset:
				git reset COMMIT_HASH
				git reset --hard COMMIT_HASH (Not Recommended)
				
Rebasing:
				git rebase <branch>/<commit>
				git rebase --interactive <branch>/<commit>
				git rebase -i HEAD~#
				git rebase -i --root
				
Check Branch:
				git branch
				git branch -a
				
Copy a Branch:
				git switch -c NewBranchName
				git checkout -b BranchName (Deprecated)
				
Merging:
				Go back to main branch (git switch master) then
				git merge <branch>
				
Deleting:
				git branch --delete NAME
				git branch -d NAME
				git branch -D NAME
				
Stashing Code:
				git stash
				# git stash list
				# git stash apply
				# git stash pop
				
Git Clean:
				git clean -n # dry run
				git clean -d # directories
				git clean -f # force 
				
Remote:
				git remote add NAME URL
				# git remote remove NAME
# git rename OLDNAME NEWNAME
				# git remote -v
				
Git Remote Push:
				git push REMOTE BRANCH
				# git push --set-upstream-to origin name
				git push -u origin main # --set-upstream
				# git push --all
				# git branch --set-upstream-to <origin/remote-branch>
![image](https://user-images.githubusercontent.com/47471073/155196285-48cc492b-6aec-4e4d-a3db-fe6e5e3dfead.png)
