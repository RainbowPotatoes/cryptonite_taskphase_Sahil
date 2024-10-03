## hidden files
pwn.college{IoPu-ozVmxNOce4b2UVn8gRHAyx.dBTN4QDL1gTN0czW}

the ls command with the '-a' argument shows us all the files (including the hidden files in a directory)

~$ ls -a  /<br>
This shows us that the flag is saved in the '.flag-228627021295' file (hidden files always start with .)

:~$ cat /.flag-228627021295<br>
will give us the flag
