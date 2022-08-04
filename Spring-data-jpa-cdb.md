**Creating a new Schema (Solving insufficent Privilages problem) oracle sql developer**
Microsoft Windows [Version 10.0.22000.832]
(c) Microsoft Corporation. All rights reserved.
C:\Users\91767>sqlplus
SQL*Plus: Release 11.2.0.2.0 Production on Thu Aug 4 12:23:26 2022
Copyright (c) 1982, 2014, Oracle.  All rights reserved.

Enter user-name: hr
Enter password:
Connected to:
Oracle Database 11g Express Edition Release 11.2.0.2.0 - 64bit Production
SQL> create user schooldb identified by schooldb;
ERROR at line 1:
ORA-01031: insufficient privileges
SQL> connect
Enter user-name: sys as sysdba
Enter password: here password is what you have given to create db <hr> i gave.
Connected.
SQL> grant sysdba to system;
Grant succeeded.
SQL> create user schooldb identified by schooldb;
User created.

Oracle Credentials:
Name : MyOracleDatabase
username :hr
password :hr
sid : XE
port :1521
Host : localhost
