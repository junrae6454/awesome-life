# mysql data dir change

---
* {variable} must be replaced to your variable
  - ex) 
      ```sql
      mysql > create user '{userid}'@'%' identified by 'password'; 
      -> 
      mysql > create user 'my_user_id'@'%' identified by 'password';
      ```
      
### create mysql user
- ```sql
  mysql > create user '{userid}'@'{host}' identified by '{password}';
  ```
  
### If you need login from any network, change host -> %
- ```sql
  mysql > create user '{userid}'@'%' identified by '{password}';
  ```
  
### set permission for user
- ```sql
  mysql > GRANT ALL PRIVILEGES ON {DB_NAME}.{TABLE_NAME} TO {userid}@{host};
  mysql > GRANT ALL PRIVILEGES ON *.* TO {userid}@{host};
  mysql > flush privileges;
  ```

# Done!
