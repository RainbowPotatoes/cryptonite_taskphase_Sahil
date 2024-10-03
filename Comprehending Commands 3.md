## more catting practice
pwn.college{EKDTOy4oIHGQqllZqwwmKEYJ1a3.dBjM5QDL1gTN0czW}

In this challenge we cant use the 'cd' command and can only use the 'cat' command with the absolute path of the 'flag' file, however we dont know the absolute path of the 'flag' file<br>
if we run- 'cd /' then we get an error message saying:

--- you MUST chase pass 'cat' the absolute path of where I put it on the<br>
filesystem (which is /usr/share/apache2/flag).<br>
hacker@commands~more-catting-practice:

Hence we now have the absolute path of the 'flag' file and running-<br>
~$ cat /usr/share/apache2/flag      will give us the flag<br>
