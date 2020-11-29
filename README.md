
# Dockerでvueプロジェクトを作成

## はじめ方

### docker-compose

1.  `cd ./docker`に移動

1. `docker-compose build`でコンテナ作成

1. `docker-compose up -d`でコンテナ起動

1. `docker-compose exec app sh`コンテナ内に入る

1. `exit`で抜ける

1. `docker-compose down`でコンテナ停止

## vue
1. `vue create {プロジェクト名}`でプロジェクト作成

1. `vue.config.js`を作り、下記のように書く<br>
    <!--<img width="691" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100516911-7c177900-31ca-11eb-9ff1-c57e3cc01e61.png">-->
   ```javascript
   module.exports = {
      devServer: {
         port: 9090
      }
   }
    ```
 

1. `cd {プロジェクト名}`,`npm run dev (yarn dev)`を実行

1. http://localhost:9090 にようこそ的なページがでる<br>
   <img height="250" width="400" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100516935-a5d0a000-31ca-11eb-82ab-b2b0a1cfd517.png">

## Nuxt
1. `npx create-nuxt-app {プロジェクト名}`

1. `nuxt.config.js`を下記のように書き換える<br>
   <!--<img width="691" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100515469-d101c200-31bf-11eb-9b44-aa4344531167.png">-->
   ```javascript
   export default {
      server: {
         port: 9090,
         host: '0.0.0.0'
      }

      //...略
   }
   ```

1. `cd {プロジェクト名}`,`npm run serve (yarn serve)`を実行

1. http://localhost:9090 にようこそ的なページがでる<br>
   <img height="250" width="400" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100516934-a5380980-31ca-11eb-8c61-ff608304c5af.png">
   

## Gridsome
1. `gridsome create {プロジェクト名}`

1. `gridsome.config.js`を下記のように書き換える<br>
   <!--<img width="691" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100516465-72d8dd00-31c7-11eb-96e7-7177eb607e7a.png">-->
   ```javascript
   module.exports = {
      siteName: 'Gridsome',
      port: 9090,
      plugins: []
   }
   ```

1. `cd {プロジェクト名}`,`npm run devlop (yarn devlop)`を実行

1. http://localhost:9090 にようこそ的なページがでる<br>
   <img height="250" width="400" alt="スクリーンショット 2020-04-08 13 33 30" src="https://user-images.githubusercontent.com/47517002/100516929-a1a48280-31ca-11eb-9efe-33288194129a.png">

## 以降の開発

1. `docker-compose exec app sh`コンテナ内に入る

1. `npm run dev`で確認

1. `npm run build`でビルド

## お好み
.gitignoreの`/source/`を`/docker/`に書き換えるとvueプロジェクトだけが管理される

