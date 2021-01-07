# Wamp

### Notes
+ Add new PHP version
    ```
        Download binaries on php.net
        Extract all files in a new folder : C:/wamp/bin/php/php5.4.13/
        Copy the wampserver.conf from another php folder (like php/php5.2.8/) to the new folder
        Rename php.ini-development file to phpForApache.ini
        Done ! Restart WampServer (>Right Mouseclick on trayicon >Exit)
    ```
+ Config vhost
    ```
        <VirtualHost *:80>
            ServerName laravel.basic.local
            DocumentRoot "e:/SoftInstalled/wamp/www/laravel_basic/public"
            <Directory "e:/SoftInstalled/wamp/www/laravel_basic/public">
                Options Indexes FollowSymLinks MultiViews
                AllowOverride All
                Allow from all
        	Require all granted
            </Directory>
        </VirtualHost>
    ```

