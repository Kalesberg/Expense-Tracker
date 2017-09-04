## Installation
```
$ composer install && npm install
```

Open ```.env``` and enter necessary config for DB.

```
$ php artisan migrate
$ php artisan db:seed
```

## Work Flow

**General Workflow**

```
$ php artisan serve --host=0
```
Open new terminal
```
$ gulp && gulp watch
```

> Default Username/Password: admin@example.com / password


## Deploy to heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

1. Click deploy button
2. After build and "successfully deployed", Click Manage App
3. Go to settings and click "Reveal Config Vars"
4. Set necessary config for DB based from CLEARDB_DATABASE_URL or from your custom database
5. Execute migration and db seed with the following commands

**Database Migration**
```
$ heroku run php artisan migrate --app your_app_name
```
**Database Seeds**
```
$ heroku run php artisan migrate --app your_app_name
```

**FAQ**

In case of Node Sass error during gulp compilation try this command:
```
$ npm rebuild node-sass
```