# インターネットとWWW
インターネットはTCP/IPプロトコルスタックを利用して相互接続されたネットワークのことである.  
例えば, 電子メール(SMTP/POP/IMAP), ファイル転送(FTP/TFTP), **WWW**(**HTTP**)等がある.  
つまり, **WWW**(**World Wide Web**)はインターネットの技術の一部である.

WWWは普段, GoogleやYahoo!といった検索エンジンで検索して見ているWebページの集まりのことである.  
プロトコルに**HTTP**を使用し, **HTML**/**CSS**/**JavaScript**といった言語を使用し, **文書のやり取り**を行うシステムである.  
文書のやり取りは基本的に**Webブラウザ**(**Google Chrome**, **Firefox**等)と**Webサーバ**(**Apache**, **Nginx**等)の間で行われる.  
今回はその中でもHTMLとCSSに焦点を絞って学び, 基本的なWebページを作成できるようになるところを目指す.  
その前に少し, インターネットの歴史やHTML/CSSの仕組みについて学んでいこう.

# インターネットの歴史

|西暦|概要|
|:--|:--|
|1966|ARPANET計画の開始. ARPANETはインターネットの起源となったネットワーク.|
|1977|OSI参照モデルの策定が開始. OSI自体は普及せず, TCP/IPが普及したがネットワークの基本モデルとしては広く参照されるようになった.|
|1972|イーサネットの原型の開発がゼロックス社にて開始される.|
|1973|TCP/IPの開発が開始される.|
|1988|IANAの設立. IANAはIPアドレス・ドメイン名・ポート番号の標準化・管理を行う組織.|
|1993|WWWを開放することをCERNが発表. それまでは一部の研究者だけが使える仕組みだった.|
|1993|NCSA MosaicというWebブラウザの誕生. テキストと画像を同一のウィンドウに描画できる最初のブラウザだった.|
|1994|W3C(World Wide Web Consortium)の設立. HTML/CSSの標準化を行っている.|
|1998|ICANNの設立. これ以降, IANAはICANNの下部組織となった.|
|2004|WHATWGの設立. W3Cの対抗団体として設立されたが, 現在はW3Cと共に仕様の策定を行っている.|
|2014|HTML5が勧告される.|

# WWWを支える３つの技術

- URI(URL)
- HTTP(Hyper Text Transfer Protocol)
- HTML
その他にもCSSやJavaScriptなど

# HTMLとは
HTMLとは, Hyper Text Markup Languageの略で, 平たく言うとWebページの構造を記述するためのマークアップ言語である.
HTMLの先祖SGML, XML, XHTML, DTD宣言

HTMLの仕様, CSSの仕様(レベルなど)

HTML(HyperText Markup Language), Webページの土台, タグ, 要素, 属性, Pug(廃れた), 歴史

# CSSとは
CSS(Cascading Style Sheets), Webページのスタイル, HTMLで記載した物を装飾する, SASS, Bootstrap, 歴史
