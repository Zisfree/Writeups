### bandit0
- SSH into bandti0 user using pass provided `ssh -p {port} usernmae@hostname`
### bandit1 
- Inside the bandit0 user I got to /home directory using ls. I searched inside and found readme file inside one of the folders.
### bandit2 
- For the next I ssh into new user bandit1 and use the password found. Then I got to bandit1 file in home and we have another password there.
### bandit3 
- I ssh into bandit2 using the password and find the next file which was obviously inside bandit2 but this time it had something new, to opening the file with spaces. I solved it and opened the file. Which had the new password.
### bandit4
- This time the file we had to work on was in the main directory so I didn't use / just ls and the filename. After going inside the file there was nothing. So I used the ls commands operation to show me all the files, using which I opened the file and found the password. I was stuck on the part where I was not supposed to add the /. 
### bandit5
- The password this time too was inside the inhere file on the main directory. I hopped inside using ls and found there were 9 or 10 files. Only 1 had the password. Others had non-humanreadable texts. I went through them one-by-one and found the password.
### bandit6
- This one took 7 minutes. In this I had to use the find command. Using the find command, I had to find the file with the info given to me. Then it was easy. I was not using find first so it took me time to figure out how to do it. `find . -type f -size 1033c ! -executable`(1033c here stands for bytes. and ! -executable to find the executable files.)
### bandit7 
- 
