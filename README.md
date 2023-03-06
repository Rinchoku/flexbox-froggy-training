# flexbox-froggy-training
[Flexbox Froggy](https://flexboxfroggy.com/#ja)を行ったことのログ

## 概要

`display: flex`をとるスタイルに対する勉強コンテンツ
後に記載

## `junstify-content`
水平方向に要素を並べるのに利用するプロパティ
取りうる値として、下記がある

* `flex-start`:左側に並べる
* `flex-end`:右側に並べる
* `center`:中央に並べる
* `space-between`:対象領域内の要素に対してスペースを適度に入れて並べる
* `space-around`:対象領域内の要素に対して、左右の領域にもスペースを入れる(space-betweenは両端に要素がいく)

## `align-items`

垂直方向に要素を並べるのに利用するプロパティ
取りうる値として、下記がある

* flex-start: アイテムはコンテナーの上部に並びます。
* flex-end: アイテムはコンテナーの下部に並びます。
* center: アイテムはコンテナーの垂直方向中央に並びます。
* baseline: アイテムはコンテナーのベースラインに表示されます。
* stretch: アイテムはコンテナーの大きさに合うよう広がります。

`align-self`も存在し、個別の要素に対して同じようなことができるプロパティ

## `flex-direction`

要素が配置される方向を示すプロパティ
取りうる値として、下記がある

* row: アイテムは文章と同じ方向に配置されます。
* row-reverse: アイテムは文章と逆の方向に配置されます。(左→右で配置されてるのを、右→左に配置するような形)
* column: アイテムは上から下に向かって配置されます。（左→右で配置されてるのを、上→下に配置するような形）
* column-reverse: アイテムは下から上に向かって配置されます。（左→右で配置されてるのを、下→上に配置するような形）

## `order`

要素の並びを任意に切り替えたい場合に利用するプロパティ
指定する値を変えることで、優先度が変わる

## `flex-wrap`

行内に対して、要素の方が多い場合にいい感じにしてくれるプロパティ
デフォルトはその領域内に無理やり収める`nowrap`になっていそう

* nowrap: 全てのアイテムは、ひとつの行にフィットします。
* wrap: アイテムは他の行へ折り返します。
* wrap-reverse: アイテムは逆順になって他の行へ折り返します。

## `align-content`

複数行になる場合、その行間に対する余白をどうするかを示すプロパティ

* flex-start: 行はコンテナーの上側に詰められます。
* flex-end: 行はコンテナーの下側に詰められます。
* center: 行はコンテナーの中央に詰められます。
* space-between: 行はその間に等しい間隔を空けて表示されます。
* space-around: 行はその周囲に等しい間隔を空けて表示されます。
* stretch: 行はコンテナーに合うよう引き延ばされます。

## 補足

`justify-content` および `align-items`は同じ要素に対して適応することができる
そのため、枠を確保したのち枠の中心に入れるといったことが可能になる
(ひと昔などはtop,leftやtranslateを使ってたりしたが、それを行う必要がなくなる)

`flex-direction:row-reverse`を利用すると左右が逆転しているため、`justify-content`も逆になる(flex-startが右側に並べることになる)
`flex-direction:column`を利用した際、`justify-content`と`align-items`が見る方向が逆転する
(flex-directionのreverseがどういう時に使うのかはよくわかっていない)

`flex-direction`と`flex-wrap`は一緒に使われることがあるため `flex-flow`というプロパティが存在する
第一引数にflex-direction、第二引数にflex-wrapの値を取る

