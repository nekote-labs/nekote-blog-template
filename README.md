# Nekote Blog テンプレート

[Nekote Blog](https://nekote.blog)のGitHub連携をすぐ始められるテンプレートリポジトリです。サンプル記事2本・下書きの見本・固定ページ（about）が入っています。

## 使い方

1. このページ右上の「**Use this template**」→「Create a new repository」で、自分のリポジトリを作ります（Privateでも利用できます）
2. [Nekote Blogのダッシュボード](https://dash.nekote.blog)でブログを作り、記事ソースにGitHubを選んで、作ったリポジトリを接続します
   - コンテンツディレクトリは**空欄**（リポジトリルート）のままにします
3. 接続を確定すると初回同期が始まり、サンプル記事が公開されます

接続手順の詳細は[GitHub連携のドキュメント](https://nekote.blog/docs/github)を参照してください。

## 構成

```
├── posts/     ← ここの .md が記事になる
│   ├── welcome.md        … 「Nekote Blogへようこそ」（公開・更新の手順とfrontmatterの説明）
│   ├── markdown-guide.md … Markdown記法のサンプル集
│   └── draft-sample.md   … 下書き（draft: true）の見本。公開されません
├── pages/     ← ここの .md が固定ページになる
│   └── about.md
├── images/    ← 記事から相対パスで参照する画像置き場（場所・名前は自由）
└── README.md  ← posts/・pages/ の外にあるので同期されない
```

サンプルの記事・画像は自由に書き換え・削除してかまいません。
