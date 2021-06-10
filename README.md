
Step One—Perform a MySQL Dump
Back it up on the original virtual server by using the mysqldump command.
mysqldump -u root -p --opt [database name] > [database name].sql

Step Two—Copy the Database
SCP helps you copy the database
scp [database name].sql [username]@[servername]:path/to/database/
#scp newdatabase.sql user@example.com:~/

Step Three—Import the Database
Once the data has been transferred to the new server, you can import the database into MySQL:
mysql -u root -p newdatabase < /path/to/newdatabase.sql
