## grepping for a needle in a haystack
pwn.college{AhuGGjnJ2I-MbYhPS_veMi5GSL-.ddTM4QDL1gTN0czW}

since the data.txt file has too many lines of code to use 'cat' we can use 'grep' to only print out the lines of code we need, we can do this is the flag always starts with 'pwn.college'. The absolute path of the 'data' file has been given to us as '/challenge/data.txt'<br>

~$ grep pwn.college /challenge/data.txt<br>
the above statement will give us the flag
