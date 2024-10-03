## linking files

pwn.college{UCmugkNegdH5esZnJFzXKF-HWYa.dlTM1UDL1gTN0czW}

the 'ln' command with the '-s' argument created a symlink of a file

'/challenge/catflag' reads out '/home/hacker/not-the-flag' but we want it to run '/flag' to do this we need to create a symlink of '/flag' with '/home/hacker/not-the-flag' as the address file.<br>
However, running '~$ ln -s /flag /home/hacker/not-the-flag' immediately will give us an error message as that file already exists, hence to make it the symlink we need to delete the file first

~$ rm /home/hacker/not-the-flag<br>
 ln -s /flag /home/hacker/not-the-flag<br>
 We hv now made symlink where '/flag' can be called by using '~/not-the-flag'

'~$ /challenge/catflag' will now run '/flag' and give us the flag as the output
