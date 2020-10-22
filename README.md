## About

This is a contacts manager app with login and registration. These are two separate projects. API is written in PHP using Laravel Framework and the frontend is written in Typescript Vue. I can have this project in a single installation via laravel-mix and have the vue files inside the Laravel installation. However, I think this approach is the best in a lot of scenarios. One particular reason is to separate the front-end project from the backend so that in case that the project needed to be updated (eg: Migrating from laravel to ExpressJS), the other project will not be affected. A decoupled project is more maintainable.

## Contacts App Installation

1. Clone this repository.

### API

cd to `api/` directory

```
cd api
```

Install dependencies

```
composer install
```

Run migrations

```
php artisan migrate
```

Generate app secret

```
php artisan key:generate
```

Generate JWT key

```
php artisan jwt:secret
```

Edit .env file and make the appropriate changes.

### App

cd to `app/` directory

```
cd app
```

Install dependencies

```
npm i
```

Update `site.ts` and change `apiUrl` to the API endpoint's URL.

```
vi src/constants/site.ts
```

```Typescript
export default {
    apiUrl: 'http://contacts.test/api' // Change this line
};
```

Run

```
npm run serve
```

## Unit Tests

The API contains unit tests. under the `tests/` directory. App does not have any test.
