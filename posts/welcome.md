---
title: Nekote Blogへようこそ
slug: welcome
tags: [はじめに]
emoji: "👋"
thumbnail: ../images/sample-thumbnail.png
---

Nekote Blogへようこそ！これは、テンプレートリポジトリに入っているサンプル記事です。

この記事は`posts/welcome.md`ファイルから作られています。ファイルを編集してpushすれば、この記事も書き換わります。ひととおり確認したら、自由に書き換え・削除してかまいません。

## 記事を公開する

`posts/`フォルダにMarkdown（`.md`）ファイルを置いて、対象ブランチへpushするだけです。

1. `posts/`に`.md`ファイルを作る（サブフォルダで整理してもOK）
2. ファイルの先頭にfrontmatterで`title`を書く
3. 本文をMarkdownで書く
4. commitしてpushする

pushすると自動で同期され、記事が公開されます。「公開する」ための特別な操作はありません。

:::info
まだ公開したくない記事には、frontmatterに`draft: true`を書いておきます。このテンプレートの`posts/draft-sample.md`が下書きの見本です（ブログには表示されていません）。
:::

## 記事を更新する

公開と同じで、`.md`ファイルを編集してpushするだけです。変更のあった記事だけが自動で反映されます。

- 公開中の記事に`draft: true`を付けてpushすると、非公開に戻ります
- ファイルを削除してpushすると、その記事はブログから消えます

## frontmatterの書き方

ファイル先頭の`---`で囲まれた部分がfrontmatterです。記事のメタ情報をYAML形式で書きます。

```md
---
title: 記事のタイトル
date: 2026-08-01
slug: my-first-post
tags: [日記, お知らせ]
emoji: "📝"
thumbnail: ../images/sample-thumbnail.png
---

本文
```

| キー | 必須 | 役割 |
| --- | --- | --- |
| `title` | ✅ | 記事のタイトル |
| `draft` | - | `true`で下書き（非公開）。省略時は公開扱い |
| `date` | - | 公開日。省略時は初めて公開した日時になります |
| `slug` | - | 記事のURLスラッグ。省略時はファイル名が使われます |
| `tags` | - | 記事に付けるタグ。複数書けます |
| `category` | - | 記事に付けるカテゴリのslug |
| `emoji` | - | 記事のアイコンにする絵文字（1つだけ） |
| `thumbnail` | - | 記事のアイキャッチ画像 |
| `cover` | - | 記事ページ上部のカバー画像 |

必須なのは`title`だけです。`slug`を書いておくと、後からファイル名を変えても記事のURLが変わらないのでお勧めです。

## 固定ページ

`pages/`フォルダに置いた`.md`は、記事一覧に並ばない「固定ページ」になります。プロフィールやお問い合わせ先向けです。このテンプレートでは`pages/about.md`が見本です。

## もっと詳しく

- Markdownで書ける記法の実例は、[書き方サンプル](./markdown-guide.md)を見てください
- 接続手順・frontmatter・同期の仕組みの詳細は、[GitHub連携のドキュメント](https://nekote.blog/docs/github)にまとまっています
