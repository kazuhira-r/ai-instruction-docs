# 書籍管理API

書籍管理を行うREST APIを開発するリポジトリです。

## ドキュメント

基本的な構成などは、以下のドキュメントを参照してください。

- [アーキテクチャー](./architecture.md)
- [ステレオタイプ](./application-stereotype.md)
- [コーディング標準](./coding-standards.md)

開発の進め方は以下のドキュメントを参照してください。

- [開発プロセス](./development-process.md)

各ステレオタイプごとの実装方法は以下のドキュメントを参照してください。

- [実装パターン](./coding-patterns.md)

## 実行方法

アプリケーションを起動するには以下のコマンドを実行します。

```shell
$ mvn spring-boot:run
```

## テスト

ソースコードを追加、修正したらテストを行います。必要なテストコードは追加してください。

```shell
$ mvn test
```
