# Requirements

* [Node.js](https://nodejs.org/ja/)
* [Honkit](https://github.com/honkit/honkit)
* [a5doc](https://github.com/a5doc/cli)

# Installation

```shell
yarn install
```

# Local Development

```shell
yarn serve
```

serve localhost:4000

# Build

```shell
yarn build
```

# Summary

Honkit を使用した各種設計用のテンプレート

* 機能設計
* API
* DB

# 各設計の作成方法

## 機能設計の作成

1. `./src/design/`に`xxx.md`を作成する
2. `./src/SUMMARY.md`に作成した設計に合わせて項目を追加する

## API仕様の作成

1. `./src/api/swagger.yaml`にAPIを追加する
    * [OpenAPI Specification 3.0](https://swagger.io/specification/)の形式で記述する
2. 以下のコマンドを実行して、`./src/api/swagger.html`を更新する

    ```shell
    yarn swagger-html
    ```

## テーブル定義の作成

1. `./src/db/`に`xxx.yaml`を作成する
2. 以下のコマンドを実行する

    ```shell
    yarn table
    ```

3. `./src/db/table/`にmdファイルが作成される
4. `./src/SUMMARY.md`に作成した設計の項目に合わせて追加

## ER図の作成

1. テーブル定義を作成 or 修正する
2. 以下のコマンドを実行する

   ```shell
   yarn erd
   ```

3. `./src/db/er/er-all.md`が作成させる

※全体のER図を作成しているが、テーブルが増えると図のレイアウトがうまくいかないときがあるので、その場合は適当なグループにわける必要がある
