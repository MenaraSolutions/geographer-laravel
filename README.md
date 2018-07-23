# geographer-laravel
Laravel (and Lumen) integration for Geographer

## Getting started

Install Laravel integration package first:

```
$ composer require menarasolutions/geographer-laravel
```

Good news is that Laravel will take care of singleton instance for you, so no matter how many times you call it – it's the same object.

> In Laravel 5.5, [service providers and aliases are automatically registered](https://laravel.com/docs/5.5/packages#package-discovery). If you're using Laravel 5.5, skip ahead.

```php
// Add in your config/app.php

'providers' => [
    '...',
    MenaraSolutions\Geographer\Integrations\LaravelServiceProvider::class,
];

'aliases' => [
    '...',
    'Geographer' => MenaraSolutions\Geographer\Integrations\LaravelFacade::class,
];

// Start playing with it, all the same calls
Geographer::getCountries()->useShortNames()->toArray();
```

Full list of methods is available in [Geographer documentation](https://github.com/MenaraSolutions/geographer)
