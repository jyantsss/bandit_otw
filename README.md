# Bandit

# Welcome to Over_The_Wire bandit solutions by Jayanti Thakur!

![WelcomeYoureWelcomeGIF.gif](Bandit%205f5d157e4cf142a2b6d87600a78ea65a/WelcomeYoureWelcomeGIF.gif)

# Description:

- This is just a solution bank. To see the question paper for each level visit the site “[https://overthewire.org/wargames/bandit/bandit26.html](https://overthewire.org/wargames/bandit/bandit26.html)”
- Password in all level keep changing. So dont try to copy the password mentioned in each level.
- If you feel stucked or confused try moving through all the resources I provided.
- For youtube refrence, I found these two playlists as the best one .

### first one

[https://youtube.com/playlist?list=PLG44s1Oo_jbTzrJ4kI24LwAyjFtTSDNlq&si=B2Kg4-GGyGGc6CTp](https://youtube.com/playlist?list=PLG44s1Oo_jbTzrJ4kI24LwAyjFtTSDNlq&si=B2Kg4-GGyGGc6CTp)

### Second one:

[https://youtube.com/playlist?list=PLBf0hzazHTGOIn_vuuuCzRFVhYiDBnJID&si=V8npoKdYx04UMblk](https://youtube.com/playlist?list=PLBf0hzazHTGOIn_vuuuCzRFVhYiDBnJID&si=V8npoKdYx04UMblk)

## Level 0 login

**Commands** **Used**:  ssh [bandit0@bandit.labs.overthewire.org](mailto:bandit0@bandit.labs.overthewire.org) -p 2220

**New Command Learned**:  **ssh** :used to securely log into a remote machine and execute commands on that machine. The basic syntax of the command is “ssh user@host”

**Password**:  bandit0
## Level 0-1 login

**Commands** **Used**:  cat, ls

**New Command Learned**:  

File:  `determine file type` 

du( disk usage):  `estimate file space usage`

**Password**: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

Process:  step1: Use ls to see the files in home directory

step2:  Use cat to read the file  readme to get the pw.
## Level 1-2 login

**Commands** **Used**:  cat, ls

**Password**: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

**Process**:  

step1: Use ls to see the files in home directory

step2:  Use cat to read the file  - to get the pw.

Note: - named file cannot be read directly using command “cat -”. So, we use “cat ./-” or “cat /home/bandit1/-”.

## Level 2-3 login

**Commands** **Used**:  cat, ls

**Password**: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

**Process**:  

step1: Use ls to see the files in home directory

step2:  Use cat to read the file  spaces in this filename to get the pw.

Note:  file name with spaces cannot be read directly using command only using cat filename . So, we use “cat  “filename”” or “cat filename1\ filename2\ filename3”. here “\ “ acts as a space.

## Level 3-4 login

**Commands** **Used**:  cat, ls -a

**Password**: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

**New Command Learned**: 

 **ls -a** : shows the hidden file

 **realpath .** : shows the path of current location

## Level 4-5 login

**Commands** **Used**:  ls, cat, file

**Password**: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

**New Command Learned**: 

 **file**: shows the type of a file



**Process**:  

step1: cd inhere

step2:  ls -alps

step3:  file ./* : to read the type of all files

step4:  cat the ASCII type of file

Note: “file *”:*  cant directly access the file whose name starts with “-”. So, we use command “file ./*”.

  

## Level 5-6 login

**Commands** **Used**:  ls, file./*, find

**Password**: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

**New Command Learned**: 

find  -size 1033c -readable ! -executable



**Process**:  

step1:  cd inhere

step2:  use find command and use the given criteria of file to find that exact file in inhere directory

step3: cat the found file

Note: when bunch of file and folders are given then use the find command to search a file with given criteria.

step1: Use ls to see the files in home directory

step2:  use ls -a to see the hidden files stored in inhere directory

step3: use cat “filename” to read the file.

## Level 6-7 login

**Commands** **Used**:  ls, find

**Password**: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

**New Command Learned**: 

find  -size 1033c -user username -group groupname



**Process**:  

step1:  cd / to go to root directory

step2:  use find command to find the file with given criteria

step3:  many files with permission denied or no such file will appear except one with .password

## Level 7-8 login

**Commands** **Used**:  ls, grep

**Password**: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

**New Command Learned**: 

grep “millionth” data.txt



**Process**:  

step1:  ls

step2:  use grep command to find the data in line which contains the word millionth
## Level 8-9 login

**Commands** **Used**:  ls, sort. uniq

**Password**: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

**New Command Learned**: 

sort filename: It arrange file data in ascending order.

uniq -u filename: gives the line which occurs only once but here repeating data should be in adjacent.



**Process**:  

step1:  ls

step2:  cant use uniq -u filename directly because data in file isnot in ascending order. So, first we use sort then its output is transferred to uniq command.
## Level 9-10 login

**Commands** **Used**:  ls, strings, grep

**Password**: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

**New Command Learned**: 

strings filename: this helps to give the text from a file which is human readable



**Process**:  

step1:  ls

step2:  get the output from strings data.txt and then supply it to grep “=” to get the password.

strings data.txt | grep "=”

## Level 10-11 login

**Commands** **Used**:  ls, cat, base64

**Password**: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

**New Command Learned**: 

base64: it is a form of decoding. It is always in a format of margin with “=” or “==” at the right end .



**Process**:  

step1:  ls

step2:  cat data.txt whose result shows that the data is bade64 encoded.

step3: now use the command base 64 to decode the pw.

cat data.txt | base64 --decode

or

base64 -d data.txt

## Level 11-12 login

**Commands** **Used**:  ls, cat

**Password**: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4



**Process**:  

step1:  ls

step2:  cat data.txt 

step3:  rot13 means every character is rotated by 13. Use any rot13 conversion website like [https://rot13.com/](https://rot13.com/)  to convert it and get the password. 
## Level 12-13 login

**Commands** **Used**:  ls, cat,  mkdir, cp, mv, xxd, file, tar, gzip. bzip2

**Password**: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

 **New Command Learned**: 

cp: cp ~/data.txt .

~ represents the home directory and last “.” means copy here.

mv : mv n1 n1.gz ( n1: current filename, n1.gz filename or format we want to change n1 to)

xxd: xxd -r data.txt n1 

(explanation see in explainshell.com)

bzip2: bzip2 -d n1.bz2 (-d: decompress)

gzip: gzip -d n1.gz

tar: tar -xf filename (-x: extract, f: file) this command is used to extract the file from archieved file.

**Process**:  

step1:  cd /tmp

step2:  mkdir newfoldername

step3:  move to new folder

step4: cp ~/data.txt

step5: cat data.txt which is in hexform

step6: use xxd to reverse the hex file into binary form into a new file 

step7:  see the type of n1

step8: rename it in the format of its type( if the file type is gzip compressed then rename it to n1.gz to decompress it)

step9: decompress it using gzip.

step 9: continue this process: 

- check the file type
- rename it
- decompress it
- when tar types come, it represents archieved file
- rename it and use tar command
- continue the process until ascii type file comes

step 10: cat to get the password.
## Level 13-14 login

**Commands** **Used**:  ls, cat, ssh login using private key

**Password**: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

 **New command used**: ssh -i sshkey.private bandit14@localhost -p 2220

**Process**:  

step1:  ls

step2:  login to level 14 using private ssh key without being exit from the level 13. 

command used:  ssh -i sshkey.private bandit14@localhost -p 2220

step 3: now cat /etc/bandit_pass/bandit14 to get the pw. 

## Level 14-15 login

**Commands** **Used**:  ls, cat, telnet, nc

**Password**: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

 **New command used**: telnet [localhost](http://localhost) 30000 (create the connection with localhost through port 30000)

nc [localhost](http://localhost) 30000

**Process**:  

step1:  telnet [localhost](http://localhost) 30000

step2:  give the pw of current level to get the pw of next level.

//add ss here
## Level 15-16 login

**Commands** **Used**:  openssl

**Password**: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

 **New command used**: openssl s_client -connect localhost:30001( openssl: makes secure connection for ssl, s-client instructs to create a connection as a client)

**Process**:  

step1:  connect to the [localhost](http://localhost) 30001 using openssl command given above.

step2:  give the pw of current level to get the pw of next level.
## Level 16-17 login

**Commands** **Used**:  nmap, ncat, touch, nano

**Password**: 

znK19XRJuZTd8BvCEVW4NQjtNJbdFLNC

 RSA Key:

“

- ----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY----- “

 **New command used**: 

- nmap localhost -p 31000-32000( to check what service is running on which port)
- ncat localhost --ssl 31518 (to send input and receive output from a particular port, —ssl: this is used to establish a ssl session with ssl server)
- ls -l key (to check the permissions in the file)
- chmod 700 key(to change permission in the file for user to read, write and execute)
- 

**Process**:  

step1:  use the nmap command mentioned ( nmap localhost -p 31000-32000)

step2:  ncat each port to know which port is having ssl without echo (ncat [localhost](http://localhost) —ssl portnumber)

step3:  one port returns rsa key

step4: copy and paste this rsa key inside a file of tmp directory.

step5: try to login to level 18 using command ssh -i filename [bandit17@localhost](mailto:bandit17@localhost) -p ssl_working_port_number

step6: here permission will be denied. now check the what kind of authority user have using command: ls -l filename
## Level 17-18-19 login

**Commands** **Used**:   diff

**Password**:  x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

 **New command used**:  diff filename1 filename2(it gives the text that is different in both file)

**Process**:  

step1:  ls after logging in

step2:  diff

step3: now, when we try to login, we are automatically logged out.

step4: we know that the pw is inside readme file so use this command “ssh  [bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org) -p 2220 cat readme”

note: you will get the pw for level 19

pw for 19: 

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
step 7: give user execute access( chmod 700 filename)

step7: now try to login to level 17 again
## Level 19-20 login

**Commands** **Used**:  ls, cat

**Password**:  0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

 **New command used**: 

- ./bandit20-do: this helps to run a command as another user.

**Process**:  

step1:  ls after logging in

step2: use “./bandit20-do” command to move forward

step3:  read the pw using command “./bandit20-do cat /etc/bandit_pass/bandit20”
## Level 20-21 login

**Commands** **Used**:  ls, nc -lvp

**Password**:  EeoULMCra2q0dSkYj561DX7s1CpBuOBt

 **New command used**: 

- nc -lvp port_number: establish a connection with the [localhost](http://localhost)

(l: listen

v: (verbose): used to establish connection properly

p: local port number)

**Process**: 

step1:  ls (”suconnect” will appear)

step2:  use the command ./suconnect. note: 

This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.

step3: now open another terminal and login to level20

step4: In the second terminal use the command “nc -lvp portnumber” to establish a connection 

step5: send the pw of current level to get the next level pw.
# Level 21-22

## Commands Used

ls, cat,

## Password:

tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

## Process:

step1: ls /etc/cron.d/

step2:  now read the file cronjon_bandit22 using cat command “cat /etc/cron.d/cronjob_bandit22”

step3: now see the location of .sh file which includes the bash script.  then read that sh file using command “

cat /usr/bin/cronjob_bandit22.sh”

step4: the script shows the location of file where pw is located. Now read the file using command “

cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv” to get the pw.
# **Level 22-23**

command used: ls, cat

password: 

0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

Process:

step1: read the shell script in cronjob_bandit23 as in previous level.

step2: The script shows that pw is stored in /tmp/$mytarget file. “$mytarget”  filename is obtained by running this command “

echo I am user bandit23 | md5sum | cut -d ' ' -f 1”  which gives password like value and is the filename inside /tmp/ where pw is stored.

step3: now cat /tmp/value_obtained_by running_previous_command to get the pw.
# level 23-24

password: 

gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

Process:

step1: read the script file in cronjob_bandit24 as done in previous level.

(Note: in the script, a loop is implemented through all files even if it is hidden.

inside the do statement if files are not hidden files , then owner is checked. If the owner is bandit23 then all files are executed for 60 sec then process is terminated using “-s”. finally the file is deleted.)

step2: Now make your own script. create folders /tmp/myscript using command “

mkdir /tmp/myscript”

step4: navigate to the folder. Now make [myyscript.sh](http://myyscript.sh) and pw.txt file inside myscript folder.

step5: nano [myscript.sh](http://myscript.sh) and write the script “

#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/myscript/pw.txt”

this is store the pw into pw.txt file.

step6: “ls -la” inside myscript folder.

step7: change the permission using “chmod 777 [myyscript.sh](http://myyscript.sh/)”

step8: now copy the file to /var/spool/bandit24/foo using the command “

cp [myyscript.sh](http://myyscript.sh/) /var/spool/bandit24_pass.sh/foo”

step9: cat pw.txt to get the pw.
# Level 24-25

## Commands used:

nc, ls, nano, chmod, cat

## Password:

iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

## process:

step1: login using ssh command

step2: “nc [localhost](http://localhost) 30002” as given then you will get the pw when you enter the “pw_of_current_level a_pincode” and this pincode can be any number within 0 to 9999.

step3: generate all the  “pw_of_current_level a_pincode” combinations using a script. code of script: “

#!/bin/bash

for i in {0..9}{0..9}{0..9}{0..9}
do
echo "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i" >> list.txt;
done”

step4: before running the script make a file list.txt in level24 directory 

step5: run the script using command “

./pwlist.sh”

step6: now display all the input combinations using command “

cat list.txt”

step7: now brute force using this command “cat list.txt | nc localhost 30002” then the pw will be displayed.
# Level 25-26

## password:

s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

New commands learned:

- more
- -v
- :set shell?: gives the name of current shell you are in
- :set shell=shell_name
- 

## Process:

step1: ls

step2: use the private ssh key file to login. You will be logged in but it will exit you with popup mssg 

step3: if you want to see the script that is making you exit use the command “cat /etc/passwd | grep bandit26”. This command is used to see all the users and it is filtered out to see only bandit26 user.

step4: Now you will get the path of shell script. now to read it use the command “cat /user/bin/showtext”

step5: Research about “more” command.

step6: Now you are well known of more command. So moving forward, we will minimize the terminal as small as possible and again try to login using sshkey. 

step7: now bandit26 will not appear clearly and you will see the text”more random%”. 

step8: now type “-v”. this will open the editor in the shell. 

step9: use the command “:set shell?” to know in which shell you are.

step10: “:set shell=/bin/bash” to go to bandit 26

step11: run” :shell” command to enter bandit26.
# Level 26-27

## password:

upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

## Process:

step1: ls

step2: ./bandit27-do 

step3: now run command as bandit user 27 “

./bandit27-do cat /etc/bandit_pass/bandit27” to get the pw.
# Level 27-28

## Password:

Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## Process:

step1: make a directory inside /tmp where you want to clone the git repo

step2: move to that directory

step3: use this command to clone the repo “

git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo”. Dont forget to specify the port number. And give the pw of current level.

step4: ls

step5: cd repo

step6: ls

step7: cat [README.md](http://README.md) to get the pw.
# Level 28-29

## Password:

4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

## Process:

step1: clone the git repo as in previous level. use this command “

git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo”

step2:  try to read the readme file. 

step6: you will not get the pw there.

step7: check the versions using “git log”

step8: now try to move through all commits using the command “git checkout commit_hashvalue” then read the readme file. You will get the pw for next level in any one of them.
# Level 29-30

## Password:

qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

## Process:

step1: clone the git repo as in previous level. make the directory first then clone there. 

step2: try reading the readme file in each commit as in previous level.

step3: Now, check for the branches using command “git branch” 

step4: to see all the branches use “git branch -a”

step5: move through each branches and read the [readme.md](http://readme.md) file to get the pw.
# Level 30-31

## Password:

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

## Process:

step1: clone the git repo

step2: go through all the branches and commits and read the readme file.

step3: If step2 not working, then use “ git tag” 

step4: use the command “git show secret” to see if pw is there.
