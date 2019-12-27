# Mongodb

### Notes
+ Cookie

    > Get cookie by key
    ```
        let cookies = document.cookie.split(';');
        let resp;
        for(let c of cookies){
            if(c.indexOf(key + '=') != -1){
                resp = c.substring(c.indexOf(key + '='), c.length);
            }
        }
        return resp;
    ```
    
    > Get cookie by key
    ```
        setCookie: (key, value, exDays) => {
            var d = new Date();
            d.setTime(d.getTime() + (exDays*24*60*60*1000));
            var expires = "expires="+ d.toUTCString();
            document.cookie = key + "=" + value + ";" + expires + ";path=/";
        }
     ```
     
    > Delete cookie
    ```
         document.cookie = key + "=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
    ```
