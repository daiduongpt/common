# MYSQL

### Notes
+ Install mysql server: [Here][1]
+ Create user, more info go [Here][2]
    ```
    CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'user_password';
        localhost | specific ip | %
        
    GRANT ALL PRIVILEGES ON database_name.* TO 'database_user'@'localhost';    
    ```
+ Get, set variable
    ```
        SHOW VARIABLES LIKE '%max_connect_errors%';
        
        SET GLOBAL max_connect_errors=101;
    ```
[1]: https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04
[2]: https://linuxize.com/post/how-to-create-mysql-user-accounts-and-grant-privileges/
