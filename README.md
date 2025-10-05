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

