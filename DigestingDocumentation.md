# Linux Luminarium- Digesting Documentation

##Learning from Documentation
 using cat command.

### Solve
**Flag:** pwn.college{0LIQTcUKDyGfkxWnA02EXjqmnq8.QX0ITO0wSO4EzNzEzW}

read the documentation and found out to use --giveflag argument in c/challenge/challenge to get the flag.

```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0LIQTcUKDyGfkxWnA02EXjqmnq8.QX0ITO0wSO4EzNzEzW}
```

### New Learnings
 to read documentation.

### References 
none.


##Learning Complex Usage
 

### Solve
**Flag:** pwn.college{0IJJuzztz0nwSYrnapWE0mET1BL.QX1ITO0wSO4EzNzEzW}

read the documentation and found out to use --printflag /flag arguments in /challenge/challenge to get the flag.

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{0IJJuzztz0nwSYrnapWE0mET1BL.QX1ITO0wSO4EzNzEzW}

```

### New Learnings
learnt about programs and its arguments in this type of case.

### References 
google gemini.


##Reading Manuals
 manual pages about commands.

### Solve
**Flag:** pwn.college{4-HVrve0XQ0l7LWJb9X3FJcNC0t.QX0EDO0wSO4EzNzEzW}

use man comand to bring up the manual page for the challenge command, saw a few arguments out of which --rvelbc had a description regarding the flag, executed it properly as said in the manual and obtained the flag.

```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --fortune
Offer limited to residents of the contiguous United States.
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~reading-manuals:~$ man ch
No manual entry for ch
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --rvelbc
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:~$ /challenge/challenge --rvelbc 400
Correct usage! Your flag: pwn.college{4-HVrve0XQ0l7LWJb9X3FJcNC0t.QX0EDO0wSO4EzNzEzW}
```

### New Learnings
to read the manual pages of commands and learnt mroe about executing programs and its arguments.

### References 
none.



##Searching Manuals
  commands to navigate through manual pages.

### Solve
**Flag:** pwn.college{wFAoQ3OssI1iCJ8OCnTs3idmbSn.QX1EDO0wSO4EzNzEzW}

use man comand to bring up the manual page for the challenge command, searched for the keyword: flag using '/' and then navigated through the manual page using n and shift n (N) till i found it .

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --uokkts
Initializing...
Correct usage! Your flag: pwn.college{wFAoQ3OssI1iCJ8OCnTs3idmbSn.QX1EDO0wSO4EzNzEzW}
```

### New Learnings
learnt to navigate through the manual pages quickly using n and N and / and ?.

### References 
none.


##Searching For Manuals
  commands to search for manual pages.

### Solve
**Flag:** pwn.college{gvhFatYYfemcqTocqZlFQ3x1MjM.QX2EDO0wSO4EzNzEzW}

use man comand to bring up the manual page for the challenge command, searched for the keyword: flag using '/' and then navigated through the manual page using n and shift n (N) till i found it .

```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
gvhatfemcq (1)       - print the flag!
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity ...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of vali...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags
hacker@man~searching-for-manuals:~$ man gvhatfemcq
hacker@man~searching-for-manuals:~$ /challenge/challenge --gvhatf 312
Correct usage! Your flag: pwn.college{gvhFatYYfemcqTocqZlFQ3x1MjM.QX2EDO0wSO4EzNzEzW}
```

### New Learnings
learnt to navigate through the manual pages quickly using n and N and / and ?.

### References 
none.


##Helpful Programs
  special argument for programs without man pages.

### Solve
**Flag:** pwn.college{EXuX-ZmvZYTb0KWB1b1Wzu8uy1m.QX3IDO0wSO4EzNzEzW}

use speciala rgyment --help for the program /challenge/challenge/ to get help page where it describes what arguments to use in order to obtain the flag, here i have to use an argument to print a value which ill have to use in another argument to get the flag .

```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --print-value
The secret value is: 11
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG 11
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag 11
Correct usage! Your flag: pwn.college{EXuX-ZmvZYTb0KWB1b1Wzu8uy1m.QX3IDO0wSO4EzNzEzW}
```

### New Learnings
learnt about special argyment --help which i can use for programs without man pages.

### References 
none.


##Help for Builtins
  builtin commands and how the shell handles them.

### Solve
**Flag:** pwn.college{YfR_UhyPcrB7uMVb_ZPpe5i_4hO.QX0ETO0wSO4EzNzEzW}

use builtin command help on bultin challenge to get information regarding obtaining the flag, using the information we use builtin command challenge and -secret argument with that attatched with second argument of the code needed to obtain the flag.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "YfR_UhyP".
hacker@man~help-for-builtins:~$ --secret YfR_UhyP
bash: --secret: command not found
hacker@man~help-for-builtins:~$ /challenge/ --secret YfR_UhyP
bash: /challenge/: Is a directory
hacker@man~help-for-builtins:~$ SECRET YfR_UhyP
bash: SECRET: command not found
hacker@man~help-for-builtins:~$ /SECRET YfR_UhyP
bash: /SECRET: No such file or directory
hacker@man~help-for-builtins:~$ challenge --secret YfR_UhyP
Correct! Here is your flag!
pwn.college{YfR_UhyPcrB7uMVb_ZPpe5i_4hO.QX0ETO0wSO4EzNzEzW}
```

### New Learnings
learnt differences between how programs and shell builtin commands are executed and the information of builtin commaands.

### References 
none.
