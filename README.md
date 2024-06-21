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
