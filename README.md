# PHP Dotenv

Loads environment variables from .env file to `getenv()`, `$_ENV` and `$_SERVER`

## Installation

```bash
composer require nazares/phpdotenv
```

## Usage

`.env` file

```dotenv
DB_HOST =localhost
DB_NAME = test
DB_PASSWORD= secret
```

```php
$dotenv = new \nazares\phpdotenv\Dotenv($path);
$dotenv->load();

echo getenv('DB_HOST'); // localhost
echo $_ENV['DB_NAME']; // test
echo $_SERVER['DB_PASSWORD']; // secret
```

or

```php
(new \nazares\phpdotenv\Dotenv($path))->load();

echo getenv('DB_HOST'); // localhost
echo $_ENV['DB_NAME']; // test
echo $_SERVER['DB_PASSWORD']; // secret
```
