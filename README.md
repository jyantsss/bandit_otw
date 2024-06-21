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
