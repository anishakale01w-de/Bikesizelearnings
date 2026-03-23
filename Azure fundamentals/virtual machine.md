Commands executed in next steps - Azure VMs
Here are some of the commands we would execute in the next few steps:

You can refer back to this if you have problems. Good Luck.

ls
 
chmod 400 my-sql-server-vm_key.pem
ssh -i my-sql-server-vm_key.pem azureuser@13.78.236.186
 
ls /opt/mssql/bin
 
sudo /opt/mssql/bin/mssql-conf set-sa-password
 
sudo systemctl stop mssql-server
sudo systemctl start mssql-server
 
cd /opt/mssql-tools/bin
./sqlcmd -S localhost -U SA -p
 
CREATE DATABASE UsersDb
go
 
use UsersDb
go
 
create table users (id INT, name NVARCHAR(100))
go
 
insert into users values (1,'Ranjith');
insert into users values (2,'John');
insert into users values (3,'Ramesh');
go
 
select * from users
go