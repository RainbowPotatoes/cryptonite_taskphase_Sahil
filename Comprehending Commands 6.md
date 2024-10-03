## touching files
pwn.college{QKG3XGNjpNfNBQtEuYfr-3MmOsj.dBzM4QDL1gTN0czW}

the 'touch' command creates an empty file at the specified location.<br>
According to the question we need to create the file at two locations and then run '/challenge/run'

~$ touch /tmp/pwn
~$ touch /tmp/college
~$ /challenge/run<br>
will give us the flag
