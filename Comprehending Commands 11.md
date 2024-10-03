## finding files

pwn.college{AkjQ9GAmNHOzSKSTYpeJV35AkhV.dJzM4QDL1gTN0czW}

the 'find' command finds any file in any search location we want. <br>
The '-name' argument is used to specidy that we are searching for a file by its name 

~$ find / -name flag<br>
The above statement is searching for the 'flag' file by its name in the '/' directory

we get an output consisting of multiple files, some of whose permission is denied<br>
if we read out the contents of each permissible file (using cat) one by one we find that the '/usr/lib/jvm/java-11-openjdk-amd64/legal/jdk.zipfs/flag' file gives us the flag
