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

## headの作成
最初にHTML内の `head` 要素を記述していく.

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8">
    <link href="https://use.fontawesome.com/releases/v5.6.1/css/all.css" rel="stylesheet">
    <link rel="stylesheet" href="css/style.css">
    <link rel="icon" href="favicon.ico">
    <title>ほうかご勉強会</title>
  </head>
  <body></body>
</html>
```

## デフォルト値の変更
各タグにはデフォルト値が入っている.  
そのデフォルト値のまま使用したくない場合もある.  
そのため, デフォルト値を変更する.

```css
body {
  font-size: 16px;
  font-family: Verdana, sans-serif;
  color: #333;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
}

section {
  padding: 100px 0;
}

ul {
  list-style-type: none;
  padding: 0;
}
```

## 共通クラスの作成
`container` クラスを作成する.

```css
.container {
  padding: 0 20px;
  box-sizing: border-box;
  max-width: 768px;
  margin: 0 auto;
}
```

`max-width` を指定することで `width` が768pxより大きくならない.  
768pxというのはタブレット端末を使用した場合でもPCと同じように表示するためである.  
また, `box-sizing: border-box;` , `padding: 0 20px;` を指定しているため, `width` の周りに `padding` が付くのではなく, 内側に付くため, `widht` は728pxになる.  
`margin: 0 auto;` を指定することで, 中央に寄せている.

`grid` クラスを作成する.

```css
.grid {
  display: grid;
  grid-template-columns: 50% 50%;
}
```

## headerの作成
`header` を作成する.

```html
<header>
  <div class="container">
    <div class="grid">
      <div class="col">
        <p>放課後に勉強して、圧倒的成長。</p>
        <h1 class="title">ほうかご勉強会</h1>
        <a href="#" class="admission">入会はこちらから <i class="fas fa-external-link-alt"></i></a>
      </div>
      <div class="col">
        <img src="images/ass.png" alt="ASS" class="header-img">
      </div>
    </div>
  </div>
</header>
```

```css
header {
  background: linear-gradient(to right, #af384d, #b81a3e);
  padding: 100px 0;
}

header p {
  color: #fff;
}

.title {
  font-size: 34px;
  margin-bottom: 50px;
  font-weight: normal;
  color: #fff;
}

.admission {
  display: inline-block;
  padding: 10px 40px;
  background: #fff;
  text-align: center;
  color: #b81a3e;
  border-radius: 5px;
  opacity: 1;
}

.admission:hover {
  opacity: 0.7;
}

.header-img {
  width: 250px;
  height: 250px;
  box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.3);
}

header .col:last-of-type {
  padding: 10px;
  text-align: right;
  box-sizing: border-box;
}
```

## mainの作成

### section1の作成

### section2の作成

### section3の作成

## footerの作成

## レスポンシブ対応
