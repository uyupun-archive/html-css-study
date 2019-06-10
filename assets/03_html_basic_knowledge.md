# HTMLの基礎知識
HTMLの基礎知識として, 知っておくべきことを紹介する.  

コードを記述する際には, プレイグラウンドサービスの利用をおすすめする.  
プレイグランドサービスとは, コードの変更点をすぐに確認したい場合に便利なサービスである.  
以下におすすめのプレイグランドサービスを紹介する.
- [CodePen](https://codepen.io/)
- [JSFiddle](https://jsfiddle.net/)
- [Liveweave](https://liveweave.com/)


### タグと要素
タグ(又は, HTMLタグとも言う)とはHTMLにおいて `<>` や `</>` で記述されたもののことを指す.  
また, `<>` このタグを開始タグ, `</>` このタグを終了タグと言う.  
下記の場合, タグは `<div>` と `</div>` になり, `div` タグと呼ばれる.

```html
<div>hogehoge</div>
```

要素とはタグとその中身を含めたもののことを指す.  
下記の場合, 要素は `<div>hoge</div>` になる.

```html
<div>hogehoge</div>
```

タグの種類は多く, 以下ではよく使用するタグを紹介する.
- html
- head
- title
- meta
- link
- body
- div
- p
- a
- h1 ~ h6
- form
- label
- input
- ul
- table


### 属性
属性とは開始タグの後ろに半角スペース区切りで記述されたものの指す.  
以下の場合, 属性は `class` となり, `class` 属性という.  
また, 属性値は `hoge` となる.

```html
<div class="hoge">hogehoge</div>
```

属性はタグによって使用できるものが決められている.  
こちらの資料では紹介しないが, 属性とタグの関係を分かりやすくまとめた[HTML 属性リファレンス](https://developer.mozilla.org/ja/docs/Web/HTML/Attributes)を見ることをおすすめする.


### 記述例
以下の記述例を元に, 基本的な記述方法について解説する.

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8" />
    <title>タイトル</title>
    <link rel="stylesheet" href="css/style.css" />
  </head>
  <body>
    <div class="hoge">hogehoge</div>
  </body>
</html>
```

`<!DOCTYPE html>` を記述することで, 文書がHTML5で作成されたものであることを宣言している.  
このことをDOCTYPE宣言といい, DTD(Document Type Definition)に従った記述をすることを宣言している.

`html` タグはすべてのタグの親にあたり(ルート要素という), HTMLを記述する際は, すべて `<html>` タグ内に記述する.  
`lang="ja"` とすることでページの言語は日本語だということを表している.

`head` タグ内には文書のヘッダ情報を記述する.  
`meta` タグ `title` タグ `link` タグなどを使用し, 様々な情報を指定する.  

`body` タグ内には文書を記述する.  
