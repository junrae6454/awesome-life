# mysql data dir change

---
## ubuntu

### install mysql server
- ```bash
  sudo apt-get install mysql-server
  ```

### stop mysql
- ```bash
  sudo systemctl stop mysql
  ```

### create or copy datadir
- ```bash
  sudo cp -R -p /var/lib/mysql /data/dir/where/you/want
  ```

### change datadir in mysqld.cnf
- ```bash
  vi /etc/mysql/mysql.conf.d/mysqld.cnf

  change
  datadir = /var/lib/mysql -> /data/dir/where/you/want/mysql
  ```
### apparmor alias
- ```bash
  vi /etc/apparmor.d/tunables/alias

  append
  alias /var/lib/mysql/ -> /data/mysql/,
  ```

### restart mysql.service
- ```bash
  sudo systemctl start mysql
  ```

# Done!
