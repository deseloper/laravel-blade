### Installation
The package can be installed via Composer by requiring the "deseloper/laravel-blade": "*" package in your project's composer.json.

```json
[
    "repositories": [
        {
          "type": "vcs",
          "url": "https://github.com/deseloper/laravel-blade"
        }
    ],
	"require": {
	    "deseloper/laravel-blade": "*"
	}
]
```

### Usage

```php
<?php

/*
|--------------------------------------------------------------------------
| Register The Auto Loader
|--------------------------------------------------------------------------
|
| Composer provides a convenient, automatically generated class loader
| for our application. We just need to utilize it! We'll require it
| into the script here so that we do not have to worry about the
| loading of any our classes "manually". Feels great to relax.
|
*/

require 'vendor/autoload.php';

use Philo\Blade\Blade;

$views = __DIR__ . '/views';
$cache = __DIR__ . '/cache';

$blade = new Blade($views, $cache);
echo $blade->view()->make('hello');
```

You can use all blade features as described in the Laravel 5 documentation:
http://laravel.com/docs/templates#blade-templating
