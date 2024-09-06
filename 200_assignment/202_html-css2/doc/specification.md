# 仕様書

## Epic

### PJ 名

- 旅行ブログ作成 PJ

### 概要

- 旅するブロガーから旅行記事を公開するためのブログサイトの制作依頼
- WardPress によるサイト構築を行う
- TOP ページのみ静的サイトなため、HTML・CSS でコーディングを実施する

## Issue

### タイトル

- TOP ページの作成

### デザイン

- Figma 参照
- Figma の利用方法は `doc/figma` 参照

### 仕様

- コンテンツ幅は最大 `1200px`
  - Haeder・Footer の背景のみ全幅
- レスポンシブデザインに対応
  - 画面比率を維持しレイアウトが崩れないこと
- SP 版のデザインも対応
  - ブレークポイントは `750px` とします
- 画面タイトルは `specification_202` とします
- Header は固定する
- 各種 Link
  - 各種リンクは`#`で遷移しない形で OK
  - ロゴもリンクであること
  - 下線付きリンクはホバー時に underLine が消えること

### 課題としての補足

- reset CSS を読み込むこと
  - 下記コードを `head` 内に埋め込んで利用してください
  - その際、**必ず `index.css` より先に読み込む** ようにしてください

```HTML
<link rel="stylesheet" href="https://unpkg.com/ress/dist/ress.min.css" />
```

- font を指定してください
  - HTML は下記 Link タグを `head` 内に埋め込んで利用してください
  - CSS は Body に下記を埋め込み利用してください

```HTML
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100;300;400;500;700;900&family=Noto+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
```

```css
font-family: "Noto Sans", "Noto Sans JP", sans-serif;
```

- twitter の埋め込みは該当箇所で下記を埋め込み利用してください。(下記コードは編集しないこと)
  - 横幅などは CSS で対応すること

```HTML
<a
  class="twitter-timeline"
  data-height="315"
  href="https://twitter.com/X?ref_src=twsrc%5Etfw"
  >Tweets by X</a
>
<script
  async
  src="https://platform.twitter.com/widgets.js"
  charset="utf-8"
></script>
```
