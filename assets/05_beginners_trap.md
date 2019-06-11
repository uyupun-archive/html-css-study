# 初心者が陥りがちな罠

### 詳細度
CSSには詳細度があり, 変更点が反映されない時のだいたいの原因は詳細度が関係している.  
以下は詳細度の高順に並べたものである.

- !important
- インライン記述( `style` 属性に記述)
- idセレクタ
- 属性セレクタ・classセレクタ・擬似クラス
- 要素セレクタ・擬似要素
- 全称セレクタ

### padding border margin
`padding` , `border`, `margin` これらのプロパティを使用することで要素に余白等を付けることができる.  
特に何も考えず, これらを使用する方も多いはずだ.  
だが, 正しく理解していないとスタイルが崩れる原因になってしまう場合がある.  

<img src="../img/05_beginners_trap/001.png" width="600">

上記の画像から, `padding` , `border`, `margin` の順で余白が付くことが分かる.

### displayプロパティ
displayプロパティの値には `block` , `inline` , `inline-block` , `flex` , `table` などがある.  
その中でも, `block` , `inline` , `inline-block` は正しく理解していない人が多い.  
ここではそれぞれの特徴について説明する.

`block` は親要素の幅全体に広がって配置される.  
`width` , `height` , `padding` , `border`, `margin` 全てを使用できる.

`inline` は文字列の幅やフォントサイズが `width` と `height` の大きさになる.  
`width` , `height` , `margin-top` , `margin-bottom` は使用できない.

`inline-block` は `inline` と違い, `width` , `height` , `padding` , `border`, `margin` 全てを使用できる.

### positionプロパティ
positionプロパティの値には `static` , `relative` , `absolute` , `fixed` の4種類ある.  
親要素に `relative` , 子要素に `absolute` を指定するのがよく見る記述だ.  
この2つの値は, 相対位置への配置か絶対位置への配置という違いがある.  
また, `absolute` の親要素が `static` 以外の場合は, 親要素の左上が基準位置となり, `static` の場合はウィンドウの左上が基準位置となる.

### レスポンシブ対応
レスポンシブ対応とは, PC, タブレット, スマートフォンなど, 異なる画面サイズのデバイスでWebサイトを閲覧した際に, ページレイアウトを調整することである.  
レスポンシブ対応をすることで, SEO対策にも繋がる.

### CSS設計
システムが大きくなった際にクラス名が重複したりすることがある.  
そのようなことを防ぐために, CSSの設計をすることが大事だ.  
以下によく使用されるCSS設計をまとめる.

- OOCSS
- SMACSS
- BEM
- MCSS
- FLOCSS
