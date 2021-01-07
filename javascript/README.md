# Javascript

### Useful javascript
+ Sheetjs: [Link][1]
+ Copy event: [Link][2]
+ Webpack beginner: [Link][3]
+ Create react app: [Link][4]
+ React app structure: [Link][5]
+ Create react native: [Link][6]
+ React tools: [Link][7]
+ React router v5: [Link][8]
+ Material kit: [Link][9]
+ Find font: [Link][10]
+ Lazy load: [Link][11]

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
[2]: https://www.sitepoint.com/clipboard-api/
[3]: https://www.sitepoint.com/webpack-beginner-guide/
[4]: https://www.sitepoint.com/create-react-app/
[5]: https://www.sitepoint.com/organize-large-react-application/
[6]: https://www.sitepoint.com/getting-started-with-react-native/
[7]: https://www.sitepoint.com/essential-react-tools/
[8]: https://www.sitepoint.com/react-router-complete-guide/
[9]: https://www.creative-tim.com/templates/free
[10]: https://www.whatfontis.com/
[11]: https://www.sitepoint.com/five-techniques-lazy-load-images-website-performance/

