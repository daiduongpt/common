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
+ Sometime error openssl when install new project: ``composer config -g -- disable-tls true``  