## An Epic Filesystem Quest

pwn.college{corSllxDhVI4xCKImannko7iwbk.dljM4QDL1gTN0czW}

According to the challenge we need to find out the target file using ls, cd, cat<br>

~$ cd /<br>
/$ ls -a -al<br>
We execute the above two commands as we hv been asked to 

we then see a file names BLUEPRINT and so read its contents using '/$ cat BLUEPRINT'<br>
It reads out- <br>
"The next clue is in: /opt/linux/linux-5.4/drivers/staging/iio/adc<br>
Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!"

Since we cant cd into the directory, we do- <br>
/$ ls /opt/linux/linux-5.4/drivers/staging/iio/adc<br>
We can now see a file named 'CUE-TRAPPED' which we can read using '/$ cat /opt/linux/linux-5.4/drivers/staging/iio/adc/CUE-TRAPPED'<br>
this gives us the output-<br>
"The next clue is in: /usr/share/racket/pkgs/unix-socket-lib/racket/private<br>
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'."

Since we need to enter the directory-<br>
/$ cd /usr/share/racket/pkgs/unix-socket-lib/racket/private<br>
/usr/share/racket/pkgs/unix-socket-lib/racket/private$ ls -a -al<br>
We can now see a file named 'TEASER' which we can read using ':/usr/share/racket/pkgs/unix-socket-lib/racket/private$ cat TEASER'<br>
this gives us the output- <br>
"The next clue is in: /usr/share/doc/liblzo2-2<br>
The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'."

/usr/share/racket/pkgs/unix-socket-lib/racket/private$ ls -a -al /usr/share/doc/liblzo2-2<br>
/usr/share/racket/pkgs/unix-socket-lib/racket/private$ cd /usr/share/doc/liblzo2-2<br>
We are now in the directory and can see a hidden file named '.POINTER' which we can read using '/usr/share/doc/liblzo2-2$ cat .POINTER'<br>
this gives us the output-<br>
"The next clue is in: /opt/libslub/.git/objects/f2<br>
Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!"

Since we cant enter the directory-<br>
/usr/share/doc/liblzo2-2$ ls /opt/libslub/.git/objects/f2<br>
we see a file named WHISPER-TRAPPED which we can read by using '/usr/share/doc/liblzo2-2$ cat /opt/libslub/.git/objects/f2/WHISPER-TRAPPED'<br>
this gives the output-<br>
"The next clue is in: /usr/share/icons/Adwaita/64x64/emblems<br>
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'."

Since we hv to enter the directory-<br>
/usr/share/doc/liblzo2-2$ cd /usr/share/icons/Adwaita/64x64/emblems<br>
/usr/share/icons/Adwaita/64x64/emblems$ ls -a -al<br>
we see a file named SECRET which we can read using '/usr/share/icons/Adwaita/64x64/emblems$ cat SECRET'<br>
this gives the output- <br>
"The next clue is in: /opt/ghidra/Ghidra/Debug/Debugger-agent-dbgmodel-traceloader/lib"

/usr/share/icons/Adwaita/64x64/emblems$ ls -a -al /opt/ghidra/Ghidra/Debug/Debugger-agent-dbgmodel-traceloader/lib<br>
we see a file named BRIEF which we can read using- '/usr/share/icons/Adwaita/64x64/emblems$ cat /opt/ghidra/Ghidra/Debug/Debugger-agent-dbgmodel-traceloader/lib/BRIEF'<br>
this gives the output-<br>
"The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/AMS<br>
Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!"

Since we cant enter the directory-<br>
/usr/share/icons/Adwaita/64x64/emblems$ ls -a -al /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/AMS<br>
We see a file named ALERT-TRAPPED which we can read by using- '/usr/share/icons/Adwaita/64x64/emblems$ cat /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/AMS/ALERT-TRAPPED'<br>
this gives the output-<br>
"The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/include/hw/misc/macio"

:/usr/share/icons/Adwaita/64x64/emblems$ ls -a -al /opt/aflplusplus/nyx_mode/QEMU-Nyx/include/hw/misc/macio<br>
we see a file named INFO which we can read by using- '/usr/share/icons/Adwaita/64x64/emblems$ cat  /opt/aflplusplus/nyx_mode/QEMU-Nyx/include/hw/misc/macio/INFO' and this finally gives us the flag.
