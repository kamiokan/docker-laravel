Windows11 DockerDesktopでLaravelしたときにパーミッションがおかしくなってた

以下のコマンドでLaravelトップ表示できるようになる
docker-compose run php chmod -R 0777 /var/www/html/bootstrap
docker-compose run php chmod -R 0777 /var/www/html/storage

以下のコマンドでresourcesディレクトリ内の編集が可能になる
docker-compose run php chmod -R 0777 /var/www/html/resources
