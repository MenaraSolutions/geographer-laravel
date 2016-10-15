# geographer-laravel
Laravel (and Lumen) integration for Geographer

## Getting started

Install Laravel integration package first:

```
$ composer require menarasolutions/geographer-laravel
```

Good news is that Laravel will take care of singleton instance for you, so no matter how many times you call it – it's the same object.

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
