# GitCheatSheet
all git commands

1.1 GIT ADVANCED
Name	Comment
Git squash to make history clean	git rebase -i HEAD~4; git push origin <branch-name> --force link
Find git branch by commit hash	git name-rev ${commit_hash}, or https://${git_repo_link}/commit/${commit_hash}
List all remote git branches	git ls-remote --heads origin
Git clone repo with another ssh key	ssh-agent bash -c ‘ssh-add yourkey; git clone git@github.com:user/project.git’

1.2 GIT COMMIT
Name	Comment
Git squash to make history clean	git rebase -i HEAD~4; git push origin <branch-name> --force link
Git commit and squash	git commit --amend --no-edit, git push origin <branch-name> --force
Git add patch	git add -p
Git commit	git commit -m ‘XXX’
Git add and commit	git ci -m ‘XXX’
git-concept.png

1.3 GIT UNDO
Name	Comment
Undo git commit	git reset --hard HEAD~1
Undo git pull	git reset --hard
Undo git merge	git merge --abort
Undo git add	git reset filename.txt

1.4 GIT LOG
Name	Comment
Check recent commits	git log -n 3
Check commit by username	git log origin/master -n 3 --author <denny>
Check changes for a given file from a given user	git log origin/master -n 3 --author <denny> <somefile.py>

1.5 GIT DIFF
Name	Comment
Compare git diff after commit	git diff --cached
Compare two git tags	git diff ${sha1sum}..${sha2sum}
Show changed file list	git diff --name-status, git diff --name-status --cached
Git diff two revision	git diff ${sha1sum}..${sha2sum}
Git show file changes	git diff --name-only ${sha1sum} ${sha2sum}
Show changeset of the latest commit	git diff HEAD^
Show prvious changeset for one file	git diff HEAD^ default.rb
Compare two branches in CLI	git diff <branch_1>..<branch_2> Make sure you have those branches locally
Compare two revision in GitHub UI	https://github.com/…/…/compare/sha1…sha2
Compare latest 3 commits in GitHub UI	https://github.com/dennyzhang/cheatsheet-git-a4/compare/HEAD~3…HEAD


1.6 GIT CONFIG
Name	Comment
Show git config	git config --global/system
Configure default editor	export pager=cat, git config --global core.editor nano
Edit git global config	git config --global --edit
Alias for git status	git config --global alias.st status Link: git aliases
Alias for git checkout	git config --global alias.co checkout
Alias for git commit	git config --global alias.ci commit
Reference	GitHub: gitignore examples

1.7 GIT BRANCH
Name	Comment
List all remote git branches	git ls-remote --heads origin
Delete local branch	git branch -d <branch_name>
Delete remote branch	git push origin --delete <branch_name>

1.8 GIT TAG
Name	Comment
Git list all tags	git ls-remote --tags
Git Fetch all tags	git fetch --tags; git checkout tags/<tag_name>
Git delete local tag	git tag -d <tag_name>
Git delete remote tag	git push --delete origin <tag_name>

1.9 GIT SUBMODULE
Name	Comment
Git add a repo to current repo	git submodule add <git_repo_url>
Update submodule	git submodule update

1.10 GITHUB
Name	Comment
Github Shortcut	Link: Using keyboard shortcuts
Generate TOC	gh-md-toc
Reference	link: generate link for code block, link: git clone wiki repo

1.11 MORE RESOURCES
https://github.com/git-tips/tips
