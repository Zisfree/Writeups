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
- The password this time too was inside the inhere file on the main directory. I hopped inside using ls and found there were 9 or 10 files. Only 1 had the password. Others had non-human-readable texts. I went through them one-by-one and found the password.
### bandit6
- This one took 7 minutes. In this I had to use the find command. Using the find command, I had to find the file with the info given to me. Then it was easy. I was not using find first so it took me time to figure out how to do it. `find . -type f -size 1033c ! -executable`(1033c here stands for bytes. and ! -executable to find the executable files.)
### bandit7 
- I use the password for the bandit7 and then do ls to find a file named data.txt. They said to find the password next to the word millionth so I used grep to filter it out.
### bandit8
- This time I had to find the password again in data.txt. This time it was non repeating so I used sort command with uniq. Since uniq works only when lines aren't spaced so I had to use sort to sort them alphabetically and without space.
### bandit9
- This one was a little bit tricky. First I was supposed to find the password in data.txt again. This time nothing came out when I used grep to find any word preceding with multiple =. So I ran `cat data.txt`, to find what exactly is inside it and it printed unreadable text so I guessed I had to run the file. So I used `./data.txt` which obviously did not work. So I used `strings data.txt` and I got a proper output but to make it more easier I used grep again and I had the password.
### bandit10
- This time it was easy for me as, I already knew how to decode base64 text. So I used the grep to find the base64 encoded password inside the data.txt and decoded it to get the password.
### bandit11
- 
