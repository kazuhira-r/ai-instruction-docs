# テストコード標準

テストコードに関する標準を記載します。

## Spring標準

- Spring管理のBeanを使ったテストは、`@SpringBootTest`をクラスに指定します
- Controllerは`MockMvc`を使ってテストしてください
- Controller以外のSpring管理のBeanはインジェクションしてテストしてください

## Javaに関する標準

- テストクラスのクラス、メソッドに対するJavadocを記述してください
  - メソッドのJavadocはテスト仕様を記述してください