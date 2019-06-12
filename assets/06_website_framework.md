# Webサイトの雛形

# header footer main nav aside article section
Webサイトは基本, `header` , `main` , `footer` の3要素からなっている.

<img src="../img/06_website_framework/001.png" width="400">

また, これらは以前まで `div` タグの `class` や `id` 属性に指定されていたが, HTML5から `<header>` のようにタグで指定できるようになった.  

これら3つ以外にもセクショニングコンテンツが追加された.  
セクショニングコンテンツは `nav` , `article` , `section` , `aside` の4つである.

`nav` はナビゲーションを意味し, メニューバーなどに使用される.  
`article` はそれ自体で独立した内容になっていることを示すセクションである.  
`section` は章・節・項のような見出しから始まるセクションであり,  `h1 ~ h6` 要素(ヘディングコンテンツ)を持つことが推奨されている.  
`aside` は補足情報を表すセクションである.  
以下はこれらのセクショニングコンテンツを使用した例である.

```html
<body>
  <header>
    ヘッダー
    <nav>メニュー</nav>
  </header>
  <main>
    <article>
      <section>
        <h1>見出し</h1>
        <p>本文</p>
        <aside>補足情報</aside>
      </section>
    </article>
    <aside>余談</aside>
  </main>
  <footer>フッター</footer>
</body>
```

# wrapper container
Webページを作成する際に, 横幅に余白を入れると見やすくなる.  
このようなレイアウトを作成するために `wrapper` , `container` がある.

<img src="../img/06_website_framework/002.png" width="400">

一般的な使用法は, `wrapper` はサイト全体に影響を及ぼすクラスとして使用する.  
`container` は各コンテンツごとの共通のクラスとして使用する.
