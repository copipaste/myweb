colocar esto dentro de Procfile
web: heroku-php-apache2 web/

variables de ambiente

heroku config:set APP_DEBUG=false
heroku config:set APP_NAME=laravel-app
heroku config:set APP_ENV=production
heroku config:set APP_KEY=base64:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

heroku config:set APP_URL=https://laravel-app.herokuapp.com
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel-app
DB_USERNAME=root
DB_PASSWORD=root



AGREGAR ESTO EN AppServiceProvider.php
if($this->app->environment('production')) {
    \URL::forceScheme('https');
}