# Homework



---

## 1. Initial Commits (Unclear Messages)

```
a27c2c5 (HEAD -> master) final version
00268c7 stuff
91adc69 update
bb6bd26 add project.txt
```
---

## 2. Squashing the Commits

```
pick 91adc69 update
squash 00268c7 stuff
squash a27c2c5 final version
```

---

## 3. Commits After Squashing

```
038ae5b (HEAD -> master) initial project setup and content (renamed from update)
bb6bd26 add project.txt
```


---

## 4. Adding a Mistake Commit

```
ba44cad (HEAD -> master) this is a mistake
038ae5b initial project setup and content
bb6bd26 add project.txt
```

---

## 5. Commits After Resetting from the Mistake

The mistaken commit was removed using:

```
git reset --hard HEAD~1
```

Result:

```
038ae5b (HEAD -> master) initial project setup and content
bb6bd26 add project.txt
```

---

## 6. Git Reflog

The lost commit can still be found using `git reflog`.

```
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
```

---

## 7. Recovering the Lost Commit

The lost commit was recovered by checking it out and creating a new branch.

```
git checkout ba44cad
git checkout -b recovered-work
```

Current branches:

```
 master
* recovered-work
```

---

## 8. Git Alias for Logging

A custom Git alias was created to simplify viewing commit history.

```
git config --global alias.l "log --oneline"
```

Now commit history can be viewed using:

```
git l
```

---

## 9. Tagging Version 1.0

The cleaned project version was tagged as:

```
git tag v1.0
```

---


