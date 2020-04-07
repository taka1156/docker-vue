# Dockerでvueプロジェクトを作成

## はじめ方

### docker-compose

1.  `cd ./docker`に移動

1. `docker-compose build`でコンテナ作成

1. `docker-compose up -d`でコンテナ起動

1. `docker-compose exec app sh`コンテナ内に入る

1. `vue init webpack {プロジェクト名}`でプロジェクト作成

1. `exit`で抜ける

1. `docker-compose down`でコンテナ停止

### vue

そのうち更新

## 以降の開発

1. `docker-compose exec app sh`コンテナ内に入る

1. `npm run dev`で確認

1. `npm run build`でビルド

## お好み
.gitignoreの`/source/`を`/docker/`に書き換えるとvueプロジェクトだけが管理される
