---
layout: post
title: "gitignore Tricks-1: Don't ignore"
subtitle: Version Control Systems
permalink: /blog/gitignore-tricks-1/
tags: [git, gitignore, version control]
---

### **Introduction**
Git users know that gitignore files plays an important role to manage their source code repository. 

**gitignore files** helps developers to avoid sliding into chaos on their *complex coding environment*.

Ignoring the files below is a good practice to keep your source code repository cleaner:
* IDE configuration/cache files,
* User-specific files,
* Build output files, 
* Auto-generated files,
* Secret/config files,
* Data files,
* Environment-specific files,
* Test result files,
* Dependency packages...

In this post series, some good practices about creating effective gitignore files will be noted into the pages of my personal notepad.

You can find a collection of .gitignore templates on this repository: [https://github.com/github/gitignore](https://github.com/github/gitignore)

## **gitignore Tricks-1: Don't ignore**



- Ignore all txt files, but don't ignore *important.txt*.

```
   *.txt
   !important.txt
```



- Ignore all txt files, but don't ignore .txt files under *important* folder. Note that it ignores *important/trace.txt* file, because last pattern causes to re-ignore previous pattern.

```
   *.txt
   !important/*.txt
   trace.*
```



- Ignore *tasks* folder, also ignore *tasks/important.txt* file. *!* doesn't work for this example. Due to a performance-related quirk in Git, you can not negate a file that is ignored due to a pattern matching a directory

```
tasks/
!tasks/important.txt
```

<br>
