---
title: Markdown書き方サンプル
slug: markdown-guide
tags: [サンプル]
emoji: "📝"
---

Nekote Blogで使えるMarkdown記法のサンプル集です。それぞれの記法について、「書き方」のコードブロックと、そのすぐ下の「表示」を見比べられます。

## frontmatter

ファイル先頭の`---`で囲まれた部分がfrontmatterです。記事のタイトルなどのメタ情報をYAML形式で書きます。

書き方:

```md
---
title: 記事のタイトル
tags: [日記, お知らせ]
emoji: "📝"
---

本文
```

必須なのは`title`だけです。使えるキーの一覧は[ようこそ記事](./welcome.md)にまとまっています。

## 見出し

書き方:

```md
## 見出し

### 小見出し
```

この記事の各見出しが、そのまま表示例です。見出しのレベルは自動で整えられます。記事タイトルが`h1`、本文でいちばん上の見出しが`h2`になるようにずれるため、`# `始まりで書いても`## `始まりで書いても同じ表示になります。

## 段落と改行

書き方:

```md
空行を挟むと、別の段落になります。

改行を1つ入れただけの行は、
同じ段落の中でつながります。
```

表示:

空行を挟むと、別の段落になります。

改行を1つ入れただけの行は、
同じ段落の中でつながります。

段落の中で改行したいときは、行末に半角スペースを2つ置きます。

## テキストの装飾

書き方:

```md
**太字**、*斜体*、~~打ち消し線~~、`インラインコード`が使えます。

HTMLタグを併用すると、<mark>マーカー</mark>や<kbd>Ctrl</kbd>+<kbd>K</kbd>のようなキー表記、<small>小さい文字</small>も書けます。
```

表示:

**太字**、*斜体*、~~打ち消し線~~、`インラインコード`が使えます。

HTMLタグを併用すると、<mark>マーカー</mark>や<kbd>Ctrl</kbd>+<kbd>K</kbd>のようなキー表記、<small>小さい文字</small>も書けます。

使えるHTMLタグは安全な範囲に限定されています。

## リスト

書き方:

```md
- 箇条書き
- 箇条書き
  - 入れ子にできます

1. 番号付きリスト
2. 番号付きリスト

- [ ] タスクリスト（未完了）
- [x] タスクリスト（完了）
```

表示:

- 箇条書き
- 箇条書き
  - 入れ子にできます

1. 番号付きリスト
2. 番号付きリスト

- [ ] タスクリスト（未完了）
- [x] タスクリスト（完了）

## 引用

書き方:

```md
> 引用文です。
> 行を続けて書くと、ひとつの段落にまとまります。
>
> `>`だけの行を挟むと、段落を分けられます。
```

表示:

> 引用文です。
> 行を続けて書くと、ひとつの段落にまとまります。
>
> `>`だけの行を挟むと、段落を分けられます。

## リンク

書き方:

```md
[Nekote Blog](https://nekote.blog)への外部リンク。

同じリポジトリ内の記事への相対リンク: [ようこそ記事](./welcome.md)
```

表示:

[Nekote Blog](https://nekote.blog)への外部リンク。

同じリポジトリ内の記事への相対リンク: [ようこそ記事](./welcome.md)

記事ファイルへの相対パスで書いたリンクは、その記事の公開URLへ自動で書き換えられます。

## 画像

書き方:

```md
![サンプル画像](../images/sample-image.png)

<img src="../images/sample-image.png" alt="幅300pxのサンプル画像" width="300">
```

表示:

![サンプル画像](../images/sample-image.png)

<img src="../images/sample-image.png" alt="幅300pxのサンプル画像" width="300">

リポジトリ内の画像を相対パスで参照すると、同期時にNekote側へコピーされて配信されます。HTMLの`<img>`を使うと幅も指定できます。

## テーブル

書き方:

```md
| 項目 | 説明 |
| --- | --- |
| GFM | テーブル・タスクリストなどの拡張記法 |
| KaTeX | 数式の表示 |
```

表示:

| 項目 | 説明 |
| --- | --- |
| GFM | テーブル・タスクリストなどの拡張記法 |
| KaTeX | 数式の表示 |

## コードブロック

書き方:

````md
```js
export function greet(name) {
  return `Hello, ${name}!`;
}
```
````

表示:

```js
export function greet(name) {
  return `Hello, ${name}!`;
}
```

言語名を付けると、シンタックスハイライトが効きます。さらにフェンスへ`title="…"`を足すと、ファイル名などのキャプションが付きます。

書き方:

````md
```js title="app.js"
export function greet(name) {
  return `Hello, ${name}!`;
}
```
````

表示:

```js title="app.js"
export function greet(name) {
  return `Hello, ${name}!`;
}
```

## 数式

書き方:

```md
インライン数式は`$`で囲みます: $a^2 + b^2 = c^2$

ブロック数式は`$$`で囲みます。

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$
```

表示:

インライン数式は`$`で囲みます: $a^2 + b^2 = c^2$

ブロック数式は`$$`で囲みます。

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

## 区切り線

書き方:

```md
---
```

表示:

---

## コールアウト

`:::`で囲むと、補足や注意書きを枠付きで目立たせられます。

書き方:

```md
:::tip[ここがポイント]
`[...]`でタイトルを付けられます。**強調**や`コード`もそのまま使えます。
:::

:::warning
タイトルを省くと、アイコンと本文が横に並びます。
:::
```

表示:

:::tip[ここがポイント]
`[...]`でタイトルを付けられます。**強調**や`コード`もそのまま使えます。
:::

:::warning
タイトルを省くと、アイコンと本文が横に並びます。
:::

種類は`tip`・`info`・`note`・`warning`・`alert`・`check`・`help`の7つです。外側を`::::`にすれば入れ子にもできます。

書き方:

```md
::::note[入れ子の例]
コールアウトの中に、

:::check
別のコールアウトを入れられます。
:::
::::
```

表示:

::::note[入れ子の例]
コールアウトの中に、

:::check
別のコールアウトを入れられます。
:::
::::

## トグル（折りたたみ）

書き方:

```md
:::toggle[クリックで開く]
折りたたまれていた中身です。中身も**Markdownとして**解釈されます。
:::
```

表示:

:::toggle[クリックで開く]
折りたたまれていた中身です。中身も**Markdownとして**解釈されます。
:::

`{level=2}`〜`{level=4}`を付けると、サマリーを見出しにできます。HTMLの`<details>`でも同じような折りたたみを書けます。

## 目次

書き方:

```md
::toc
```

表示:

::toc

## カラム

書き方:

```md
::::columns
:::column
左のカラムです。リストや画像も入ります。
:::
:::column
右のカラムです。
:::
::::
```

表示:

::::columns
:::column
左のカラムです。リストや画像も入ります。
:::
:::column
右のカラムです。
:::
::::

## 図とキャプション

書き方:

```md
:::figure[画像のキャプション]
![サンプル画像](../images/sample-image.png)
:::
```

表示:

:::figure[画像のキャプション]
![サンプル画像](../images/sample-image.png)
:::

## ブックマーク（リンクカード）

書き方:

```md
::bookmark{url="https://nekote.blog"}
```

表示:

::bookmark{url="https://nekote.blog"}

URLのOGP情報を取得して、リンクカードとして表示されます。

## 埋め込み

書き方:

```md
::embed{url="https://www.youtube.com/watch?v=4I8f8y2IGBs"}
```

表示:

::embed{url="https://www.youtube.com/watch?v=4I8f8y2IGBs"}

対応サービスはYouTubeとXです。URLを1行だけで書いた場合も、自動で埋め込み（対応外のサービスはリンクカード）になります。

## 動画

書き方:

```md
[サンプル動画](../media/sample-video.mp4)
```

表示:

[サンプル動画](../media/sample-video.mp4)

リポジトリ内のmp4・webm・movへの相対リンクは、動画プレイヤーとして埋め込まれます。

## 音声

書き方:

```md
::audio{url="../media/sample-audio.mp3"}
```

表示:

::audio{url="../media/sample-audio.mp3"}

## ファイル

書き方:

```md
::file[サンプルPDF]{url="../media/sample-document.pdf"}
```

表示:

::file[サンプルPDF]{url="../media/sample-document.pdf"}

リポジトリ内のPDFやzipなどへのダウンロードリンクになります。

## 文字色とマーカー

書き方:

```md
<span class="u--keyText -keycolor:red">赤の文字色</span>と<span class="u--marker -keycolor:yellow">黄色のマーカー</span>が使えます。
```

表示:

<span class="u--keyText -keycolor:red">赤の文字色</span>と<span class="u--marker -keycolor:yellow">黄色のマーカー</span>が使えます。

色名は`gray`・`brown`・`orange`・`yellow`・`green`・`blue`・`purple`・`pink`・`red`の9つです。

記法の詳しいルールは[ドキュメント](https://nekote.blog/docs/others)を参照してください。
