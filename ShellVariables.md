# Linux Luminarium-Shell Variables

## Printing Varables
 printing a variable.

### Solve
**Flag:** pwn.college{gwiGRMhHpfLqfYhH3U2F8ak1Bhz.QX3UTN0wSO4EzNzEzW}

used echo to print out the variable FLAG by prepending the varibale with $.

```
hacker@variables~printing-variables:~$ echo !FLAG
bash: !FLAG: event not found
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{gwiGRMhHpfLqfYhH3U2F8ak1Bhz.QX3UTN0wSO4EzNzEzW}

```

### New Learnings
to print out a variable and that prepending a variable with $ will substitute its name with the stores value.

### References 
none.


## Setting Varables
 storing value into a variable.

### Solve
**Flag:** pwn.college{0IzGuoG3eduT1ivfpSabv_WR_Yf.QX5UTN0wSO4EzNzEzW}

typed in the variable name paired with = and the value ( with no spaces in between).

```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0IzGuoG3eduT1ivfpSabv_WR_Yf.QX5UTN0wSO4EzNzEzW}

```

### New Learnings
to store value into a variable.

### References 
none.


## Multi-word Variables
 storing values with spaces into a variable.

### Solve
**Flag:** pwn.college{4bK8Xtd8MP3E5qPypr3kEPP6eHT.QXwYTN0wSO4EzNzEzW}

typed in the variable name paired with = the value with spaces within double quotes, ( no space between the = and the first ").

```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4bK8Xtd8MP3E5qPypr3kEPP6eHT.QXwYTN0wSO4EzNzEzW}

```

### New Learnings
to store values with spaces between them into a variable.

### References 
none.


## Exporting a Variable
exporting variables.

### Solve
**Flag:** pwn.college{wgdqMu5UmYohEkEtr1Y_j3lBV1P.QXyYTN0wSO4EzNzEzW}

used export command before inputting value into PWN variable and inputted value like normal into the COLLEGE varibale and ran the run program to get the flag.

```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run 
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{wgdqMu5UmYohEkEtr1Y_j3lBV1P.QXyYTN0wSO4EzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!

```

### New Learnings
to store export variales to other processes and child shells.

### References 
none.


## Printing Exported Variables
 

### Solve
**Flag:** pwn.college{A1mH1ZIu76IUkAaxanXgSGLgeU6.QX4UTN0wSO4EzNzEzW}

used env command to give out a list of all the variables and its values stored in that shell and found the variable which has the flag stored in it.

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=5507953c09a3a84c7d3b2ea27b72c39fb358d979de74871ecc43620564ed88cc
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{A1mH1ZIu76IUkAaxanXgSGLgeU6.QX4UTN0wSO4EzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env

```

### New Learnings
found another way to print flags given it is exported to the shell.

### References
none.


## Storing Command Outputs
 storing outputs of commands into a variable.

### Solve
**Flag:** pwn.college{sTFy-3P8-tQX6Wi6z3cyihbu3QT.QX1cDN1wSO4EzNzEzW}

typed in the variable name paired with = then the command whose output needs to be assingned within brackets, adn the whole thing prepended by $,
after that since the value is stored printed out the variable using echo to get the flag.

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run )
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{sTFy-3P8-tQX6Wi6z3cyihbu3QT.QX1cDN1wSO4EzNzEzW}

```

### New Learnings
to store command outputs into a variable.

### References 
none.


## Reading Inputs
 getting inputs and storing them into variables.

### Solve
**Flag:** pwn.college{4y2Jp01voFiQ5KUNqSCUA3WN_iV.QX4cTN0wSO4EzNzEzW}

used read command with the variable name as the argument, recieved input from keyboard which unlocked the flag.

```
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4y2Jp01voFiQ5KUNqSCUA3WN_iV.QX4cTN0wSO4EzNzEzW}

```

### New Learnings
to store user inputs into the variable.

### References 
none.


## Reading Files
reading files through variables.

### Solve
**Flag:** pwn.college{c3ccXonVXyjuh-ELzmTVD2X2y9S.QXwIDO0wSO4EzNzEzW}

used read command with the variable name as the argument and < and the file so the value of the file is stored into the variable and can be printed to get the flag.

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{c3ccXonVXyjuh-ELzmTVD2X2y9S.QXwIDO0wSO4EzNzEzW}

```

### New Learnings
to store file values into variables to prevent using cat.

### References 
none.
