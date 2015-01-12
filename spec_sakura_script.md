# 如何かのさくらスクリプト実装状況

## スコープコマンド

- \0 \h
- \1 \u
- \p[]

## サーフェスコマンド

- \s[]
- \i[]
- <del>\4</del>
- <del>\5</del>

## バルーン、テキストコマンド

- \b[]
- <del>\_b[]</del>
- \n
- \n[half]
- \n[]
- <del>\_n</del>
- \c
- \l[x,y] (注意)
- \![*] (簡易実装)

### \l[x,y]

現スコープ側のカーソル位置をXYの座標に移動する。X,Yについては、以下の定義方法が可能である。

- 数値
    - バルーンの文字描画範囲左上からのピクセル単位座標
- (省略)
    - 移動しない。x,y両方ともに省略すると無効果。
- 数値em
    - バルーンの文字描画範囲左上からの文字高さ単位座標。1em＝タグを書いた時点での文字高さ。小数点指定可能。
- 数値%
    - バルーンの文字描画範囲左上からの文字高さ単位座標。100%＝タグを書いた時点での文字高さ。小数点指定可能。
- @任意
    - 現在の文字描画位置からの相対座標。Xがマイナス値だと左、Yがマイナス値だと上。emや%指定との共存可能。

- xまたはyがJavaScriptの数値として解釈できない場合無効となる。
- xのみを書いてカンマを書かずにyを省略することが可能である。
- yのみを書いてxを省略する場合はカンマが必須である。
- バルーンの表示位置外の位置を指定する場合の挙動は未定義であり、指定してはならない。

## 文字変更コマンド

実装なし

## ウエイトコマンド

- \w1 - \w9
- \_w[]
- \x (簡易実装)
- \t
- \_q
- \_s
- \_s[]

## 選択肢コマンド

- \q[タイトル,ID]
- \q[タイトル,OnID,r0,r1,...]
- \q[タイトル,ID,r2,r3...]
- \q[タイトル,script:実行内容]
- \q[ID][タイトル] \q*[ID][タイトル]
- \z
- \__q[ID,...]
- \*
- \![set,choicetimeout,時間]
- \_a[OnID,r0,r1...]
- \_a[ID]
- \_a[ID,r2,r3...]

## 選択肢マーカー変更コマンド

実装なし

## イベントコマンド

- \e
- \-
- <del>\6</del> (実装予定なし)
- <del>\7</del> (実装予定なし)
- <del>\+</del>
- <del>\_+</del>
- <del>\![change,ghost,ゴースト名]</del>
- <del>\v</del>
- <del>\![set,windowstate,stayontop]</del>
- <del>\![set,windowstate,!stayontop]</del>
- <del>\![set,windowstate,minimize]</del>
- \![raise,...]

## サウンドコマンド

実装なし

## オープンコマンド

- <del>\j[]</del>
- <del>\![open,browser,パラメータ]</del>
- <del>\![open,mailer,パラメータ]</del>
- <del>\__t</del>
- <del>\![open,teachbox]</del>
- <del>\![close,teachbox]</del>
- \__c (簡易実装)
- \![open,communicatebox] (簡易実装)
- <del>\![close,communicatebox]</del>
- \![open,inputbox,...] (簡易実装)
- <del>\![close,inputbox,ID]</del>

## プロパティシステム操作コマンド

実装予定なし

## 未分類コマンド

- <del>\![execute,http-get,URL]</del> (実装予定なし)
- <del>\![enter,passivemode]</del> (実装予定なし)
- <del>\![leave,passivemode]</del> (実装予定なし)
- <del>\![enter,inductionmode]</del> (実装予定なし)
- <del>\![leave,inductionmode]</del> (実装予定なし)
- <del>\![reloadsurface]</del>
- \_u[]
- \_m[]
- \&[]
- <del>\m[umsg,wparam,lparam]</del> (実装予定なし)

## 環境変数

実装なし
