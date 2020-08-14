Checkout the previous branch you were on with

`git checkout -`

Useful for switching between your main branch and your feature branch.

---

Stash only some files with `git stash push filename1 filename2 ...`

---

Delete all your remote-tracking branches that have been deleted at origin.

`git fetch --prune origin`

See all merged branches:

`git branch --merged`

Delete all merged branches that aren't master:

`git branch --merged | egrep -v "(^\*|master)" | xargs git branch -d`

Source = https://stackoverflow.com/questions/6127328/how-can-i-delete-all-git-branches-which-have-been-merged

