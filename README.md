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
1. `config/index.js`を下記のように書き換える<br>
    <img width="691" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/78744854-967fb680-799d-11ea-917e-b61593ed94fe.png">

1. コンテナに入り`npm run dev`を実行

1. http://localhost:9090 にようこそ的なページがでる


## 以降の開発

1. `docker-compose exec app sh`コンテナ内に入る

1. `npm run dev`で確認

1. `npm run build`でビルド

## お好み
.gitignoreの`/source/`を`/docker/`に書き換えるとvueプロジェクトだけが管理される
