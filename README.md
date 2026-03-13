======These are the first commits (Unclear messages) ======
a27c2c5 (HEAD -> master) final version
00268c7 stuff
91adc69 update
bb6bd26 add project.txt

====== Squashing the commits ======
pick 91adc69 update
squash 00268c7 stuff
squash a27c2c5 final version

====== Commits after squashing ======
038ae5b (HEAD -> master) initial project setup and content (renamed from update)
bb6bd26 add project.txt

====== Adding mistake commit ======
ba44cad (HEAD -> master) this is a mistake
038ae5b initial project setup and content
bb6bd26 add project.txt

====== Commits after resetting from the mistake ======
038ae5b (HEAD -> master) initial project setup and content
bb6bd26 add project.txt

====== This is the reflog ======
038ae5b (HEAD -> master) HEAD@{0}: reset: moving to HEAD~1
ba44cad HEAD@{1}: commit: this is a mistake
038ae5b (HEAD -> master) HEAD@{2}: rebase (finish): returning to refs/heads/master
038ae5b (HEAD -> master) HEAD@{3}: rebase (squash): initial project setup and content
f4d2ba9 HEAD@{4}: rebase (squash): # This is a combination of 2 commits.
91adc69 HEAD@{5}: rebase (start): checkout HEAD~3
a27c2c5 HEAD@{6}: commit: final version
00268c7 HEAD@{7}: commit: stuff
91adc69 HEAD@{8}: commit: update
bb6bd26 HEAD@{9}: commit (initial): add project.txt

====== These are the branches after switching to the mistake commit and creating the "recovered-work" branch ======
 master
* recovered-work

====== this is the alias for logging ======
git config --global alias.l "log --oneline"
