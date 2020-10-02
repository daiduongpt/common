# PHP

### Notes
+ Abstract vs Interface: [Here][1]
+ Ubuntu php multi versions:
    ```php
          sudo update-alternatives --config php  
          sudo a2dismod php5.6
          sudo a2enmod php7.1
          sudo service apache2 restart
    ```
+ File excel html accept: `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/vnd.ms-excel`

+ PHP unit: `vendor/bin/phpunit file --coverage-html coverage`

[1]: https://codeinphp.github.io/post/abstract-class-vs-interface/
