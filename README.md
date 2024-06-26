# Using-Linux-commands-to-manage-file-permissions
Welcome to the Linux File Permissions Management GitHub repository! This repository is a robust resource crafted to serve as both a practical guide and a detailed reference for managing file permissions using Linux commands. 

## Objective
The primary objective of this lab is to show that I have the practical skills and theoretical knowledge required to effectively manage file permissions in a Linux environment. I can understand, apply, and manipulate Linux file permission settings using command-line tools, ensuring secure and efficient access control for files and directories.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.
- Understanding Linux File Permissions: Gain a fundamental understanding of how Linux handles file permissions, including the roles of different permission types (read, write, execute) and the implications for users and groups.
- Using chmod: Master the use of the chmod command to modify file access permissions using both symbolic (e.g., rwx) and numeric (e.g., 755) notation.
- Applying chown and chgrp: Learn to change file ownership with chown and modify group associations with files and directories using chgrp, crucial for managing user access on multi-user systems.
- Practicing Secure Permission Settings: Develop the ability to set permissions that balance operational functionality with security needs, minimizing the risk of unauthorized access.
- Troubleshooting Permission Issues: Enhance problem-solving abilities by diagnosing and resolving issues related to incorrect file permissions that could impact system functionality or security.
- Command-Line Proficiency: Improve overall command-line interface (CLI) skills which are invaluable for any professional working in Linux or Unix-like environments.

### Tools Used

- Command line interface

### Lab Exercise

Check file and directory details
In this task, we will explore the permissions of the projects directory and the files it contains.The lab starts with /home/researcher2 as the current working directory. This is because you're changing permissions for files and directories belonging to the researcher2 user. 
Steps:
1. Navigate to the `projects` directory.

The command to complete this step:

`cd projects`

2. List the contents and permissions of the `projects` directory.

The command to complete this step:

`ls -l`

The permissions of the files in the `projects` directory are as follows:

`total 20
drwx--x--- 2 researcher2 research_team 4096 Oct 14 18:40 drafts
-rw-rw-rw- 1 researcher2 research_team   46 Oct 14 18:40 project_k.txt
-rw-r----- 1 researcher2 research_team   46 Oct 14 18:40 project_m.txt
-rw-rw-r-- 1 researcher2 research_team   46 Oct 14 18:40 project_r.txt
-rw-rw-r-- 1 researcher2 research_team   46 Oct 14 18:40 project_t.txt`

3. Check whether any hidden files exist in the `projects` directory.

The command to complete this step:

`ls -la`

![Screenshot (165) revised](https://github.com/MaryamUmarShehu/Using-Linux-commands-to-manage-file-permissions/assets/169352998/d6eabbac-7b56-445a-85fa-e0da92c3d740)
The `.project_x.txt` file is hidden  as shown in the screenshot above.



Change file permissions

In this task, you must determine whether any files have incorrect permissions and then change the permissions as needed. This action will remove unauthorized access and strengthen security on the system.

We will chanhing the permissins using the chmod command so that none of the files should allow the other users to write to files.

`chmod o-w project_k.txt`

Using the `chmod` command to change permissions of the `project_m.txt` file so that the group doesn’t have read or write permissions.

`chmod g-r project_m.txt`

![Screenshot (167) revised](https://github.com/MaryamUmarShehu/Using-Linux-commands-to-manage-file-permissions/assets/169352998/7c70c3a8-c50b-448c-b9bc-f664bdbdb784)

# **Change directory permissions**

In this task, you must change the permissions of a directory. 

Only the `researcher2` user should be allowed to access the `drafts` directory and its contents. Remove the execute permission for the group from the `drafts` directory.

The command to complete this step:

`chmod g-x drafts`

![Screenshot (170) revised](https://github.com/MaryamUmarShehu/Using-Linux-commands-to-manage-file-permissions/assets/169352998/65fc9e1d-6709-407b-9e8b-7aade72e9a49)


In conclusion, the lab on "Using Linux Commands to Manage File Permissions" has been a deep dive into the crucial tools and techniques needed to secure and manage file permissions on Linux systems. Through engaging hands-on examples, and practical exercises, I have significantly enhanced my understanding of the Linux file permissions system. More importantly, I've developed valuable skills in using command-line tools to confidently and effectively set and manage these permissions. This experience has not only expanded my knowledge but also equipped me with practical skills that are essential for navigating the complexities of Linux environments.
