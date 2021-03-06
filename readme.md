# [DSS] Eloquent exercise

## Project initialization

After downloading the project execute
```shell
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate:install
```

If you have dependency errors when initializing the project, execute this command
```shell
composer update
```

## Writing your code

Your models must be in the `App` namespace. The unit tests in this project will try to load them in the following way:
```php
use App\Player;
use App\Team;
use App\Sponsor;
```

You must also create the migrations in folder `database/migrations`, and the seeders in folder `database/seeds` for initializing the database. You can execute them together with:
```shell
php artisan migrate --seed
```

## Running the tests

The folder `tests/Unit` contains several tests for the exercise. Once you have written your code, and executed the migrations and seeders, run PHPUnit with:
```shell
vendor/bin/phpunit
```
