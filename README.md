# AI開発向けのメモ

## GitHub Copilot

### GitHub Copilot Chat

- [Customize chat responses in VS Code](https://code.visualstudio.com/docs/copilot/copilot-customization)
  - インストラクションファイルから、別のファイルを読み込むことはできない
    - つまり、規約などのドキュメントを用意しておき、インストラクションファイルから「○×を参照」と書いても読み取ってくれない（Markdownのリンクを書いても効果がない）
  - 自動で参照するインストラクションファイルのルール以外でインストラクションファイルとして読み込ませるには、`github.copilot.chat.codeGeneration.instructions`などを利用する
  - `applyTo`でファイルの絞り込みを行った場合、すでに存在するファイルにしか作用しない
    - このため、新規にファイルを作成する指示をした場合、特定の拡張子にマッチするインストラクションを書いていた場合は生成されるファイルの拡張子が一致していても無視される
  - `applyTo`で`src/main/java/**/*.java`のような書き方が効果があるかどうかは不明
  - インストラクションファイルは[edit mode](https://code.visualstudio.com/docs/copilot/chat/copilot-edits#_use-instructions-to-get-ai-edits-that-follow-your-coding-style)でも使える模様