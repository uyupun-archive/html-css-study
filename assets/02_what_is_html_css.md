# HTMLとは
**HTML**とは, **Hyper Text Markup Language**の略で, 平たく言うとWebページの構造を記述するためのマークアップ言語である.  
現在は**W3C**と**WHATWG**の２つの団体によって仕様の策定が行われている.

Google Chromeの場合, 任意のWebページを開いて右クリックして出てきたメニューから「ページのソースを表示」を選択することで, そのWebページのHTMLやCSSを確認することができる.  
他のブラウザでも大抵似たような方法で確認ができる.

<img src="../img/02_what_is_html_css/001.png" width="700">

# W3CとWHATWG
**W3C**(**World Wide Web Consortium**)はWeb技術の仕様の策定・標準化を行う非営利団体である.  
**ティム・バーナーズ＝リー**によって1994年に設立された.  
現在は**HTML**, **XHTML**, **XML**, **CSS**, **DOM**などの仕様を策定している.

**WHATWG**(**Web Hypertext Application Technology Working Group**)はHTMLとその関連技術の仕様の策定・標準化を行うコミュニティである.  
W3Cに不満を持った開発者たちによって2004年に結成された.  
W3Cの対抗組織として始まったWHATWGだが, HTML5はWHATWGが提唱したものをもとに仕様策定された.

# HTMLの仕様策定の流れ
W3Cで勧告されるHTMLの仕様は「**W3C勧告プロセス**」と呼ばれる仕組みで審議・検討され, **作業草案** -> **最終草案** -> **勧告候補** -> **勧告案** -> **W3C勧告** という５つの段階を踏む.  

これに対し, WHATWGでは**HTML Living Standard**というHTMLの仕様が存在し, これはバージョン番号や何年何月何日に策定されたかという概念がなく, 日々更新されている.  
W3Cが勧告するHTML 5以降の仕様と差分は少なかったものの多少のズレはあり, これからそれぞれの仕様がどうなるのか懸念されていたが, つい先日2019年5月28日にW3Cは独自のHTMLの仕様策定を終了し, HTML Living Standardに一元化することを発表した.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">🗞 W3C and the WHATWG signed an agreement to collaborate on a single version of HTML and DOM <a href="https://t.co/UQVjTmH0g7">https://t.co/UQVjTmH0g7</a></p>&mdash; W3C (@w3c) <a href="https://twitter.com/w3c/status/1133300432133079041?ref_src=twsrc%5Etfw">May 28, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

ちなみに, HTML Living StandardのGitリポジトリは https://github.com/whatwg/html から参照できる.

# なぜ標準化するのか
業界の標準として仕様を策定することで, それに準拠した(つまり仕様に沿った機能を実装している)Webブラウザが作られる.  
そうすることにより, 開発者はWebブラウザごとの互換性を考えることなくプログラムを作成できる.  

# HTMLの歴史

|バージョン|説明|
|:--|:--|
|HTML 1.0|1993年6月に策定.<br>HTMLは**SGML**というマークアップ言語を参考に開発された.|
|HTML+|1993年11月に策定. HTML 1.0の上位互換.<br>テーブルなどが追加された.|
|HTML 2.0|1995年11月に策定. HTML 2.0以降, HTMLの仕様策定はIETFではなくW3Cが行うこととなった.|
|HTML 3.0|策定作業が行われたがドラフト段階で破棄.|
|HTML 3.2|1997年1月14日に策定.|
|HTML 4.0|1997年12月18日に策定.|
|HTML 4.01|1999年12月24日に策定.<br>これをベースにしてXHTML 1.0が策定される.|
|HTML 5|2014年10月28日に策定.<br>大幅にアップデートされ, 様々な要素や属性が追加される.|
|HTML 5.1|2016年11月1日に策定.|
|HTML 5.2|2017年12月14日に策定.|

HTMLの先祖SGML, XML, XHTML, DTD宣言

HTMLの仕様, CSSの仕様(レベルなど)

HTML(HyperText Markup Language), Webページの土台, タグ, 要素, 属性, Pug(廃れた), 歴史

# CSSとは
CSS(Cascading Style Sheets), Webページのスタイル, HTMLで記載した物を装飾する, SASS, Bootstrap, 歴史
