# Linux Luminarium-File Globbing 

## Matching with *
 using * command.

### Solve
**Flag:** pwn.college{8OfVdC50gi4D7bViXXs0-XssGXK.QXxIDO0wSO4EzNzEzW}

.

```
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run 
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8OfVdC50gi4D7bViXXs0-XssGXK.QXxIDO0wSO4EzNzEzW}

```

### New Learnings
to use * to navigate throuugh directories quicker.

### References 
none.



## Matching with ?
 using ? command.

### Solve
**Flag:** pwn.college{EHpAN7qSUliD__ARsOVdwnzaFA4.QXyIDO0wSO4EzNzEzW}

used cd command but replace c and l with ? w=to succefully get into the directory and get the flag.

```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?hallenge
You used either the 'c', 'l', or '*' characters. Disallowed!
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EHpAN7qSUliD__ARsOVdwnzaFA4.QXyIDO0wSO4EzNzEzW}

```

### New Learnings
to use ? while navigating through directories.

### References 
none.


## Matching with []
 using [] command.

### Solve
**Flag:** pwn.college{I805cdtSw8euxHZofbDdfTBHbov.QXzIDO0wSO4EzNzEzW}

got into chalenge/files directory normally and then ran /challenge/run file[bash] to open all the files with b,a,s,h at the end and got the flag successfully.

```
hacker@globbing~matching-with-:~$ cd /challenge/files/
hacker@globbing~matching-with-:/challenge/files$ /challenge/run 
Error: you did not use a square bracket glob...
hacker@globbing~matching-with-:/challenge/files$ /challenge/[run]
bash: /challenge/[run]: No such file or directory
hacker@globbing~matching-with-:/challenge/files$ /challenge/ru[n]
Your expansion did not expand to the requested files (file_a, file_b, file_h, 
and file_s). Instead, it expanded to:

hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/files/file_[bash]
hacker@globbing~matching-with-:/challenge/files$ /challenge/run 
Error: you did not use a square bracket glob...
hacker@globbing~matching-with-:/challenge/files$ /challenge/ru[n]
Your expansion did not expand to the requested files (file_a, file_b, file_h, 
and file_s). Instead, it expanded to:

hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{I805cdtSw8euxHZofbDdfTBHbov.QXzIDO0wSO4EzNzEzW}
```

### New Learnings
to use [] while navigating through directories.

### References 
none.


## Matching paths with []
   using [] with path as argument.

### Solve
**Flag:** pwn.college{EPXgpCjLzbcAMdouXdraLihf0jP.QX0IDO0wSO4EzNzEzW}

found the files in /challenge/files and then used /challenge/run /challenge/files/file_[bash] using path as the argument to glob the files and get the flag successfully.

```
hacker@globbing~matching-paths-with-:~$ /challenge/run file_[bash]
Error: you will need to specify the path to the files as part of your glob 
argument, since they are in a different directory than your current working 
directory!
hacker@globbing~matching-paths-with-:~$ /challenge/run /home/hacker/file_[bash]
Error: you will need to specify the path to the files as part of your glob 
argument, since they are in a different directory than your current working 
directory!
hacker@globbing~matching-paths-with-:~$ ls /challenge/
DESCRIPTION.md  files  run
hacker@globbing~matching-paths-with-:~$ ls /challenge/files/
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{EPXgpCjLzbcAMdouXdraLihf0jP.QX0IDO0wSO4EzNzEzW}

```

### New Learnings
to use [] and path as the argument.

### References 
none.


## Multiple Globs
 using multiple glob com.

### Solve
**Flag:** pwn.college{wQN1M1NIjcZk1xsRbyOD-mNFrn7.0lM3kjNxwSO4EzNzEzW}

got into challenge/files directory normally run /challenge/run with *p* as argument to run all files .

```
hacker@globbing~multiple-globs:~$ cd /challenge/files/
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run /*p*
Error: your argument is too long! It must be 3 characters or less.
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{wQN1M1NIjcZk1xsRbyOD-mNFrn7.0lM3kjNxwSO4EzNzEzW}
```

### New Learnings
how multiple globbing works and the process behind it, here the '*' before p fills the letters before the letter p in the file and the '*' after p fills all the letter afters so therefore all the files with the letter p are mentioned.

### References 
none.



## Mixing Globs
 using multiple glob com.

### Solve
**Flag:** pwn.college{wQN1M1NIjcZk1xsRbyOD-mNFrn7.0lM3kjNxwSO4EzNzEzW}

got into challenge/files directory normally run /challenge/run with *p* as argument to run all files .

```
hacker@globbing~multiple-globs:~$ cd /challenge/files/
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run /*p*
Error: your argument is too long! It must be 3 characters or less.
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{wQN1M1NIjcZk1xsRbyOD-mNFrn7.0lM3kjNxwSO4EzNzEzW}
```

### New Learnings
how multiple globbing works and the process behind it, here the '*' before p fills the letters before the letter p in the file and the '*' after p fills all the letter afters so therefore all the files with the letter p are mentioned.

### References 
none.

