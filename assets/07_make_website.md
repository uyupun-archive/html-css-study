# Webサイトの作成
この章では実際に小さなWebサイトを作成し, より実践的な手法について学んでいく.  
完成品は https://after-school-study-group.github.io/html-css-study/src/index.html を参照.

# 素材の入手
作成に先立って, 今回作成するWebサイトに必要な素材(画像, テキスト)をダウンロードする.  
https://github.com/after-school-study-group/html-css-study-parts にアクセスし, Download Zipを押すとZipファイルがダウンロードされるため, 各自のPCで展開しておく.

<img src="../img/07_make_website/001.png" width="300">

# ファイルとディレクトリの作成
まずは必要なファイルとディレクトリを作成する.
構成は以下の通りである.

```
my-site
  index.html
  favicon.ico
  css
    style.css
  images
    ass.png
    takashi1.jpg
    takashi2.jpg
    takashi3.jpg
```

なお, `favicon.ico`と`images`ディレクトリ以下の画像は前項でダウンロードした素材の中に入っている.

まず初めにPC版を作成し, その後レスポンシブ対応のためのコードを追加していく.  
レスポンシブ対応については, 次章で詳しく紹介している.

## ヘッダ情報の記述
まず初めに, ヘッダ情報を記述する.

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="css/style.css">
    <link rel="icon" href="favicon.ico">
    <title>ほうかご勉強会</title>
  </head>
  <body></body>
</html>
```

5行目:  
カレントディレクトリ内のcssフォルダ内の`style.css`というCSSファイルを読み込んでいる.

6行目:
カレントディレクトリ内の`favicon.ico`というファビコンを読み込んでいる.

## リセットCSSの作成
次にリセットCSSを作成する.  
リセットCSSとは, ブラウザによって異なるデフォルト値のCSSを打ち消し, ブラウザ間の表示を揃えるためのCSSファイルのことである.  
有名なリセットCSSには[Eric Meyer’s “Reset CSS” 2.0](https://cssreset.com/scripts/eric-meyer-reset-css/)や[Normalize.css](https://necolas.github.io/normalize.css/)がある.  
今回は簡易的なリセットCSSを作成する.  
また, 共通のスタイルを使用する要素型セレクタに関しても記述する.

```css
body {
  font-size: 16px;
  font-family: Verdana, sans-serif;
  color: #333;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

ul {
  list-style-type: none;
  padding: 0;
}

article {
  padding: 100px 0;
  background: #fff;
}

article:nth-of-type(2n) {
  background: #f8f8f8;
}
```

3行目:  
font-familyプロパティは, フォントのデザインを設定している.  
`Verdana`はMicrosoftが開発したサンセリフ体のフォントである.  
`sans-serif`は総称ファミリーと言い, 指定したフォントが使用できない閲覧者に, 最低限のフォントファミリーを提供するためのものである.  
今回は`sans-serif`を設定したので, ゴシック系のフォントを表示する.

7行目:  
box-sizingプロパティは, paddingとborderの幅と高さをwidthに含めるかどうかを設定する.  
`border-box`を指定することで, paddingとborderの幅と高さをwidthに含める設定にしている.

11行目:  
list-style-typeプロパティは, リストの項目の先頭に表示するマーカー文字の種類を示す.  
`none`を指定することで, マーカー文字を表示しないように設定している.

20行目:  
`article:nth-of-type(2n)`は, articleプロパティの偶数番目のものにスタイルを適用する.

## 共通クラスの作成
今回はCSS設計のOOCSSを元にクラスを作成する.  
CSS設計については次章で詳しく説明している.

```css
.container {
  padding: 0 20px;
  box-sizing: border-box;
  max-width: 768px;
  margin: 0 auto;
}

.grid {
  display: grid;
  grid-template-columns: 50% 50%;
}

.title {
  font-size: 34px;
  margin-bottom: 50px;
  font-weight: normal;
}

.sub-title {
  text-align: center;
  margin-top: 0;
  margin-bottom: 80px;
  font-size: 30px;
  font-weight: normal;
}

.image {
  width: 250px;
  height: 250px;
}
```

// TODO: コードの説明 以下も参考程度に
`max-width` を指定することで `width` が768pxより大きくならない.  
768pxというのはタブレット端末を使用した場合でもPCと同じように表示するためである.  
また, `box-sizing: border-box;` , `padding: 0 20px;` を指定しているため, `width` の周りに `padding` が付くのではなく, 内側に付くため, `widht` は728pxになる.  
`margin: 0 auto;` を指定することで, 中央に寄せている.


## コンテンツの作成
次に完成品を元に, コンテンツを作成する.

### ヘッダーの作成
まずはヘッダーから作成する.  
以下の画像のように, 要素ごとのまとまりを作成すると, HTML文が記述しやすくなる.

<img src="../img/07_make_website/002.png" width="600">

```html
<header>
  <div class="container">
    <div class="grid">
      <div class="col header-col">
        <p class="text-white">放課後に勉強して、圧倒的成長。</p>
        <h1 class="title text-white">ほうかご勉強会</h1>
        <a href="#" class="link">入会はこちらから</a>
      </div>
      <div class="col header-col">
        <img src="images/ass.png" alt="ASS" class="image shadow">
      </div>
    </div>
  </div>
</header>
```

### メインの作成

### section1の作成

### section2の作成

### section3の作成

### footerの作成

## レスポンシブ対応
