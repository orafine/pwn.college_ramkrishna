# Linux Luminarium-Pondering Paths

## Cat Command
 using cat command.

### Solve
**Flag:** pwn.college{IXG9dECKrvYg_3p7Ck34WAWP1gl.QXxcTN0wSO4EzNzEzW}

using cat command and flag as argument to read the content of the flag file and get the flag.

```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat falg
cat: falg: No such file or directory
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{IXG9dECKrvYg_3p7Ck34WAWP1gl.QXxcTN0wSO4EzNzEzW}

```

### New Learnings
 learnt function of cat command.

### References 
none.



## Catting Absolute Paths
 using cat command with absolute path as argument

### Solve
**Flag:** pwn.college{ADw5s7HyGZG-I-Gn3bJj29GPbxm.QX5ETO0wSO4EzNzEzW}

using cat command and /flag as argument to read the content of the flag file and get the flag.

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{ADw5s7HyGZG-I-Gn3bJj29GPbxm.QX5ETO0wSO4EzNzEzW}

```

### New Learnings
 learnt to cat abosolute paths.

### References 
none.


## More Catting Practice
 using cat command with absolute path as argument

### Solve
**Flag:** pwn.college{csCdiXEX3vUn74_bPMbPdqCBPdU.QXwITO0wSO4EzNzEzW}

using cat command and the specified directory as argument to read the content of the flag file and get the flag.

```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/local/include/flag. Go cat it out **without** cding into that 
directory!
hacker@commands~more-catting-practice:~$ cat /usr/local/include/flag
pwn.college{csCdiXEX3vUn74_bPMbPdqCBPdU.QXwITO0wSO4EzNzEzW}

```

### New Learnings
 nothing new, more comfotable with catting absolute paths.

### References 
none.


## Grepping practice
 using grep command with absolute path to get data we specifically want

### Solve
**Flag:** pwn.college{Ya4ZW4Rup0A93b8FkntUoCrvIcK.QX3EDO0wSO4EzNzEzW}

using grep command and the specified directory as argument to read the content of the  text file to get the specified line where it contains the flag.

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt 
pwn.college{Ya4ZW4Rup0A93b8FkntUoCrvIcK.QX3EDO0wSO4EzNzEzW}
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ 


```

### New Learnings
 learnt to use grep command and more comfortable with commands now.

### References 
none.


## Comparing Files
 learn importance of diff command

### Solve
**Flag:** pwn.college{QSk65OyEqXfjYSWv3B4qAhyJ2G7.01MwMDOxwSO4EzNzEzW}

used diff command with the two files, one decoy and the other real to find the difference in text between them. Found the additional text containing the real flag.

```
hacker@commands~comparing-files:~$ cd /challenge/
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt 
93a94
> pwn.college{QSk65OyEqXfjYSWv3B4qAhyJ2G7.01MwMDOxwSO4EzNzEzW}
hacker@commands~comparing-files:/challenge$ 


```

### New Learnings
the diff command and its importance in finding exactly what you want, using absolute paths while using diff commands as arguments,
meaning of 'c' and 'a'. here in this problem, it says after the 93rd line theres another 94th line containing the real flag.

### References 
none.


## Listing Files
 learn importance of ls command

### Solve
**Flag:** pwn.college{EkCOL5aaga9eARPVZFOrE5vEB_d.QX4IDO0wSO4EzNzEzW}

used ls command in the challenge directory to find the renamed run file then use ' ./ run-file ' to run the file within the challenge directory to get the flag.

```
hacker@commands~listing-files:~$ cd /challenge/
hacker@commands~listing-files:/challenge$ ls
23285-renamed-run-17437  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ ./
.init                    23285-renamed-run-17437  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ ./23285-renamed-run-17437 
Yahaha, you found me! Here is your flag:
pwn.college{EkCOL5aaga9eARPVZFOrE5vEB_d.QX4IDO0wSO4EzNzEzW}


```

### New Learnings
learnt importance of ls command, got more confident with using '.' command since i needed it to run the new file from the challenge directory itself.

### References 
none.


## Touching Files
 learn importance of touch command

### Solve
**Flag:** pwn.college{camQhzaTMzcEAN8BS4ZQxyLvBcv.QXwMDO0wSO4EzNzEzW}

made tmp file in home directory, got into it and created two files using touch command called pwn and college and then ran /challenge/run to ge the flag.

```
hacker@commands~touching-files:~$ ls
Desktop  f
hacker@commands~touching-files:~$ touch tmp
hacker@commands~touching-files:~$ /tmp/
bash: /tmp/: Is a directory
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ cd /pwn
bash: cd: /pwn: No such file or directory
hacker@commands~touching-files:/tmp$ /pwn
bash: /pwn: No such file or directory
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ cd /challenge/run
bash: cd: /challenge/run: Not a directory
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{camQhzaTMzcEAN8BS4ZQxyLvBcv.QXwMDO0wSO4EzNzEzW}

```

### New Learnings
learnt importance of touch command, learnt how to create files in directories.

### References 
none.


## Removing Files
 learn importance of rm command

### Solve
**Flag:** pwn.college{Iz-tg8pWf7OWQ_dfKui4eeSn4H0.QX2kDM1wSO4EzNzEzW}

using ls to see all the files in home directory and deleted the required file using rm command and then ran /challenge/check to get the flag.

```
hacker@commands~removing-files:~$ ls
Desktop  delete_me  f  tmp
hacker@commands~removing-files:~$ rm delete_me d
rm: cannot remove 'd': No such file or directory
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{Iz-tg8pWf7OWQ_dfKui4eeSn4H0.QX2kDM1wSO4EzNzEzW}
```

### New Learnings
learnt importance of rm command, learnt how to remove unnecessary files and found out we could delete multiple files by adding multiple arguments which i wasnt sure about before.

### References 
none.


## Moving Files
 learn importance of mv command

### Solve
**Flag:** pwn.college{kf0Qax5DjJ33M8BuIljfeyJ8YsH.0VOxEzNxwSO4EzNzEzW}

used mv command to move flag into speciifed directory and ran /challenge/check for it to be checked and recieved the flag.

```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet 
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
/bin/mv: cannot stat '/flag': No such file or directory
hacker@commands~moving-files:~$ /challenge/check 
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{kf0Qax5DjJ33M8BuIljfeyJ8YsH.0VOxEzNxwSO4EzNzEzW}
```

### New Learnings
learnt importance of mv command, learnt how to move files from differenet paths.

### References 
none.


## Hidden Files
 how to find the hidden files in a directory.

### Solve
**Flag:** pwn.college{Y_uw2Z8mMhRrMZNpVOKeU4SLyWQ.QXwUDO0wSO4EzNzEzW}

went into / directory and used ls -a to list all the hidden files as well, finding the flag file and read it out using cat.

```
hacker@commands~hidden-files:~$ ls -a
.  ..  .ICEauthority  .bash_history  .cache  .config  .dbus  .local  Desktop  f  tmp
hacker@commands~hidden-files:~$ cd /local
bash: cd: /local: No such file or directory
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-13552311569742  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-13552311569742 
pwn.college{Y_uw2Z8mMhRrMZNpVOKeU4SLyWQ.QXwUDO0wSO4EzNzEzW}
```

### New Learnings
learnt how to find hidden files in directories.

### References 
none.


## Epic Filesystem Quest
 using all the knowledge from previous tasks.

### Solve
**Flag:**  pwn.college{w5o5oMFfjwFIadf1vELwY2AWbBr.QX5IDO0wSO4EzNzEzW}

used all the previous knowledge to navigate through all the directories, for example used 'ls -a' to find hidden files clues, skipped using cd and used ls with path as argument to prevent getting into the directory to find files and used cat and path as argument to read files without entering into its directory.

```
hacker@commands~an-epic-filesystem-quest:~$ ls 
Desktop  f  tmp
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INFO  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat INFO
Tubular find!
The next clue is in: /usr/lib/ruby/2.7.0/ostruct

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/ruby/2.7.0/ostruct
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ ls
TIP  version.rb
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ cat TIP
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/STIX/SizeTwoSym/Bold

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ cat /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/STIX/SizeTwoSym/Bold/TEASER-TRAPPED 
Congratulations, you found the clue!
The next clue is in: /usr/lib/R/library/utils/Sweave

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ ls -a /usr/lib/R/lib
lib/     library/ 
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ ls -a /usr/lib/R/library/utils/Sweave/
.  ..  .NOTE  Sweave-test-1.Rnw  example-1.Rnw
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ cat /usr/lib/R/library/utils/Sweave/.NOTE 
Congratulations, you found the clue!
The next clue is in: /usr/share/doc/libdrm-radeon1

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/ostruct$ cd /usr/share/doc/libdrm-radeon1/
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a
.  ..  SECRET  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat SECRET 
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/DoubleStruck/Regular

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Lat
in-Modern/DoubleStruck/Regular/
.  ..  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Latin
-Modern/DoubleStruck/Regular/Main.js 
/*************************************************************
 *
 *  MathJax/jax/output/HTML-CSS/fonts/Latin-Modern/DoubleStruck/Regular/Main.js
 *  
 *  Copyright (c) 2013-2018 The MathJax Consortium
 *
 *  Licensed under the Apache License, Version 2.0 (the "License");
 *  you may not use this file except in compliance with the License.
 *  You may obtain a copy of the License at
 *
 *     http://www.apache.org/licenses/LICENSE-2.0
 *
 *  Unless required by applicable law or agreed to in writing, software
 *  distributed under the License is distributed on an "AS IS" BASIS,
 *  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 *  See the License for the specific language governing permissions and
 *  limitations under the License.
 */

MathJax.OutputJax['HTML-CSS'].FONTDATA.FONTS['LatinModernMathJax_DoubleStruck'] = {
  directory: 'DoubleStruck/Regular',
  family: 'LatinModernMathJax_DoubleStruck',
  testString: '\u00A0\u2102\u210D\u2115\u2119\u211A\u211D\u2124\u213C\u213D\u213E\u213F\u2140\u2145\u2146',
  0x20: [0,0,332,0,0],
  0xA0: [0,0,332,0,0],
  0x2102: [705,22,667,55,611],
  0x210D: [683,0,722,83,639],
  0x2115: [683,0,722,83,639],
  0x2119: [683,0,639,83,583],
  0x211A: [705,194,667,55,611],
  0x211D: [683,0,639,83,583],
  0x2124: [683,0,667,55,611],
  0x213C: [431,0,517,27,488],
  0x213D: [431,216,472,27,444],
  0x213E: [683,0,611,83,583],
  0x213F: [683,0,667,83,583],
  0x2140: [683,0,667,55,611],
  0x2145: [683,0,694,47,680],
  0x2146: [694,22,500,26,547],
  0x2147: [453,22,472,26,460],
  0x2148: [691,0,279,19,331],
  0x2149: [691,216,389,-69,441],
  0x1D538: [683,0,611,27,583],
  0x1D539: [683,0,639,83,583],
  0x1D53B: [683,0,694,83,639],
  0x1D53C: [683,0,611,83,583],
  0x1D53D: [683,0,611,83,583],
  0x1D53E: [705,22,667,55,611],
  0x1D540: [683,0,334,83,251],
  0x1D541: [683,22,639,55,555],
  0x1D542: [683,0,639,83,583],
  0x1D543: [683,0,611,83,583],
  0x1D544: [683,0,722,83,639],
  0x1D546: [705,22,667,55,611],
  0x1D54A: [705,22,611,55,555],
  0x1D54B: [683,0,611,27,583],
  0x1D54C: [683,22,722,83,639],
  0x1D54D: [683,0,611,27,583],
  0x1D54E: [683,0,833,27,805],
  0x1D54F: [683,0,667,55,611],
  0x1D550: [683,0,611,27,583],
  0x1D552: [453,22,500,27,444],
  0x1D553: [694,22,628,55,599],
  0x1D554: [453,22,472,27,444],
  0x1D555: [694,22,500,27,444],
  0x1D556: [453,22,472,27,444],
  0x1D557: [716,0,389,55,388],
  0x1D558: [453,216,500,27,444],
  0x1D559: [694,0,572,55,516],
  0x1D55A: [691,0,279,33,245],
  0x1D55B: [691,216,389,0,355],
  0x1D55C: [694,0,544,55,516],
  0x1D55D: [694,0,279,55,223],
  0x1D55E: [453,0,722,55,667],
  0x1D55F: [453,0,572,55,516],
  0x1D560: [453,22,472,27,444],
  0x1D561: [453,194,628,55,599],
  0x1D562: [453,194,500,27,444],
  0x1D563: [453,0,544,55,516],
  0x1D564: [453,22,389,27,360],
  0x1D565: [694,22,417,55,388],
  0x1D566: [431,22,528,55,472],
  0x1D567: [431,0,472,27,443],
  0x1D568: [431,0,667,27,639],
  0x1D569: [431,0,472,27,444],
  0x1D56A: [431,216,472,27,443],
  0x1D56B: [431,0,472,27,444],
  0x1D7D8: [666,22,556,55,499],
  0x1D7D9: [644,0,556,55,499],
  0x1D7DA: [666,0,556,55,499],
  0x1D7DB: [666,22,556,55,499],
  0x1D7DC: [644,0,556,55,499],
  0x1D7DD: [644,22,556,55,499],
  0x1D7DE: [666,22,556,55,499],
  0x1D7DF: [644,0,556,55,499],
  0x1D7E0: [666,22,556,55,499],
  0x1D7E1: [666,22,556,55,499]
};

MathJax.Callback.Queue(
  ["initFont",MathJax.OutputJax["HTML-CSS"],"LatinModernMathJax_DoubleStruck"],
  ["loadComplete",MathJax.Ajax,MathJax.OutputJax["HTML-CSS"].fontDir+"/DoubleStruck/Regular/Main.js"]
);
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Latin-Modern/DoubleStruck/Regular/
.  ..  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Latin-
Modern/DoubleStruck/Regular/
Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat SECRET 
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/DoubleStruck/Regular

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/DoubleStruck/Regular/
.  ..  Main.js  SPOILER-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern/D
oubleStruck/Regular/SPOILER-TRAPPED 
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/numpy/core/tests/examples/cython

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /usr/local/lib/python3.8/dist-packages/numpy/co
compat/      conftest.py  core/        
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /usr/local/lib/python3.8/dist-packages/numpy/core/tests/examples/cython/
.  ..  README-TRAPPED  __pycache__  checks.pyx  setup.py
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat /usr/local/lib/python3.8/dist-packages/numpy/core/tests/examples/cytho
n/README-TRAPPED 
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/dce100
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/dce100/
.  ..  Makefile  TRACE  dce100_hw_sequencer.c  dce100_hw_sequencer.h  dce100_resource.c  dce100_resource.h
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/dce100/TRACE 
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/tools/arch/mips/include
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ ls -a /opt/linux/linux-5.4/tools/arch/mips/include/
.  ..  INSIGHT  asm  uapi
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libdrm-radeon1$ cat /opt/linux/linux-5.4/tools/arch/mips/include/INSIGHT 
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{w5o5oMFfjwFIadf1vELwY2AWbBr.QX5IDO0wSO4EzNzEzW}
```

### New Learnings
got very comfortable in navigating through the directories and got comfortable with all the commands.

### References 
none.


## Making Directories
 learn command to make directories

### Solve
**Flag:** pwn.college{oGGxgHZ9a57ZdgNq1Jncbt3GXWo.QXxMDO0wSO4EzNzEzW}

made pwn directory in the tmp directory using mkdir command and entered into it using cd and made college file using touch command.

```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ touch /tmp/pwn college
hacker@commands~making-directories:/tmp$ /challenge/run 
Uh oh! /tmp/pwn/college does not exist. Please use the 'touch' command to 
create it!
hacker@commands~making-directories:/tmp$ touch /tmp/pwn /college
touch: cannot touch '/college': Permission denied
hacker@commands~making-directories:/tmp$ cd /tmp/pwn/
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run 
Success! Here is your flag:
pwn.college{oGGxgHZ9a57ZdgNq1Jncbt3GXWo.QXxMDO0wSO4EzNzEzW}

```

### New Learnings
learnt how to make directories, got more comfortable with touch command.

### References 
none.
