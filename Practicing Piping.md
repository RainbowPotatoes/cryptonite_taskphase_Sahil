### Redirecting Output
```pwn.college{4yn6UHL82mj7Kx_RKRLfBWELyeX.dRjN1QDL1gTN0czW}```  

the '>' character redirects the output of any command to any file we want.  
```~$ echo PWN > COLLEGE```  
Here we're redirecting the output of 'echo' which is "PWN" to the file 'COLLEGE'. If the file COLLEGE didnt already exist then '>' will create the file  
This command will give us the flag  

### Redirecting more Output
```pwn.college{40ZesCV50pbqGxPUNHG0iEdsqlr.dVjN1QDL1gTN0czW}```

Since we '>' character will redirect the output of any command to any file we can use it to redirect the flag value to a file and then read it from there  
```~$ /challenge/run > myflag```  
This gives an error saying we need to redirect it to the file- '/home/hacker/myflag'
```
~$ /challenge/run > ~/myflag
~$ cat ~/myflag
```
This will give us the output  

### Appending Output
```pwn.college{8ARLEzeMgXwid75RyXZfhRgV3Th.ddDM5QDL1gTN0czW}```

the '>>' character works the same way as the '>' character but it appends the data instead of creating a new output file  
In this challenge the flag has been split into 2 parts and must be added to the 'the-flag' file  
in order to get both the parts without losing the first one, we need to use '>' first followed by '>>'  
```
~$ /challenge/run > ~/the-flag
~$ /challenge/run >> ~/the-flag
```
This gives us the entire flag  

### Redirecting Errors
```pwn.college{gZREdiLPYeRoiqOOKY2i4XicAct.ddjN1QDL1gTN0czW}```

FD describes the communication channel-  
0=stdin   1=stdout   2=stderr  
we can use multiple in the same command  
we need to redirect the output to 'myflag' and rhe errors to 'instructions'  
this will put the flag value in 'myflag' which can then be accessed  
```
~$ /challenge/run >myflag 2>instructions
~$ cat myflag
```  
Will give us the flag  

### Redirecting Input
```pwn.college{Ap16LbNd-QNFKTroFTrg0lafCWa.dBzN1QDL1gTN0czW}```

We need to redirect the PWN file to '/challenge/run' and PWN must contain the value 'COLLEGE'  
first we need to change the value in PWN to COLLEGE and then redirect it into the program  
```
~$ echo COLLEGE > PWN
~$ /challenge/run < PWN
```
This will give us the flag 

### Grepping Stored Results
```pwn.college{4DUIcgVJg_gljT-2O-RGO_oJmKx.dhTM4QDL1gTN0czW}```

In this challenge we need to redirect the output of /challenge/run to /tmp/data.txt and then use 'grep' to find the flag in it  
-grep is a command used for searching and matching text patterns in files contained in the regular expressions, To know more- https://www.geeksforgeeks.org/grep-command-in-unixlinux/  
```
~$ /challenge/run > /tmp/data.txt
~$ grep -i "pwn.college" /tmp/data.txt
```
this grep command searches for the string "pwn.college" in the file and will output the line it is in.  
the '-i' argument enables to search for a string case insensitively in the given file.  
The above commands will give us the flag as the output.

### 
