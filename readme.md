# 結果
公開画面
http://localhost:8080

phpMyAdmin
http://localhost:8888
DB: testdb
root / root
testuser / testpw

# 導入

## インストール

インストール
brew install --cask docker
brew install docker-compose

実行テスト
docker -v
docker-compose -v

## cakephpのtests利用まで
cd projectA
docker-compose up -d
docker-compose exec osapp bash
cd /var/www
composer install
./vendor/bin/phpunit

# その他

## ディレクトリ構成
projectA
 - docker-compose.yml
 - sql
    - 〇〇.sql
 - docker
    - Dockerfile
    - マウントするphp.init等
 - .vscode
    - launch.json


## コマンド類

・バックグラウンド実行
docker-compose up -d

・リビルド(php.iniの更新等)
docker-compose up --build -d

・キャッシュ等の全削除
docker-compose down --rmi all --volumes --remove-orphans

・Bash起動
docker-compose bash osphp bash
