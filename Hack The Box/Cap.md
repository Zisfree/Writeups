# Cap
Cap is an Easy machine. It has the use of wireshark, basic python, concept of IDOR and website enumeration.

## Enumeration
- First we do a nmap scan which will show us 3 ports.
- I tried the http first which lands us in a website.
- After going here and there in the website, I managed to find `/data/2` endpoint. In which if we change our data type from 2 to 0, we are able to see other's network information.

## Foothold
- We can download this info in a file. After googling I found out we can run it with wireshark.
- In wireshark I found the password and username. Using them did ssh on the user nathan, as it was his data.

## PrivEsc
- In the system, I found ou that it has given SUID to the python3.
- So I found a command `python3 -c 'import os; os.setuid(0); os.execl("/bin/bash", "bash", "-p")'`. This command will give us root shell.
- After getting the root access I got the root flag easily.
