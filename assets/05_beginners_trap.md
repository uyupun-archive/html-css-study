# 詳細度
CSSには**詳細度**(**Specificity**)と呼ばれる概念があり, 簡単に説明すると「スタイルが重複したときにどのスタイルを優先するか」を定量化したものである.  
定義したCSSが上手く適用されない場合は, 詳細度を疑うと良い.

詳細度はかなり複雑なため, 全て覚える必要は無いが, 一般的に適用範囲が広いセレクタほど優先度は低くなる.  
正確さには欠けるが, 以下に簡易的に詳細度をまとめた.  
上に行くほど詳細度が高い(つまり優先度が高い)ものとなっている.

- !important
- インライン記述(`style`属性に記述)
- idセレクタ
- 属性セレクタ・classセレクタ・擬似クラス
- 要素セレクタ・擬似要素
- 全称セレクタ

詳しい詳細度については, https://specifishity.com/ に分かりやすくまとめられている.

# ボックスモデル
HTMLの全ての要素は**ボックス**として表現され, ボックスは２種類の余白(`margin`, `padding`), 境界線(`border`), 幅(`width`), 高さ(`height`), そしてその中に入っている要素で構成される.  
ボックスモデルを意識してCSSを書くことで, レイアウト崩れで悩むことは格段に減るだろう.

<img src="../img/05_beginners_trap/001.png" width="600">

# displayプロパティ

// TODO: まずdisplayプロパティが何なのかを説明

displayプロパティの値には`block`, `inline`, `inline-block`, `table`, `flex`, `grid`などがある.  

// TODO: それぞれの値の特徴を表にまとめる

|プロパティ名|説明|
|:--|:--|
|block||
|inline||
|inline-block||
|table||
|flex||
|grid||

// TODO: ↓の内容をいい感じに表に移動できそう

その中でも, `block` , `inline` , `inline-block` は正しく理解していない人が多い.  
ここではそれぞれの特徴について説明する.

`block`は親要素の幅全体に広がって配置される.  
`width`, `height`, `padding`, `border`, `margin`の全てを使用できる.

`inline`は文字列の幅やフォントサイズが`width`と`height`の大きさになる.  
`width`, `height`, `margin-top`, `margin-bottom`は使用できない.

`inline-block`は`inline`と違い, `width`, `height`, `padding`, `border`, `margin`全てを使用できる.

// TODO: 簡単なサンプルを入れる

# positionプロパティ

// TODO: まずpositionプロパティが何なのかを説明

positionプロパティの値には`static`, `relative`, `absolute`, `fixed`の４種類が存在する.  

// TODO: それぞれの値の特徴を表にまとめる

親要素に `relative` , 子要素に `absolute` を指定するのがよく見る記述だ.  
この2つの値は, 相対位置への配置か絶対位置への配置という違いがある.  
また, `absolute` の親要素が `static` 以外の場合は, 親要素の左上が基準位置となり, `static` の場合はウィンドウの左上が基準位置となる.

// TODO: 簡単なサンプルを入れる

# レスポンシブ対応
一昔前までは, WebページはPCに対応しておけば問題が無かった.  
しかし現在では, PCの他にもタブレットやスマートフォンなど, 様々なサイズ, 操作性を持ったデバイスが登場している.  
したがって, Webページも様々なデバイスで閲覧されるということである.  
そのため, どのデバイスで閲覧してもレイアウトが崩れずに表示され, それぞれのデバイスに合った操作性を提供することが必要になる.  
それを実現するのがレスポンシブ対応と言われるものである.  

まず, レスポンシブ対応をするために `head` 内にviewportを設定する.  
viewportはブラウザの表示領域のことを指す.  
スマートフォン等のデバイスはPC版のブラウザよりも表示領域が狭いためviewportを指定し, 各デバイスの表示領域に合わせる必要がある.

```html
<head>
  <meta name="viewport" content="width=device-width,initial-scale=1">
</head>
```

上記のように `meta` タグ内で `name` 属性に `viewport` と値を入れることでviewportの情報を定義する.  
そして `content` 属性で `viewport` の幅と高さとスケールを指定する.  
`device-width` を指定することで, デバイスごとにviewportの幅が変更され, `initial-scale=1` を指定することで, その幅を等倍で表示する.

次にメディアクエリを設定する.  
メディアクエリとは, CSS3で追加された仕様の1つで, ブラウザの画面サイズに応じてCSSのスタイルを切り替える機能である.  
メディアクエリは `link` タグ内で指定するか, `@import` でCSSファイルを読み込む場合に指定するか, `@media` で指定するかの3種類ある.  
下記のコードはメディアクエリの指定の例である.

```html
<link rel="stylesheet" href="style.css" media="screen and (max-width: 767px)">
```

```css
@import url("style.css") screen and (max-width: 767px);
```

```css
@media (max-width: 767px) {
  ...
}
```

これらのコードは `width` が767px以下のブラウザに対してスタイルが適用される.  
また `min-width: 768px` と定義すると,  `width` が768px以上のブラウザに対してスタイルが適用される.

# CSS設計
CSSは思っているよりも破綻しやすい.  
そのため, ある程度CSSが複雑になることが予想されるのであれば, 初めのうちからCSS設計を導入することをお勧めする.  
CSS設計とは, class名の付け方やCSSファイルの分類に一定のルールを設けることで, 破綻しにくい堅牢なCSSを書くことができる仕組みの総称である.
CSS設計にも様々な種類があり, 導入の際にはそのプロジェクトに合ったCSS設計を採用すると良い.  
以下はCSS設計の例である.

|設計パターン|説明|
|:--|:--|
|OOCSS||
|SMACSS||
|BEM||
|MCSS||
|FLOCSS||
