# Key

### Some useful 
+ RSA
    ```
    + Generate rsa private key: `openssl genrsa -out rsa_privatekey.pem 128`
    + Generate rsa public key: `openssl.exe rsa -in rsa_privatekey.pem -pubout -out id_rsa.key.pem`
    + Check bit length: `openssl rsa -in rsa_privatekey.pem -text -noout`
    ```
+ EC
    ```
    + List: `openssl ecparam -list_curves`
    + Generate ec params: `openssl ecparam -name secp112r1 -genkey -out ec_privatekey.pem`
    + Generate ec public: `openssl ec -in ec_privatekey.pem -pubout -out ecpubkey.pem`
    ```  

### Some examples openssl|phpseclib
+ Encrypt and signature: [Link][1]
+ Encrypt with libsodium: [Link][3]
+ Tool online: [Link][4]

[1]: https://hotexamples.com/examples/phpseclib.crypt/Hash/-/php-hash-class-examples.html
[2]: http://phpseclib.sourceforge.net/rsa/intro.html
[3]: https://github.com/discordrb/discordrb/wiki/Installing-libsodium
[4]: https://8gwifi.org/hmacgen.jsp
[5]: http://certificate.fyicenter.com/2032_OpenSSL_rsautl_data_too_large_for_key_size_Error.html