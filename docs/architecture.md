# アーキテクチャー

本アプリケーションの基本的な構成、アーキテクチャーを解説します。

## 基本的な構成

- REST API
  - データフォーマットはJSONとする
- 認証・認可制御を行う

## 構成技術要素

- プログラミング言語
  - Java 21
- フレームワーク
  - Spring Boot 3.4.6
- アプリケーションサーバー
  - Apache Tomcat 10.1
- セキュリティ
  - Spring Security
- データベースアクセスライブラリー
  - MyBatis Spring Boot Starter 3.0.4
- データベースマイグレーション
  - Flyway
- テスト
  - JUnit 5
  - AssertJ
  - AssertJ-DB
- ビルドツール
  - Apache Maven 3.9.9
- 自動生成ツール
  - MyBatis Generator 1.4.2
    - Mavenプラグインとして利用
- データベース
  - MySQL 8.4
