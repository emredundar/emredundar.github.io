---
layout: post
title: 5 Ways of Starting A New Project on TFS 2018 and VSTS
subtitle: Version Control Systems
meta-title: "5 Ways of Starting A New Project on TFS 2018 and VSTS - Emre Dündar"
permalink: /blog/starting-new-project-tfs2018/
tags: [tfs, vsts, version control, en]
---

After creating a new team project on TFS or VSTS, you need to start coding on this project.

There are 5 ways of starting a new coding project on **TFS 2018** and **VSTS**. You can **choose your action depending on your status of project**.

<div style="text-align:left;">
  <a href="https://emredundar.github.io/img/tfs-1.PNG">
    <img src="https://emredundar.github.io/img/tfs-1.PNG" alt="tfs2018" style="width: 1000px;">
  </a>
</div>

<p style="text-align: center;"><i>5 ways of starting a new project</i></p>

  
|   | Status			                                                         | Action						                    					|
| - | -------------------------------------------------------------------- | ---------------------------------------------- |
| 1 | You don't have any code written.                                     | initialize with a README or gitignore			    |
| 2 | You have code on your local machine.                                 | initialize with a README or gitignore			    |
| 3 | You have an existing git repository on your local machine.           | push an existing repository from command line	|
| 4 | You have an existing repository on a different Git repository.       | import a repository							              |
| 5 | You don't want to add any code repository, just need a build system. | build code from an external repository		    	|

<br>
**Close shot: import a repository**

You can import an existing public or private repository (from github, bitbucket, gitlab, tfs...). 
It is possible to import a Git or TFVC source code repository.

<div style="text-align:left;">
  <a href="https://emredundar.github.io/img/tfs-2.PNG">
    <img src="https://emredundar.github.io/img/tfs-2.PNG" alt="tfs2018" style="width: 500px;">
  </a>
</div>
<br>

**Close shot: initialize with a README or gitignore**

If you want to initialize an empty git repository, TFS and VSTS creates a ReadMe and .gitignore file for your repository.

<div style="text-align:left;">
  <a href="https://emredundar.github.io/img/tfs-3.PNG">
    <img src="https://emredundar.github.io/img/tfs-3.PNG" alt="tfs2018" style="width: 500px;">
  </a>
</div>
<br>
