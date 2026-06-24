# Deployment Notes

This is a Laravel 5.5 ecommerce project. GitHub can store the source code, but it cannot host the PHP admin panel directly with GitHub Pages.

## Recommended Hosting

Use a PHP/MySQL host such as cPanel/shared hosting or a VPS.

## Server Requirements

- PHP 7.0 to 7.4
- MySQL or MariaDB
- Composer, unless the host lets you upload built dependencies
- PHP extensions commonly required by Laravel: openssl, pdo_mysql, mbstring, tokenizer, xml, ctype, json, fileinfo, gd

## Deploy Steps

1. Upload this repository to the server.
2. Point the web root to this folder so `index.php` is public, or configure the server to route all requests to `index.php`.
3. Create a MySQL database.
4. Import `database.sql`.
5. Copy `core/.env.example` to `core/.env`.
6. Update `APP_URL`, `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD`.
7. Run `composer install` inside `core` if `core/vendor` is not uploaded.
8. Ensure these folders are writable by PHP:
   - `core/storage`
   - `core/bootstrap/cache`
   - `assets/images/product`
   - `assets/images/advertise`
   - `assets/images/payment`
   - `assets/images/slider`

The local `.runtime` folder is only for running the project on this computer and should not be uploaded.
