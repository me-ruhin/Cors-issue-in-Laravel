# Cors-issue-in-Laravel

## Step:01 : Create a middleware

> php artisan make:middleware Cors 

## Step:02 Modify the handle method()

```

return $next($request)
	->header('Access-Control-Allow-Origin', '*')
	->header('Access-Control-Allow-Methods', 'POST, GET,PUT,DELETE,OPTIONS')
	->header('Access-Control-Allow-Headers', 'Accept,Authorization,Content-Type'); 
}

```

## Step:02 Open the Kernel.php file

```
Add the Cors middleware path in $middleware group 
 
protected $middleware = [
	\App\Http\Middleware\Cors::class
]

```


