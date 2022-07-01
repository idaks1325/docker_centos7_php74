
## Dockerインストール

brew install --cask docker
brew install docker-compose

実行テスト
docker -v
docker-compose -v

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

## 実行

・バックグラウンド実行
docker-compose up -d

・リビルド(php.iniの更新等)
docker-compose up --build -d

・キャッシュ等の全削除
docker-compose down --rmi all --volumes --remove-orphans

## Bash起動
docker-compose bash osphp bash