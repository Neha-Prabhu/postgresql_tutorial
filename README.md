# postgresql_tutorial

## Installing postgres on ubuntu 20.04

to update and upgrade packages

```
$ sudo apt update
$ sudo apt -y upgrade
```
to Install PostgreSQL on Ubuntu 20.04
```
$ sudo apt install postgresql postgresql-client
```
After completing the installation of PostgreSQL, you will start, stop, and enable the PostgreSQL services using the following command:
```
$ sudo systemctl stop postgresql.service
$ sudo systemctl start postgresql.service
$ sudo systemctl enable postgresql.service
```

Now, to verify the PostgreSQL service status that either it is running on your system or not. Use the following command to check the service status:
```
$ sudo systemctl status postgresql.service
```

Setting PostgreSQL user password:
```
sudo passwd postgres
```
![output of above command](https://linuxhint.com/wp-content/uploads/2020/06/6-48.png)

##Access PostgreSQL shell

PostgreSQL has been installed on your system. Now, you will log in to PostgreSQL as a user to access the databases and working shell using the following command:
```
$ sudo su -l postgres
$ psql <dbname>
```
default db is postgres.

Creating a database and user roles:

creating a db:
```
postgres=# create database testdb;
```
moving inside a database:
```
postgres=# \c testdb
```

after u enter into a db
```
testdb=# alter user postgres with password 'my00pass';
```
Use the following command to list databases:
```
$ psql -l
```
