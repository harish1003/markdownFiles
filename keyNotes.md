> What is sanity ?
 
 This sanity test is performed after receiving the software build, sanity test is performed to ensure that code changes introduced are working as expected.
 It is performed only after the build has cleared the smoke test and been accepted by the Quality Assurance team for further testing. If the sanity test fails, the build is rejected by the testing team to save time and money.

> How to change db password / password expiry ?
1. open sql plus, enter user name as : SYS AS SYSDBA -- trying to login as a root user, no need to enter the password, just click on the enter button
2. after connecting, ALTER USER USER_NAME IDENTIFIED BY NEW_PASSWORD;
or
enter username : hr
enter passwword : hr
password expiry .. .
new password --> enter
retype --> enter

* if command prompt is not showing enter username use this CONN USERNAME/PASSWORD

> How to create a users in db ?
1. connect to a database using sqlplus conn username/password
2. CREATE USER MY_USER IDENTIFIED BY MY_PASSWORD
3. GRANT CONNECT, RESOURCE TO MY_USER

