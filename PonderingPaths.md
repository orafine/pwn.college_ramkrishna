# Linux Luminarium-Pondering Paths

## The Root
 going through directories.

### Solve
**Flag:** pwn.college{IoZNQCX_zzeZddQq356jZf_Qy-i.QX4cTO0wSO4EzNzEzW}

navigated through the directories using / command and went into pwn program to get the key.

```
hacker@paths~the-root:~$ /pwn 
BOOM!!!
Here is your flag:
pwn.college{IoZNQCX_zzeZddQq356jZf_Qy-i.QX4cTO0wSO4EzNzEzW}

```

### New Learnings
to navigate the directories and use tab button to autofill the names of files present in the directory.

### References 
none.


## Program and Absolute paths
navigate more into directories

### Solve
**Flag:** pwn.college{wIyuJ4PjFZAnr3K4oW-Y46a7BEe.QX1QTN0wSO4EzNzEzW}

navigated through the directories using / command and went into challenge program directory and then into the run program within that.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run 
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{wIyuJ4PjFZAnr3K4oW-Y46a7BEe.QX1QTN0wSO4EzNzEzW}

```

### New Learnings
to navigate the directories more deeply.

### References 
none.


## Position thyself
navigate around diretories using cd command.

### Solve
**Flag:** pwn.college{4cFmkULrXLMTkUXL67qno_Xqx8H.QX2QTN0wSO4EzNzEzW}

navigated through the directories uing cd command and the specific location of /usr/bin as the argument to get into that directory and then ran /challenge/run to successfully run the program and get the key.

```hacker@paths~position-thy-self:~$ cd /challenge/run 
bash: cd: /challenge/run: Not a directory
hacker@paths~position-thy-self:~$ cd
hacker@paths~position-thy-self:~$ /challenge/run 
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd
hacker@paths~position-thy-self:~$ cd /usr
hacker@paths~position-thy-self:/usr$ /bi
bash: /bi: No such file or directory
hacker@paths~position-thy-self:/usr$ /binq
bash: /binq: No such file or directory
hacker@paths~position-thy-self:/usr$ /b
bin/  boot/ 
hacker@paths~position-thy-self:/usr$ /bin
bash: /bin: Is a directory
hacker@paths~position-thy-self:/usr$ cd /bin
hacker@paths~position-thy-self:/bin$ cd /challenge/run 
bash: cd: /challenge/run: Not a directory
hacker@paths~position-thy-self:/bin$ cd /run
hacker@paths~position-thy-self:/run$ f
bash: f: command not found
hacker@paths~position-thy-self:/run$ cd
hacker@paths~position-thy-self:~$ cd /usr/bin
hacker@paths~position-thy-self:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4cFmkULrXLMTkUXL67qno_Xqx8H.QX2QTN0wSO4EzNzEzW}
hacker@paths~position-thy-self:/usr/bin$ 
```

### New Learnings
learnt how the cd command works and to get into directories to open and run the programs you want.

### References 
none.


## Position Elsewhere
navigate more into directories

### Solve
**Flag:** pwn.college{ErMVe7kYkzxJB0UI-DPCERSdgOq.QX3QTN0wSO4EzNzEzW}

navigated through the directories uing cd command and the specific location of /usr/share/doc/fontconfig as the argument to get into that directory and then ran /challenge/run to successfully run the program and get the key.

```
hacker@paths~position-elsewhere:~$ /challenge/run 
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately. 
hacker@paths~position-elsewhere:~$ cd /usr/share/doc/fontconfig
hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$ /challenge/run 
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{ErMVe7kYkzxJB0UI-DPCERSdgOq.QX3QTN0wSO4EzNzEzW}

```

### New Learnings
to navigate the directories more deeply.

### References 
none.


## Implicitive relative paths, from /
learn about relative paths and current working directory

### Solve
**Flag:** pwn.college{Y84OMwrbiQELgpgTxHFyb51X421.QX5QTN0wSO4EzNzEzW}

use cd command and '/' as the argument to make the cwd into '/' and type in challenge/run to open the program.

```
hacker@paths~implicit-relative-paths-from-:~$ cwd
bash: cwd: command not found
hacker@paths~implicit-relative-paths-from-:~$ cwd
bash: cwd: command not found
hacker@paths~implicit-relative-paths-from-:~$ challenge/run
bash: challenge/run: No such file or directory
hacker@paths~implicit-relative-paths-from-:~$ cd
hacker@paths~implicit-relative-paths-from-:~$ cd /challenge/run 
bash: cd: /challenge/run: Not a directory
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Y84OMwrbiQELgpgTxHFyb51X421.QX5QTN0wSO4EzNzEzW}

```

### New Learnings
learnt about current working directory and how to get into it.

### References 
none.


## Explicit Relative Paths, from /
about the 2 implicit directories '.' and '..'

### Solve
**Flag:** pwn.college{4l9KH9jbuNbJqEWS7TR6NdoQ3Rv.QXwUTN0wSO4EzNzEzW}

use cd as command and '/' as argument to get into '/' directory and then used ' ./challenge/run ' to run the program and get the flag successfully .

```
hacker@paths~position-elsewhere:~$ /challenge/run 
hacker@paths~explicit-relative-paths-from-:~$ /challenge/.
bash: /challenge/.: Is a directory
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge/run
Incorrect...
This challenge must be called with a relative path that explicitly starts with a `.`!
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4l9KH9jbuNbJqEWS7TR6NdoQ3Rv.QXwUTN0wSO4EzNzEzW}
```

### New Learnings
to use '.' in my relative paths and its meaning and about the two implicitive directories '.' and '..'
### References 
none.


## implicit relative path
looking and running programs in current directory using '.'

### Solve
**Flag:** pwn.college{YKlcTSurG1L-xu3OnQon5aq4-E6.QXxUTN0wSO4EzNzEzW}


```
hacker@paths~implicit-relative-path:~$ cd /challenge/
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ /./run
bash: /./run: Is a directory
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YKlcTSurG1L-xu3OnQon5aq4-E6.QXxUTN0wSO4EzNzEzW}
```

### New Learnings
to use '.' to execute programs in the current directory.

### References 
none.


## Home Sweet Home
navigating through home directory and '~'

### Solve
**Flag:** pwn.college{of1MCox0OFPOg8KaeB769O1pqOw.QXzMDO0wSO4EzNzEzW}


```
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{of1MCox0OFPOg8KaeB769O1pqOw.QXzMDO0wSO4EzNzEzW}
```

### New Learnings
that '~' expands to home directory and itll only expand if its the leading '~' in the command and running cd alone in the terminal will make you go back to your home directory

### References 
google gemini to learn.
