This is a README file that describe what each task does
0-iam_betty
Create a script that switches the current user to the user betty.

    You should use exactly 8 characters for your command (+1 character for the new line)
    You can assume that the user betty will exist when we will run your script

1-who_am_i
Write a script that prints the effective username of the current user.

2-groups
Write a script that prints all the groups the current user is part of.

3-new_owner 
Write a script that changes the owner of the file hello to the user betty.
4-empty
Write a script that creates an empty file called hello.
5-execute
Write a script that adds execute permission to the owner of the file hello.

    The file hello will be in the working directory
6-multiple_permissions
Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

    The file hello will be in the working directory
7-everybody
Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

    The file hello will be in the working directory
    You are not allowed to use commas for this script
8-James_Bond
Write a script that sets the permission to the file hello as follows:

    Owner: no permission at all
    Group: no permission at all
    Other users: all the permissions

The file hello will be in the working directory You are not allowed to use commas for this script

9. John Doe
mandatory

Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

    The file hello will be in the working directory
    You are not allowed to use commas for this script

Repo:

    GitHub repository: alx-system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 9-John_Doe

10. Look in the mirror
mandatory

Write a script that sets the mode of the file hello the same as olleh’s mode.

    The file hello will be in the working directory
    The file olleh will be in the working directory

julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ ./10-mirror_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ 

Note: the mode of olleh will not always be 664. Make sure your script works for any mode.

Repo:

    GitHub repository: alx-system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 10-mirror_permissions

11. Directories
mandatory

Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx------ 2 julien julien 4096 Sep 20 14:49 dir0
drwx------ 2 julien julien 4096 Sep 20 14:49 dir1
drwx------ 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./11-directories_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: alx-system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 11-directories_permissions

12. More directories
mandatory

Create a script that creates a directory called my_dir with permissions 751 in the working directory.

julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./12-directory_permission s
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: alx-system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 12-directory_permissions

13. Change group
mandatory

Write a script that changes the group owner to school for the file hello

    The file hello will be in the working directory

julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./13-change_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien    4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien school   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: alx-system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 13-change_group

Copyright © 2022 ALX, All rights reserved.
