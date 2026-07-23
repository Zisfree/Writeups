## Enumeration
- First I use nmap to scan for open ports. Which are 2 open, 1 is http and other is ssh.
- Then I use the IP in browser and it did not open. So I added the site orion.htb to my hosts list as it was written.
- Using that I managed to open the site. After seacrching for a while on the website and its source code, I didn't find anything.
- So I used ffuf on the sub folders. I found 4 results out of which /admin lead me to a login page.
- This login page had its version below which I searched online and found its CVE-2025-32432.
