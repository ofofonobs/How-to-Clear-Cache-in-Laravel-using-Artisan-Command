In this articale, you will learn how to clear caches in laravel application. In laravel application you can clear cache two types using artisan command and from browsers.

I will mention few commands you can use to clear various types of cache like config cache, view cache, route cache and application cache from your laravel application.

If you want to clear cache using commnad then open your terminal and go to the laravel application's folder and execute below commands:

Clear Application Cache

To clear laravel application cache, run the following artisan command:

php artisan cache:clear
Clear Route Cache

To clear route cache of your Laravel application run the following artisan command:

php artisan route:clear
Clear Configuration Cache

To clear the config cache of your laravel application, run the following artisan command:

php artisan config:clear
Clear Compiled Views Cache

To clear the view cache of your laravel application which are basically compiled view files, run the following artisan command:

php artisan view:clear
If you want to clear cache through browser then we need to run these commands programatically because sometimes hard to get console access to your laravel application. So this method is very easy and helpfull Clear Cache in Laravel using Browser.

Thus, we will create special routes to clear cache in Laravel.

// Clear application cache:
Route::get('/clear-cache', function() {
    Artisan::call('cache:clear');
    return 'Application cache has been cleared';
});

//Clear route cache:
Route::get('/route-cache', function() {
	Artisan::call('route:cache');
    return 'Routes cache has been cleared';
});

//Clear config cache:
Route::get('/config-cache', function() {
 	Artisan::call('config:cache');
 	return 'Config cache has been cleared';
}); 

// Clear view cache:
Route::get('/view-clear', function() {
    Artisan::call('view:clear');
    return 'View cache has been cleared';
});
