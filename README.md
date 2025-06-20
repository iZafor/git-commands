> **Initialize a Repository**
```bash
git init
```

---

> **Rename a Branch**
```bash
git branch -m <new-name>
```
or,
```bash
git branch -M <new-name>
```

---

> **Delete a Branch**
```bash
git branch -d <branch-name>
```
or,
```bash
git branch -D <branch-name>
```
---

>**Start Tracking of a File**
```bash
git add <file-path>
```

---

>**Restore Deleted Tracked Files**
```bash
git restore <file-path>
```
---

>**Remove File from Index**
```bash
git restore --staged <file-path>
```

---

>**Commit Changes**
```bash
git commit -m <commit-message>
```

---

>**Reset Commits**
* The `--soft` option is useful if you just want to go back to a previous commit, but keep all of your changes. Committed changes will be uncommitted and staged, while uncommitted changes will remain staged or unstaged as before.
	```bash
	git reset --soft <hash>
	```
* The `--hard` removes everything from the index and committed changes.   
	```bash
	git reset --hard <hash>
	```

---

>**Revert Changes of a Commit**
```bash
git revert <hash>
```

---

>**Merge Branches**
```bash
git merge <source-branch>
```

> **Handle Merge Conflict**

* Keep changes only from the `current/target` branch
	```bash
	git checkout --ours <file-path>
	```  
* Keep changes only from the `source` branch
	```bash
	git checkout --theirs <file-path>
	```  
* Or manually make the changes and remove 
`<<<<<<< HEAD`
.
.
`=======`
.
.
`>>>>>>> <source-branch>` 
* Stage all the changes
	```bash
	git add .
	```
* Commit the changes
	```bash
	git commit -m <commit-message>
	```
