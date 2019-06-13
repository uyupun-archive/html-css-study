# Webサイトの構成

よく見かけるWebサイトは, タイトルなどを書いておく**ヘッダー**, そのWebサイトが提供する情報を置く**コンテンツ**, コピーライトなどを書いておく**フッター**の３つの部分から構成されていることが多い.  
これらの構成要素をHTML 5で記述する場合, それぞれ`header`, `main`, `footer`といったタグを用いる.

<img src="../img/06_website_framework/001.png" width="400">

さらにコンテンツを置く`main`の中身は ひとまとまりの記事を表す`article`, さらにそれぞれの節を表す`section`に分割できる.  
また, メインコンテンツではない補足的な情報の場合は`aside`タグで記述する.  
また, Webサイトのメニューは`nav`タグで記述する.

<img src="../img/06_website_framework/002.png" width="400">

ちなみに, HTML 5以前は`header`, `main`, `footer`, `article`, `section`, `aside`, `nav`といったタグが用意されていなかったため, `div`タグに`id`や`class`を指定することで表現していた.

ここまでの話をまとめて作成したWebサイトの雛形を以下に示す.

```html
<!-- 省略 -->
<body>
  <header>ヘッダー</header>
  <main>
    <nav>メニュー</nav>
    <article>
      <section>
        <h2>見出し１</h2>
        <p>本文１</p>
      </section>
      <section>
        <h2>見出し２</h2>
        <p>本文２</p>
      </section>
    </article>
    <aside>補足</aside>
  </main>
  <footer>フッター</footer>
</body>
<!-- 省略 -->
```

# WrapperとContainer
ディスプレイのサイズによって左右の余白を使い分ける必要がある.  
例えばディスプレイの横幅が広ければ左右に余白を入れないと読みにくくなるし, 逆にスマートフォンのようにディスプレイが小さいと左右に余白がありすぎるとコンテンツの表示領域が極端に狭まってしまう.  
こういった左右の余白を制御するための概念がWrapperとContainerである.  
WrapperはWebサイト全体に影響を及ぼすクラスとして使用し, Containerは各コンテンツごとに共通のクラスとして使用する.

<img src="../img/06_website_framework/003.png" width="400">

以下はWrapperとContainerを使用した例である.  
分かりやすいように背景色を付けて表示する.

```html
<body>
  <div class="wrapper">
    <header>
      ヘッダー
    </header>
    <div class="container">
      <nav>
        ナビゲーション
      </nav>
      <main>
        メイン
      </main>
    </div>
    <footer>
      フッター
    </footer>
  </div>
</body>
```

```css
body {
  background: lightgray;
}

.wrapper {
  max-width: 480px;
  margin: 0 auto;
  background: red;
}

header footer {
  background: orange;
}

.container {
  display: flex;
}

nav {
  width: 30%;
  background: blue;
}

main {
  width: 70%;
  background: green;
}
```
> 実行結果:  
> <img src="../img/06_website_framework/005.png" width="400">
