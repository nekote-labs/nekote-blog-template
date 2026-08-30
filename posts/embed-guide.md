---
title: 埋め込みコンテンツの書き方サンプル
slug: embed-guide
tags: [サンプル]
category: ガイド
emoji: "🧩"
---

対応サービスのURLを、URLだけの段落として書くと、自動で埋め込みコンテンツになります。このページでは対応サービスごとに、コードブロックとそのすぐ下の表示を見比べられます。

対応していないURLの段落はリンクカードになります。リンクカードやその他の記法は[マークダウン書き方サンプル](./markdown-guide.md)を参照してください。

## YouTube

```md
https://www.youtube.com/watch?v=4I8f8y2IGBs
```

https://www.youtube.com/watch?v=4I8f8y2IGBs

## X（旧Twitter）

ポストのURLを貼ります。

```md
https://x.com/nekote_tools/status/2088681433217069279
```

https://x.com/nekote_tools/status/2088681433217069279

## Vimeo

動画のURLを貼ります。

```md
https://vimeo.com/347119375
```

https://vimeo.com/347119375

## CodePen

ペンのURL（`codepen.io/{ユーザー名}/pen/{ID}`）を貼ります。

```md
https://codepen.io/chriscoyier/pen/gfdDu
```

https://codepen.io/chriscoyier/pen/gfdDu

## StackBlitz

プロジェクトのURL（`stackblitz.com/edit/{ID}`）を貼ります。

```md
https://stackblitz.com/edit/react
```

https://stackblitz.com/edit/react

## JSFiddle

フィドルのURL（`jsfiddle.net/{ユーザー名}/{ID}/`）を貼ります。

```md
https://jsfiddle.net/zalun/Yazpj/
```

https://jsfiddle.net/zalun/Yazpj/

## Figma

ファイルの共有URLを貼ります。URLに`node-id`が付いていると、そのフレームが初期表示されます。中身が表示されるのは、そのファイルを閲覧できる人だけです（ファイルの共有設定に従います）。

```md
https://www.figma.com/design/8UWo8O0bpqKeHKiONYrl0i?node-id=1-2
```

https://www.figma.com/design/8UWo8O0bpqKeHKiONYrl0i?node-id=1-2

## asciinema

録画のURL（`asciinema.org/a/{ID}`）を貼ります。

```md
https://asciinema.org/a/335480
```

https://asciinema.org/a/335480

## blueprintUE

ブループリントのURL（`blueprintue.com/blueprint/{ID}/`）を貼ります。

```md
https://blueprintue.com/blueprint/ha3ksn1c/
```

https://blueprintue.com/blueprint/ha3ksn1c/

## `::embed`で明示する

URLだけの段落と同じ結果を、`::embed`で明示的に書けます。

```md
::embed{url="https://vimeo.com/347119375"}
```

サービス名とIDの指定でも書けます。表示はどちらもURLだけの段落と同じです。

```md
::embed{service="youtube" id="4I8f8y2IGBs"}
```

::embed{service="youtube" id="4I8f8y2IGBs"}
