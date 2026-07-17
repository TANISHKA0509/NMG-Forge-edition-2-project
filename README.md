# NMG Submission Backend

Laravel 12 backend application prepared for submission.

## Requirements

- PHP 8.2 or newer
- Composer
- Node.js and npm
- SQLite, MySQL, or another Laravel-supported database

## Setup

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
npm install
npm run build
```

The default `.env.example` uses SQLite. To use SQLite locally, create the database file before running migrations:

```bash
touch database/database.sqlite
php artisan migrate
```

## Development

Run the Laravel development server:

```bash
php artisan serve
```

In a separate terminal, run Vite when working on frontend assets:

```bash
npm run dev
```

## Tests

```bash
php artisan test
```
