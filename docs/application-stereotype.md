# ステレオタイプ

本アプリケーションで使用するステレオタイプおよびパッケージ構成を記述します。

## ステレオタイプ

- Controller
  - リクエストを受け取り、レスポンスを返却する
  - 処理そのものはServiceに委譲する
  - 命名規則は<リソース名（複数形）>Controller
- Request/Response
  - HTTPリクエストおよびHTTPレスポンスを表す
  - リクエストパラメーターのみで完結するバリデーションは、Requestに実装する
  - 命名規則はそれぞれ<目的>Request、<目的>Response
- Service
  - ビジネスロジックを実装する
  - 命名規則は<目的>Service
- Dto
  - Serviceのインターフェース
  - 命名規則は<目的>Dto
- Mapper
  - MyBatisのMapperインターフェース
  - SQLはアノテーションで実装する
  - 命名規則は<目的>Mapper
- Entity
  - MyBatisのModel
  - テーブルと対になる、検索結果や検索条件を表す
  - クラス名にステレオタイプに合わせたsuffixは付与しないこと

## パッケージ構成

- com.example.app … ルートパッケージ
- com.example.app.<機能名>.controller … Controllerを配置
- com.example.app.<機能名>.request … Requestを配置
- com.example.app.<機能名>.response … Responseを配置
- com.example.app.<機能名>.service … Serviceを配置
- com.example.app.<機能名>.dto … Dtoを配置
- com.example.app.<機能名>.mapper … 機能ごとのMapperを配置
- com.example.app.<機能名>.entity … JOINした結果や検索条件などのEntityを配置
- com.example.app.mapper … MyBatis Generatorで生成したMapperを配置
- com.example.app.entity … MyBatis Generatorで生成したEntityを配置
- com.example.app.common … 共通機能を配置
- com.example.app.common.exception … アプリケーション共通で使う例外クラスを配置
