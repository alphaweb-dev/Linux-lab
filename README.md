# 30 Days of Linux, Git and Cloud Administration

## Overview
This repository documents my 30-day journey learning Linux, Git, and Cloud Adminstratio.
It includes daily labs, scripts, and projects that demonstrates my growth and practical skills

## Structure
- **docs/** - Daily notes (day1.md, day2.md, etc.)
- **scripts/** - Bash/Python scripts created along the way
- **labs/** - Hands-on exercises and practice files
- **README.md** - Overview and case studies 

## Case Study 

### Day 3 - File & Folder Management

#### Problem Statement 
In real-world administration, managing files and directories efficiently is critical. 
Tasks such as creating, moving, copying, and deletimg files form the foundation of Linux administration.

#### What I Did
- Created a working directory (`day3_lab`) to simulate a real lab environment.
- Used commands like `mkdir`, `touch`, and `ls`to create and explore files.
- Practiced moving files into folders (`mv`) and copying files aacross directories (`cp`)
- Learned how to safely delete files and directories using `rm`

#### Why It Matters
- File and folder management is a **core skill for every Sysadmin/DevOps engineer**.
- These operations are essential for managing configurations, logs, and project files in real systems.
- Mistakes here can cause data loss, so practicing in labs builds confidence.

#### Key Commands Learned
```bash
mkdir day3_lab
touch file1.txt file2.txt
mv file1.txt folderA/
cp folderA/file1.txt folderB/
rm -r folderA
```

### Day 4 - Searching Files with grep and find

#### Problem Statement
As systems grow larger, searching for specific text or files manually becomes inefficient.  
System administrators need quick ways to locate logs, configuration values, or specific files in huge directories.  

#### What I Did
- Used `grep` to search inside files for specific keywords.  
- Practiced case-insensitive searches using the `-i` option.  
- Numbered search results with `-n` to know the exact line where matches occurred.  
- Used `find` to locate files and directories by name and type.  

#### Why It Matters
- `grep` helps quickly scan configuration files and logs for errors or keywords.  
- `find` is essential for locating files in complex directory structures.  
- Together, they save time and make troubleshooting much faster.  

#### Key Commands Learned
```bash
grep "Linux" mynotes.txt
grep -i "cloud" mynotes.txt
grep -n "Ubuntu" mynotes.txt
find . -name "mynotes.txt"
find ~ -type d -name "day3_lab"
```

### day 5 - Exploring Git Logs & Linux History

#### Problem Statement 
As projects grow, it's important to track changes in Git and also review system history.
Systems admins and Devops engineers often need to investigate **who changed what, when, and why**.

#### What I Did 
- Learned how to view Git commit history using `git log`and `git log --online`.
- Used `git show`to inspect details of a specific commit.
- Compared two commits using `git diff <commit1> <commit2>`.
- Praccticed Linux history commands (`history`, `!!`, `!<number>`).
- Checked logs with `tail`and `less`to monitor system events.

#### Why it Matters 
- Git logs help trace changes, debug issues, and maintain accountability in teams.
- System logs (`syslog`, `auth.log`) are vital for troubleshooting errors, security, and audits.

#### Key Commands Learned
```bash
git log
git log --oneline
git show <commit-id>
git diff <commit-id1> <commit-id2>
history
!!	# repeat last command
!45	# run command #45 from history
tail -n 20 /var/log/syslog
less /var/log/auth.log
```

### Day 6 - Branching and Merging in Git

#### Problem Statement 
In real projects, we can't work directly on the main branch (master/main) all the time.
Developers use branches to add new features without breaking the main codebase.

#### What I did
- Created new branches using `git checkout -b branch-name`.
- Switched between branches with `git checkout branch-name`.
- Merged feature branches back into `master`using `git merge`.
- Practiced pushing branches to GitHub and syncing changes.

#### Why It matters 
- Branching keeps work organized and prevents conflicts.
- Merging allows collaborating and clean integration of features.
- This workflow is the backbone of professional Git usage.

#### Key Commands Learned 
```bash
git checkout -b day6-notes 
git add file.md
git commit -m "Added new notes"
git checkout master 
git merge day6-notes 
git push origin master 
```

### Day 7 - Practice & Keeping a Clean Repo

#### Problem Statement 
Some repositories confuse both developers and recruiters, because of not showing professionalism in organising their Github repos

#### What I Did 
- Practiced creating and deleting branches (`git branch -d`, `git push origin --delete branch`).
- Renamed branches properly (avoiding names like practice.md).
- Wrote meaningful commit messages instead of random notes.
- Learned about structuring repos with folders (`docs/`, `labs/`, `scripts/`).
- Updated README with clear documentation.

#### Why It Matters
- Clean repos will lead to easy collaboration + professionalism.

#### Key commands Learned
```bash
git branch -m Old-name new-name
git branch -d branch-name
git push origin --delete branch-name
mkdir docs labs scripts
echo "# My Project" > README.md
```

