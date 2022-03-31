<br/>
<br/>
<div align="center">
    <img src="image/worldcob-w.png" alt="Logo" width="200" height="200" />
</div>
<br/>
<br/>

# BIZZDOME-BACKEND
```sh
# Note: only supports php:^8.0.
# Make sure currently requires redisphp to be installed on the system
```
- [phpredis ext](https://pecl.php.net/package/redis)
- [Guide for installing extension on windows](https://dev.to/dendihandian/installing-php-redis-extension-on-laragon-2mp3)
- [Guide for installing redis on windows via laragon](https://forum.laragon.org/topic/35/work-with-redis/4)

```sh
# Currently the app should be configured to use s3 for development
# It is also required to generate a 
```
- [MAXMIND License key](https://www.maxmind.com/en/home)

```sh
# Make sure you configure mailtrap or mailhog locally
# Make sure that the access_token and refresh_token are the same as on the `bizzdome-ws` project
```

##### Clone GitHub
```sh
git clone [Repositorio] [rename]
cd [Repositorio]
```

##### Install PHP dependencies
```sh
composer install
```

##### Install NPM dependencies
```sh
yarn install
```

##### Build assets
```sh
yarn dev
```

##### Setup configuration
```sh
cp .env.example .env
```

##### Generate application key:
```sh
php artisan key:generate
```

##### Run database migrations:
```sh
# Create a database (MySQL).
```
```sh
php artisan migrate
```


##### Generate Super Admin
```sh
php artisan central-app:init-supa
```
```sh
~ User: admin@bizz-dome.com
~ Password: v1demo
```

##### Execute command
```sh
php artisan queue:work
```

##### AWS - S3
```sh
~ User: dliza-s3
```

<br/>

# BIZZDOME-FRONTEND

##### Setup configuration
```sh
cp .env.example .env.local
```
##### Project setup
```sh
yarn install
```
##### Compiles and hot-reloads for development
```sh
yarn serve
```
##### Compiles and minifies for production
```sh
yarn build
```
##### Lints and fixes files
```sh
yarn lint
```

<br/>

# BIZZDOME-WS
```sh
# This project depends on the laravel component backend to have created the databases. (MySql) This project also requires Redis to be working on the system, parameters can be configured on the `.env` file.
```
##### Install NPM dependencies
```sh
yarn install
```
##### Setup configuration
```sh
cp .env.example .env
```
##### Run Dev server
```sh
yarn dev
```
##### Build
```sh
yarn build
```
<br />

# Tasks of WorldCob
```sh
[x] BZ-35 is_autoplay in content library
[x] BZ-35 is_autoplay modal
[] ~
[] ~BZ-45 Hybrid registration with credential creation ~ new table checking
[] Open Room Representatives (Change text in Click action)
[] BZ-36 ~image ~video ~text ~click action)
[] Landing Page ~3 slider versions and replace the main banner
[] Modified Modal ~ booths ~ Enable autoplay -> not show in item option
[] Element Autoplay -> Content Library
[] Modal Video Element Autoplay
```
##### [BZ-35] is_autoplay in content library
```sh
# added an is_autoplay field to the content_library_element table
# a migration was added to add the is_autoplay field to the content_library_element table
```
```sh
ContentLibraryElementsAdminController > generalElementInputs ~ is_autoplay
```
```sh
# url's
'Youtube': https://www.youtube.com/embed/DMqbXKqlrfA
'Vimeo': https://vimeo.com/607608089
```

##### [BZ-45] Hybrid registration with credential creation
```sh
# definir dia lunes
```