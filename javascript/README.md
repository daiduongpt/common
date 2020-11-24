# Javascript

### Useful javascript
+ Sheetjs: [Link][1]

###
+ Convert input value
    ```
    currencyTarget.on('keyup input', function () {
        wrapperErrorTarget.addClass('d-none');
        let amount = $(this).val();
        if (amount) {
            amount = amount.replace(/[a-zA-Z,.\\/:;'"{}\[\]\-=~`!@#$%^&*()+]/g, '');
            if( !amount.match(/^[0-9]+$/g) || amount <= 0) {
                amount = '';
            }
            let amountNumber = Number(amount);

            amount = new Intl.NumberFormat('en-EN').format(amountNumber);
            $(this).val(amount);
        }
    })
    ```

[1]: https://docs.sheetjs.com/
      
