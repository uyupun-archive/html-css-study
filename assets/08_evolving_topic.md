# レスポンシブ対応
一昔前までは, WebページはPCに対応しておけば問題が無かった.  
しかし現在では, PCの他にもタブレットやスマートフォンなど, 様々なサイズ, 操作性を持ったデバイスが登場している.  
したがって, Webページも様々なデバイスで閲覧されるということである.  
そのため, どのデバイスで閲覧してもレイアウトが崩れずに表示され, それぞれのデバイスに合った操作性を提供することが必要になる.  
それを実現するのがレスポンシブ対応と言われるものである.  

レスポンシブ対応を行うには, HTMLとCSSの両方で設定する必要がある.

まず, HTMLでは`meta`タグに**viewport**の設定を行う.  
詳細は本書のレベルを超えるため説明を省くが, 簡単に説明するとviewportを設定することでスマートフォンなどの携帯型デバイスにも合った表示領域を設定することができる.  
これが上手く設定されていない場合, スマートフォンで閲覧してもPC版の表示がされてしまうことがある.

設定は以下のように行う.  
まず, `meta`タグの`name`属性に`viewport`と値を入れることでviewportの情報を定義する.  
次に, `content`属性には`width=device-width`と`initial-scale=1`を指定する.
`width=device-width`を設定することでデバイスごとにviewportの幅が自動で設定され, `initial-scale=1`を設定することで幅を等倍で表示する(IE以外では基本的にこれがデフォルト値なのだが, IEが生きている限りこの設定を書いておいた方が良いだろう).

```html
<!-- 省略 -->
<head>
  <meta name="viewport" content="width=device-width,initial-scale=1">
</head>
<!-- 省略 -->
```

次に, CSSでは**メディアクエリ**を設定する.  
メディアクエリとは, CSS3で追加された仕様の1つで, ブラウザの画面サイズに応じて適用するスタイルを切り替える機能である.  
メディアクエリの指定方法には大きく分けて３種類存在する.

- `link`タグ内で指定するパターン

```html
<link rel="stylesheet" href="style.css" media="screen and (max-width: 767px)">
```

- `@import`でCSSファイルを読み込む際に指定するパターン

```css
@import url("style.css") screen and (max-width: 767px);
```

- `@media`で指定するパターン  
このパターンが最も用いられる

```css
@media (max-width: 767px) {
  /* 省略 */
}
```

これらのコードは`width`が767px以下のブラウザに対してスタイルが適用される.  
また, `min-width: 768px`と定義すると, `width`が768px以上のブラウザに対してスタイルが適用される.


# CSSの単位
// TODO: px rem em % vh vw

# box-sizing

# z-index

# CSS設計
CSSは思っているよりも破綻しやすい.  
そのため, ある程度CSSが複雑になることが予想されるのであれば, 初めのうちからCSS設計を導入することをお勧めする.  
CSS設計とは, class名の付け方やCSSファイルの分類に一定のルールを設けることで, 破綻しにくい堅牢なCSSを書くことができる仕組みの総称である.
CSS設計にも様々な種類があり, 導入の際にはそのプロジェクトに合ったCSS設計を採用すると良い.  
以下はCSS設計の例である.

|設計パターン|説明|
|:--|:--|
|OOCSS|オブジェクト指向プログラミングの概念を取り入れたCSS設計(Object Oriented CSS).|
|SMACSS|OOCSSのコンセプトを元にして考えられたCSS設計.<br>Base, Layout, Module, State, Themeの5つのカテゴリに分けることで, 定義したレイアウトを管理しやすくなる.|
|BEM|CSS設計で最も難しいともいえる命名規則において, その問題を解決するために考えられたCSS設計.|
|MCSS|OOCSSとBEMのコンセプトを元にして考えられたCSS設計.<br>Foundation, Base, Project, Cosmeticの4つのレイヤーで構成される.|
|FLOCSS|上記4つのCSS設計を元にして考えられたCSS設計.<br>Foundation, Layout, Objectの3つのレイヤーと, Objectレイヤーの子レイヤーである, Component, Project, Utilityで構成される.|

# Pug

# Emmet

# Sass

# Bootstrap
