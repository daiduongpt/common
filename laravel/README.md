# Laravel

### Some useful 
+ Get query log
    ```
        DB::enableQueryLog();
        DB::getQueryLog()
    ```

+ Get paginator
    ```
        $paginatorIns = new LengthAwarePaginator(
            $jobList->forPage($searchParams['page'], CommonConstants::DEFAULT_SEARCH_LIMIT),
            $jobList->count(),
            CommonConstants::DEFAULT_SEARCH_LIMIT,
            $searchParams['page'],
            []
        );
    ``` 

+ Create custom route: Go to `RouteServiceRovider` and register.
   
+ Sometime error openssl when install new project: `composer config -g -- disable-tls true`  

+ Useful package:
    - Laravel permission: https://docs.spatie.be/laravel-permission/v3/installation-laravel/
    - Laravel passport: https://laravel.com/docs/7.x/passport
    - Laravel admin: https://laravel-admin.org/docs/v1.4/#/
    - QrCode: simplesoftwareio/simple-qrcode
    - BarCode: zendframework/zend-barcode
    
+ Publish config: ` php artisan vendor:publish --provider="Encore\Admin\AdminServiceProvider"`    

+ Clear cache: ` php artisan cache:clear && php artisan route:clear && php artisan config:clear && php artisan view:clear`

+ Excel: 
    ```
        # Read file
        Excel::load($file, function ($reader) use (&$rows) {
            $rows = $reader->select(['h1', 'h2', 'h3'])->get();
        });
  
        # Download
        Excel::create('file_excel_name'),
            function($excel) use($data) {
                // Set the title
                $excel->setTitle('Title');

                // Chain the setters
                $excel->setCreator('DayOne')
                    ->setCompany('DayOne');

                // Call them separately
                $excel->setDescription('Desc');

                $excel->sheet('Sheet 1', function($sheet) use ($data) {
                    $sheet->setFontFamily('Tahoma');
                    $sheet->fromArray($data);
                });
            })->download('xlsx');
    
    ```