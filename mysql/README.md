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
+ Drop, add index
    ```
        ALTER TABLE `job_lists` ADD FULLTEXT INDEX `name` (`name`);
        ALTER TABLE `job_lists` DROP INDEX `name`;
        CREATE FULLTEXT INDEX name_index ON job_lists(name);
    ```  
+ Connect
    ``` 
        mysql -h host -u"duong.vu" -p<pass> dbname -P 3306
        mysqldump -h host -u"duong.vu" -pDuong@2020! -P 3306 --default-character-set=utf8 --result-file=gotit.sql gotit --verbose (error lock table: --single-transaction or --lock-tables=false)
        Get-Content gotit.sql | mysql -uroot -P 3308 -p --default_character_set utf8 gotit; (power shell window)
    ```  
+ For trigger
    ```sql
        mysqldump -h localhost -uroot -p --routines --add-drop-trigger --add-drop-trigger --no-create-info --no-data --no-create-db --skip-opt gotit > gotittrigger.sql
        mysql < triggers.sql  
        Get-Content gotittrigger.sql | mysql -uroot gotit
    ```  
+ Lock wait time out
    ```sql
        transaction-isolation = READ-COMMITTED
        SELECT @@GLOBAL.transaction_isolation, @@transaction_isolation, @@session.transaction_isolation;
        SHOW ENGINE INNODB STATUS\G
```

+Lock for update (ex: laravel)
    ```
        Usually, this prevent nth request same resource must be wait to selected and process => can be overwrite
    ```

+ Mapping error state
    ```
        https://dev.mysql.com/doc/connector-j/5.1/en/connector-j-reference-error-sqlstates.html
    ```
  
### Problems
+ Export question mark: [Here][3]
  
[1]: https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04
[2]: https://linuxize.com/post/how-to-create-mysql-user-accounts-and-grant-privileges/
[3]: https://confluence.atlassian.com/confkb/characters-appear-as-question-marks-using-mysql-204051027.html
