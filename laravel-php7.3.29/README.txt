# 構築コマンド

docker-compose run php composer create-project --prefer-dist laravel/laravel .
docker-compose up -d


# Windows11 DockerDesktopでLaravelしたときにパーミッションがおかしくなってた

## 以下のコマンドでLaravelトップ表示できるようになる
docker-compose run php chmod -R 0777 /var/www/html/bootstrap
docker-compose run php chmod -R 0777 /var/www/html/storage

## 以下のコマンドでresourcesディレクトリ内の編集が可能になる
docker-compose run php chmod -R 0777 /var/www/html/resources
