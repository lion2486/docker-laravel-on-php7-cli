# docker-laravel-on-php7-cli
Docker image for Laravel 5.1 on php7-cli

## Usage

```
$ cd /path/to/laravel-application
$ docker run -v `pwd`:/code shin1x1/laravel-on-php7-cli
Laravel Framework version 5.1.28 (LTS)

$ docker run -v `pwd`:/code shin1x1/laravel-on-php7-cli php artisan env
Current application environment: local
```

## docker-composer (with postgres)

```
$ docker-compose up -d

# application setting
$ cp .env.example .env
$ docker-compose run web php artisan key:generate
$ docker-compose run web php artisan migrate
$ docker-compose run web php artisan db:seed

# PHPUnit
$ docker-compose run web ./vendor/bin/phpunit
```
