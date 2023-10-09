コンテナ立ち上げてappコンテナに入る
```
docker-compose up -d
docker-compose exec app /bin/bash
```
コンテナ内でLaravelプロジェクトを作成してマイグレーションを流す
```
composer create-project laravel/laravel .
php artisan migrate
```