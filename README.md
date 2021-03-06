[![Build Status](https://travis-ci.org/hristonev/sportmonks-client-bundle.svg?branch=master)](https://travis-ci.org/hristonev/sportmonks-client-bundle)  SportMonks Soccer API
=============================


## API Version support

This API Client supports SportMonks v2.0.

## Requirements

- PHP 7.0 or higher

### Installation

`composer require mohammad-mazraeshahi/sportmonks-soccer-api`

## Configuration

In your `config/app.php` add `'SportMonksAPI\Soccer\SportMonksSoccerApiServiceProvider'` to the end of the `$providers` array

```php
'providers' => [

    Illuminate\Foundation\Providers\ArtisanServiceProvider::class,
    Illuminate\Auth\AuthServiceProvider::class,
    ...
    SportMonksAPI\Soccer\SportMonksSoccerApiServiceProvider::class,

],


'alias' => [
    ...
    'SportMonksSoccerApi' => SportMonksAPI\Soccer\APIFacade::class,
]
```

Copy the package config to your local config with the publish command:

```shell
php artisan vendor:publish --provider="SportMonksAPI\Soccer\SportMonksSoccerApiServiceProvider"
```

And add Token in config/sportMonks.php